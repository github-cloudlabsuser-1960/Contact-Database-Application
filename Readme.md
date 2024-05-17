# Contact Database Application

This is a CRUD application built with ASP.NET. The application is deployed to Azure using an ARM template and a GitHub Actions workflow.

## Deployment

### ARM Template

The application is deployed using an Azure Resource Manager (ARM) template. The template is defined in the [deploy.json](deploy.json) file. This template sets up the necessary Azure resources, including the web app and hosting plan.

To deploy the application using the ARM template, you need to provide certain parameters. These parameters are defined in the [deploy.parameters.json](deploy.parameters.json) file.

### GitHub Actions Workflow

The application is automatically built and deployed to Azure using a GitHub Actions workflow. The workflow is defined in the [.github/workflows/master_csaghcadminwebapp.yml](.github/workflows/master_csaghcadminwebapp.yml) file.

The workflow is triggered on a push to the `master` branch. It sets up the build environment, restores NuGet packages, builds the application, and deploys it to Azure.

## Usage

Once the application is deployed, you can access it at `https://<webAppName>.azurewebsites.net`, where `<webAppName>` is the name of the web app you specified in the ARM template parameters.
