## Azure ARM template to deploy a Rails application

**Note**: Make sure you have Azure CLI installed in your machine

### Steps to follow

```sh
az login -u "email@domain.com" -p "your_password"
```

Set Azure subscription
```sh
az account set --subscription [SubscriptionID/SubscriptionName]
```

If you don't have a Resource Group created run the following

```sh
az group create --name myResourceGroup --location "Central US"
```

myResourceGroup - user defined (string) resource group name that you wish to create.

**TIP**: To get a list of valid locations `az account list-locations`

To create the deployment

```sh
templateFile="{provide-the-path-to-the-template-file}"
az deployment group create \
  --name blanktemplate \
  --resource-group myResourceGroup \
  --template-file $templateFile
```

blanktemplate - user defined (string)