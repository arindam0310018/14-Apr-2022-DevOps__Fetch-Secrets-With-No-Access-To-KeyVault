# FETCH SECRETS WITH NO ACCESS TO KEY VAULT USING DEVOPS PIPELINES

Greetings my fellow Technology Advocates and Specialists.

| **USECASE INTRODUCTION:-** | 
| --------- |
Azure Key Vault is Protected by "**Access Policies**" and "**Firewall and Virtual Networks**". An Azure Cloud Engineer **Cannot Fetch Secrets** because of one of the condition or both (Depending upon the Scenerio).

| __PROBLEM STATEMENTS:-__ |
| --------- |

1. User Account of Cloud Engineer is not part of Key Vault Access Policy. Hence Secrets cannot be viewed from Azure Portal.
2. Key Vault is Protected by Organization's Public NAT IPs. Secrets cannot be viewed from Azure Portal unless Cloud Engineer is working from inside Organization Network.
3. Key Vault is Protected by Azure Virtual Network. Secrets cannot be viewed from Azure Portal unless inside Azure Virtual Network.   

| **QUESTION TIME:-** |
| --------- |
How will the Cloud Engineer Fetch Secrets ?


| __LIVE RECORDED SESSION:-__ |
| --------- |
| __LIVE DEMO__ was Recorded as part of my Presentation in __WELSH AZURE GROUP__ Forum/Platform |
| Duration of My Demo = __32 Mins 38 Secs__ |
| Start and End Time = __00:39:22 to 01:12:00__ |

| [![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/um_6WtIBSA8/0.jpg)](https://www.youtube.com/watch?v=um_6WtIBSA8) |
| --------- |


| __REQUIREMENTS:-__ |
| --------- |

1. Azure Key Vault
2. Three Sample Secrets in Azure Key Vault 
3. Azure Resource Manager Service Connection 
4. Azure DevOps Pipeline (YAML)

| **NOTE:-** |
| --------- |

The Service Principal (which is required to Create Service Connection) should at minimum have **GET** and **LIST** Access Policy Permissions in Azure Key Vault.

| __BELOW DISPLAYS THE SAMPLE SECRETS IN KEY VAULT:-__ |
| --------- |
| ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7uifu9nh2pcpgoevd5us.png) |

| __WHAT DOES THE PIPELINE DO:-__ |
| --------- |

| # | PIPELINE TASKS | 
| --------- | --------- |
| 1. | AZURE KEY VAULT TASKS |
| 2. | FETCH ALL SECRETS AND STORE IT IN A TEXT FILE | 
| 3. | COPY THE SECRETS TEXT FILE TO ARTIFACTS STAGING DIRECTORY |
| 4. | PUBLISH THE ARTIFACTS |
