# Deploying the contoso-creative-writer demo

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

## Authenticating

You need to authenticate using both the Azure CLI `az` and the Azure Developer CLI `azd`:

```
az login --use-device-code
```

Note that you may need to add the `--tenant` parameter to login to your specific BAMI tenant.

```
azd auth login --use-device-code
```

Note that you may need to add the `--tenant-id` (different than for `az`) parameter to login to your specific BAMI tenant.

## Provisioning

To provision the project with `azd` (Azure Developer CLI), at the root of the project, type the following:

```
azd up
```
