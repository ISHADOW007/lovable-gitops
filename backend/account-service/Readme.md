5. Install Argo Rollouts (one time)
kubectl create namespace argo-rollouts

kubectl apply -n argo-rollouts \
-f https://github.com/argoproj/argo-rollouts/releases/latest/download/install.yaml


6. Verify Installation
kubectl get pods -n argo-rollouts




7. Commit
git add .

git commit -m "Convert account-service to Argo Rollouts Blue-Green"

git push origin main

Argo CD will automatically sync the changes.




8. Watch Rollout
kubectl argo rollouts get rollout account-service \
-n lovable-core --watch




9. Test Preview
kubectl port-forward svc/account-service-preview \
8081:80 -n lovable-core

Open:

http://localhost:8081/account/actuator/health




10. Promote

After QA approval:

kubectl argo rollouts promote account-service \
-n lovable-core




11. Rollback
kubectl argo rollouts undo account-service \
-n lovable-core





Developer

↓

Git Push

↓

GitHub

↓

Argo CD Sync

↓

Rollout Resource

↓

Argo Rollouts Controller

↓

Blue ReplicaSet
Green ReplicaSet