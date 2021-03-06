# Active Directory module for Sitecore XP Environment

Visualize:
[AD Module deployment](http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FSitecore%2Fsitecore-azure-quickstart-templates%2Fmaster%2FAD%201.3.0%2Fxp%2Fazuredeploy.json)

This template deploys Active Directory module into a Sitecore XP Environment. AD module files are deployed on CM role only.

Resources provisioned:

* Dlls and configuration files required by module on CM role. Additional configuration required.

## Parameters

| Parameter                                 | Description
--------------------------------------------|------------------------------------------------
| adMsDeployPackageUrl                      | An HTTP or blob storage URL of Active Directory module Web Deploy package.

## Deploying as part of Sitecore deployment

In order to configure Sitecore deployment parameters to include Active Directory module:

* Add the following snippet to the `modules` parameter:

```JSON
{
    "name": "active-directory",
    "templateLink": "https://raw.githubusercontent.com/Sitecore/sitecore-azure-quickstart-templates/master/ad%201.3.0/xp/azuredeploy.json",
    "parameters": {
        "adMsDeployPackageUrl" : "<URL of the WDP file *.scwdp.zip>"
    }
}
```
