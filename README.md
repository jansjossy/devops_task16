# devops_task16
# DevOps Internship - Task 16: Kubernetes Deployments & Rollouts
**User:** Amal

## 1. Deployment Configuration
- **Workload Type:** Deployment (`apps/v1`)
- **Application:** Nginx
- **High Availability:** Configured with `replicas: 3` (Scaled dynamically to 5).
- **Health Checks Configured:**
  - **Readiness Probe:** Checks HTTP port 80 every 5 seconds (5s initial delay) to ensure the Pod is ready to route traffic.
  - **Liveness Probe:** Checks HTTP port 80 every 20 seconds (15s initial delay) to restart frozen or crashed containers automatically.

## 2. Operations Performed
- **Scaling:** Successfully scaled the ReplicaSet horizontally from 3 to 5 Pods using `kubectl scale`.
- **Rolling Update:** Triggered a zero-downtime rollout by updating the container image from `nginx:1.24` to `nginx:1.25`.
- **Version Control & Rollback:** Monitored the rollout status, inspected the revision history using `kubectl rollout history`, and successfully restored the previous stable state using `kubectl rollout undo`.

## 3. Evidence

<img width="960" height="1020" alt="Screenshot 2026-02-14 121842" src="https://github.com/user-attachments/assets/e57c4ddc-2f86-450a-a9fb-82adcb382691" />
<img width="960" height="1020" alt="Screenshot 2026-02-14 121839" src="https://github.com/user-attachments/assets/b67813bc-7440-4ca8-ab10-0d15e041ca6f" />
<img width="960" height="1020" alt="Screenshot 2026-02-14 121821" src="https://github.com/user-attachments/assets/6fe0bdf2-4fbf-43f9-9b9f-6c5d5a1a9aba" />
