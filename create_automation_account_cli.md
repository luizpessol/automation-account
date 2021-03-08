## Criar Automation Account
```
az automation account create \
    --automation-account-name "Nome_Automation_Account" \
    --location "East US" \
    --sku "Free" \
    --resource-group "Meu_Resoruce_Group"
 ```
 ## Criar Runbook
 ```
 az automation runbook create \
    --automation-account-name "Automation" \
    --resource-group "RG-Automation" \
    --name "StartVM" \
    --type "PowerShell" \
    --location "East US"
 ```
 ## Obs. Criar a Run as Account conforme vídeo.
