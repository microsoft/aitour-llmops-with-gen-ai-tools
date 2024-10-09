# Deploying the contoso-creative-writer demo

## How-to video

This how-to complements the [Azure Deployment video recording](https://microsoft-my.sharepoint.com/:v:/p/cedricvidal/EW88E0K68f5Fgx-wdie6szQBeDYRiS7WSt-POKzwJ5TuOQ?e=GMhsNh).

## Opening the project

To open the project in GitHub Codespaces, simply follow these steps:

1. Navigate to the GitHub project page: https://github.com/azure-Samples/contoso-creative-writer
2. Ensure you are logged in to your GitHub account.
3. On the repository page, locate and click the "Open in GitHub Codespaces" button.
4. If you don't see the button, you may alternatively click the green "Code" button and select "Open with Codespaces" from the dropdown menu.
5. If necessary, create a new codespace by selecting "New codespace" from the list of available codespaces.
6. GitHub will set up a codespace environment, which may take a few moments. Once the environment is ready, an editor window will open, displaying the project files.
7. You can now start working on the project in the web-based Visual Studio Code editor provided by Codespaces.

For more detailed information, you can refer to the [GitHub Codespaces documentation](https://docs.github.com/en/codespaces).

## Prerequsities 

<mark>**Azure OpenAI GPT4 Quota** The AZD template deployment requires 10 new capacity in quota Tokens Per Minute (thousands) for GPT-4, which is bigger than the current available capacity.</mark>

### How to request additional azure openai quota
To request additional quota for Azure OpenAI, follow these steps:
- Navigate to [Azure OpenAI Studio](https://oai.azure.com): Go to the Azure OpenAI Studio in your Azure portal
- Click on "Quotas": In the Azure OpenAI Studio, click on the "Quotas" section
- Select the Model: Choose the model for which you want to increase the quota
- Request Quota: Click on the "Request quota" icon and fill out the necessary details to submit your request

Make sure you have the appropriate permissions, such as the Cognitive Services OpenAI Contributor role at the resource level and the Reader role at the subscription level.

<mark>**Note** If you cannot request additional capacity please edit the `ai.yaml` file located in `contoso-creative-writer/infra` within the Azure-Sample `https://github.com/Azure-Samples/contoso-creative-writer`
</mark>

## Authenticating

You need to authenticate using both the Azure CLI `az` and the Azure Developer CLI `azd`:

```
az login --use-device-code
```

<mark>**Note** that you may need to add the `--tenant` parameter to login to your specific BAMI tenant. Use the command `az login --tenant <TenantID> --use-device-code` </mark>

The `az` authentication is required because the `az` tool is used during post provisioning to build and deploy the `api` and the `web` ACA containers.

```
azd auth login --use-device-code
```

<mark>**Note** that you may need to add the `--tenant-id` (different than for `az`) parameter to login to your specific BAMI tenant. Use the command `azd auth login --tenant-id <TenantID> --use-device-code` </mark>

## Provisioning

To provision the project with `azd` (Azure Developer CLI), at the root of the project, type the following:

```
azd up
```

<mark>**Note** Please ensure you select Canada East as your resource group location</mark>

![](./azd-up.png)

<details>

<summary><b>Optional</b>: Follow deployment progress in Azure Portal</summary>

You can optionally click on the link under `You can view detailed progress in the Azure Portal:`, you'll be redirected to the following screen:

![](./deployment-progress.png)

Note that if you're deploying to a BAMI tenant and are already logged in to a different tenant in Azure Portal, you may get the following error:

![](./deploy-progress-portal-error.png)

If you do, you need to switch to the BAMI directory in the top right menu

![](./switch-tenant.png)

Then navigate to the resource group and click on the deployments link

![](./rg-click-deployments.png)

</details>


The provisioning takes some time and if everything works correctly, you should see the following:

![](./azd-up-success.png)

At the very bottom, it should display `SUCCESS` and if you scroll up a bit, you should see the URL at which the web ACA container has been deployed.

Click on the link, it should display the web app successfully deployed:

![](./web-app-success.png)

You can then start using the web app, click on the `Example` button then on the `Start Work` button then on the bug shaped debug button on the lower right of the screen, if everything works correctly, you should start to see some debug messages and eventually the final article.

![](./start-work.png)
