# Supermario-argocd

# Step 1: Initialize your Terraform workspace
terraform init

# Step 2: Generate and show an execution plan
terraform plan

# Step 3: Apply the changes required to reach the desired state of the configuration
terraform apply

# Step 4: Retrieve the ArgoCD default admin(username) password and decode it using Base64 extension
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}"

# Step 5: Destroy all resources created by the Terraform configuration
terraform destroy
