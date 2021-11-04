# CI_CD_Terraform  <img src="https://user-images.githubusercontent.com/71599740/140194394-8d8b8fe8-a7d6-4b2b-938e-e5b00dea3bd4.png" width="130" height="100"/>  


## Requirements and Installations:
* [Node.js](https://nodejs.org/) 12.x or higher
* [Free Okta developer account](https://developer.okta.com/) for account registration, login
* Download Terraform from [terraform.io](https://www.terraform.io/downloads.html)
* Download and install [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)
* Type `az login` and login to Azure.

## Configuration:
* Use `azurerm` as a [provider](https://www.terraform.io/docs/language/providers/configuration.html).
* Create `.tfvars` file for your secret variables (for each environment - staging/production)

## Basic commands:
* `terraform` - make sure terraform CLI is installed
* `terraform init` - initialize terraform Azure modules
* `terraform fmt` - automatically updates configurations in the current directory for readability and consistency
* `terraform validate` - make sure your configuration is syntactically valid and internally consistent
* `terraform apply` or `terraform apply main.tfplan` - command to apply the infrastructure changes
* `terraform destroy` - remove the infrastructure

* now you will see in your azure portal your resource group with all the resources that your created.
* after you did it you can install the  Weight Tracker application in your VM'S.

## Emphasis:
* Create a vm controller that does not belong to the load balancer, which can communicate with all machines.
* Create 2 vnet one per environment - staging / production, and the connect vnet via peering [vnet-perring] (https://www.youtube.com/watch?v=wVWWthd8fzg)

![image](https://user-images.githubusercontent.com/71599740/140195050-03fbd26b-8c20-45b9-bb7e-61bc1c5f6d2c.png)

# Node.js Weight Tracker:

This sample application demonstrates the following technologies.

* [hapi](https://hapi.dev) - a wonderful Node.js application framework
* [PostgreSQL](https://www.postgresql.org/) - a popular relational database
* [Postgres](https://github.com/porsager/postgres) - a new PostgreSQL client for Node.js
* [Vue.js](https://vuejs.org/) - a popular front-end library
* [Bulma](https://bulma.io/) - a great CSS framework based on Flexbox
* [EJS](https://ejs.co/) - a great template library for server-side HTML templates


## Install and Configuration

1. Clone or download source files
1. Run `npm install` to install dependencies
1. If you don't already have PostgreSQL, set up using Docker
1. Create a [free Okta developer account](https://developer.okta.com/) and add a web application for this app
1. Copy `.env.sample` to `.env` and change the `OKTA_*` values to your application
1. Initialize the PostgreSQL database by running `npm run initdb`
1. Run `npm run dev` to start Node.js

The associated blog post goes into more detail on how to set up PostgreSQL with Docker and how to configure your Okta account.
