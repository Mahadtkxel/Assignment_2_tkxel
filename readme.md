Steps:
- Installing azure CLI: curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
- check subscription ID and tenant ID: 
    az account show --query "{SubscriptionID:id}" --output table
    az account show --query "{TenantID:tenantId}" --output table

https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-terraform?tabs=azure-cli

- export environment variables:
    export ARM_CLIENT_ID="your-app-id"
    export ARM_CLIENT_SECRET="your-client-secret"
    export ARM_SUBSCRIPTION_ID="your-subscription-id"
    export ARM_TENANT_ID="your-tenant-id"
- In playground cannot create new resource groups so get current resource group
name: az group list

- /home/{username}/.ssh/authorized_keys is fixed path for azure by default.

for ansible:
- ansible-playbook -i inventory docker_compose_playbook.yaml --ask-become-pass