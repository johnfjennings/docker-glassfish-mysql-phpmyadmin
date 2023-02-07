# Deploy to Azure

Source: https://learn.microsoft.com/en-us/azure/container-instances/tutorial-docker-compose


## Setup

Install Azure CLI - https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-windows?tabs=azure-cli



## Commands 


az login

az group create --name myResourceGroup --location northeurope

az acr create --resource-group myResourceGroup --name tusidm3 --sku Basic




az login

az acr login --name tusidm3


docker login azure

docker context create aci myacicontext

docker context use myacicontext

Need to upload mysql.sql file to a zure file share 

https://learn.microsoft.com/en-us/azure/container-instances/container-instances-volume-azure-files



# Create the storage account with the parameters & then create the file share
az storage account create --resource-group myResourceGroup --name mystorageaccountidm32023 --location northeurope --sku Standard_LRS


az storage share create --name idm3share --account-name mystorageaccountidm32023

Login to https://portal.azure.com/
Storage Accounts 
Locate idm3share
create db folder
crete war folder
upload mysql.sql to db folder
upload app.war to war folder





# After each reboot or session

az login

az acr login --name tusidm3


docker login azure
