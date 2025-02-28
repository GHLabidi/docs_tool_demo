
# DevOps - Bicep 🌍

## 🔎 What is Bicep?
**Bicep** is an Infrastructure-as-Code (IaC) language for Azure, simplifying ARM templates.

✅ **Advantages of Bicep**:
- **Declarative syntax** like Terraform.
- **No JSON clutter**, easy to read.
- **Supports all Azure resources**.

Example **Bicep vs ARM Template**:
```bicep
resource myStorage 'Microsoft.Storage/storageAccounts@2021-09-01' = {
  name: 'mystorageaccount'
  location: 'eastus'
  kind: 'StorageV2'
  sku: { name: 'Standard_LRS' }
}
```
This is simpler than an equivalent ARM template.

---

## 🚀 Deploying an Azure Web App using Bicep
### 1️⃣ **Create a Web App Bicep File (`webapp.bicep`)**
```bicep
resource webApp 'Microsoft.Web/sites@2021-02-01' = {
  name: 'myWebApp'
  location: 'eastus'
  properties: {
    serverFarmId: 'myAppServicePlan'
  }
}
```

### 2️⃣ **Deploy Using Azure CLI**
```sh
az deployment group create --resource-group MyResourceGroup --template-file webapp.bicep
```
This command deploys the **web app** in Azure! 🌐🎉
