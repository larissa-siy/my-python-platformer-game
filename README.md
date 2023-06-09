# my-python-platformer-game

**Project Outline: **

_Project: Deploying a Python Web Application on Azure using Infrastructure as Code (IaC) and CI/CD pipelines_

Overview:

In this project, I will deploy a Python web application on Azure using Infrastructure as Code principles, leveraging Azure DevOps for CI/CD pipelines. We will use Terraform for infrastructure provisioning, YAML for configuration, and Azure services for hosting the web application.

Project Steps:

**Set up Azure resources:
-  After uploading the file I created a resource group on Azure to host my new project. I created a Linux Web App using a Python 3.7 Runtime Stack, within the resource group, to host my Python App.
- If I was to do this project again, I would use Terraform to define the infrastructure components. Terraform scripts in a combination of Bash and PowerShell to provision the resources would be a time saving way to provision the infrastructure components. However, I imported the infrastructure components using

    ``` 
  resource azurerm_resource_group my-python-platformer-game_group {
  name = "my-python-platformer-game_group"
  }
  
  terraform import "azurerm_resource_group.my-python-platformer-game_group" "/subscriptions/772f1a68-850d-4639-92cc-278f98532405/resourceGroups/my-python-platformer-game_group"
  
  terraform init

****Configure the Python web application:
****Develop a Python web application using a web framework like Flask or Django.

I coded a Platform game animated in Python using Visual Studio Code. I used for loops and functions to create a pixel-perfect collision animated game with sprite sheet and masks. 

In the game I:
- generated a background using the functions def get_background and def draw
- created a player using the class function with def __init__ and def move to be able to move the player left or right
- added gravity using loops to imitate the act of falling / jumping
- moved the player with animations by loading and splitting sprite sheets
- adding terrain that the player is able to collide with
- added a scrolling background using the offset function
- published the local repository onto GitHub and used Git for version control between the local and GitHub repositories.

****Use YAML or JSON files to define the application configurations, such as database connection strings and environment variables.
Implement CI/CD pipelines:

- I linked my GitHub repository to my Azure DevOps account and pushed the GitHub repo into the Azure DevOps repo.
- I create an Azure DevOps pipeline using YAML to automate the build and deployment processes.
- Defined stages for building the application, running tests, and deploying to Azure resources.
- I utilised Azure DevOps tasks to execute commands/scripts, e.g. running Python tests and deploying infrastructure using Terraform.

****Enabling security and networking

- I configured the authentication/authorization for the web application and secured the database.
- I configure networking settings. I used a virtual network and network security groups, to control traffic flow and enhance security.


****Continuous Deployment:

- I triggered the CI/CD pipeline on each commit to the main branch or on specific events (e.g., pull requests).
- I kept the trigger as "main" so if any changes were made in the repos, it would continuously integrate the pipeline.
- I validated and deploy the updated application and infrastructure automatically.


Skills demonstrated: Programming in Python, using VS Code and Git (+GitHub), Azure DevOps, Pipelines, CI/CD, Azure Web App Deployment, Security, Scripting in Bash and PowerShell.
