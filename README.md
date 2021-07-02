# Terraform 101

### **What is Iac?** 
Infrastructure as Code (IaC) automates the provisioning of infrastructure, enabling your organization to develop, deploy, and scale cloud applications with greater speed, less risk, and reduced cost. 

for more on Iac [click here](https://www.ibm.com/cloud/learn/infrastructure-as-code)

<br>
Before we see what is Terraform let's understand the difference between Configuration Management vs Infrastructure Orchestration

Ansible, Chef, Puppet are configuration management tools which means that they are primarily designed to install and manage software on existing servers.

Terraform, AWS CloudFormation, Azure Resource Manager are the infrastructure orchestration tools which basically means they can provision the servers and infrastructure by themselves.

I don't mean to say we cannot provision infra with configuration management tools, but the focus here is that some tools are going to be better fit for certain type of tasks.

### **What is Terraform?**
  
Terraform is a Infrastructure Orchestration tool developed by HashiCorp for **building, changing** and **versioning infrastructure** safely and efficiently. Terraform can manage existing and popular service providers as well as custom in-house solutions.

### Advantages to using Terraform

1. Supports multiple platforms and has hundreds of provides
2. Easy to learn
3. Free and open source

## Enough of intro let's get started

### **Installation**
To use Terraform you will need to install it. HashiCorp distributes Terraform as a [binary package](https://www.terraform.io/downloads.html). You can also install Terraform using popular package managers.

**Homebrew on MacOS**

```
brew tap hashicorp/tap

brew install hashicorp/tap/terraform
```

**Chocolatey on Windows**

```
choco install terraform
```

For Linux and manual installation [click here](https://learn.hashicorp.com/tutorials/terraform/install-cli)


### **basic commands**
These are the four main commands you will be using with Terraform the most. 

![LifeCycle](./images/lifecycle.png "Terraform lifecycle")

`terraform init` - The terraform init command is used to initialize a working directory containing Terraform configuration files. This is the first command that should be run after writing a new Terraform configuration

`terraform plan` - Terraform plan is used to create an execution plan to reach a desired state of the infrastructure. Changes in the configuration files are done in order to achieve the desired state.

`terraform apply` - Terraform apply then makes the changes in the infrastructure as defined in the plan, and the infrastructure comes to the desired state.

`terraform destroy` - Terraform destroy is used to delete all the old infrastructure resources, which are marked tainted after the apply phase.


*Yes there are other commands too.*

### **Terraform statefile**
Terraform stores the state of the infrastructure that is being created from the TF files.

This state allows terraform to map real-world resources to your existing configuration.
All metadata are stored in statefile

<!-- ### Terraform Refresh
will fetch current status -->

### **Provider versioning**
To understand provider versioning first lets understand provider and its architecture 

![Provider Architecture](images/provider_arch.png "Provider Architecture")

Terraform Provider is responsible to authenticate/interact with the service provider (in the above example Digital ocean), TF provider acts as a middle man between TF and Service provider.

whenever `terraform init` command is executed terraform will download appropriate provide plugin , these provider plugin are different from terraform configuration and they have different set of version.

*example: version 3.0 and above will be used*
```sh
provider "aws" {
    region = "us-east-1"
    version = "~> 3.0" 
}
```
### Attributes and Output 

#### variables
- Environment variable `TF_VAR_<name>`
- variable file
- command line variable

#### variable type

#### count parameter

#### conditional expression

#### local value

#### functions

#### data source

#### format

#### Dynamic block

#### graph

#### provisioners

#### module

#### workspace

#### remote backend

#### TF import
