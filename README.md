# ingress steps-K8s

Deploy ingress with nginx controller for  devops.in domain with cert-bot and three alb with cluster ip and three nodeport service with url devops.in/homepage, devops.in/blog, devops.in/course-list respectively for nodes with 3 replicaset each.


1. Install nginx Ingress Controller:
   ```bash
   kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.1.1/deploy/static/provider/cloud/deploy.yaml
   ```

2. Deploy cert-manager for Let's Encrypt certificate management:
   ```bash
   kubectl apply -f https://github.com/jetstack/cert-manager/releases/download/v1.5.4/cert-manager.yaml
   ```

3. Create a ClusterIssuer for Let's Encrypt (similar to previous yaml).

4. Deploy TLS Secret for your domain.

5. Deploy Ingress for devops.in domain (similar to previous yaml).

6. Deploy three NodePort Services (similar to previous yaml).

7. Deploy three Replication Controllers (Deployments) with three replicas each (similar to previous yaml).

Make sure to replace placeholders like email, paths, and image names with your actual values.
