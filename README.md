# Terraform 101

### What is Iac? 
Infrastructure as Code (IaC) automates the provisioning of infrastructure, enabling your organization to develop, deploy, and scale cloud applications with greater speed, less risk, and reduced cost. 

for more on Iac [click here](https://www.ibm.com/cloud/learn/infrastructure-as-code)

<br>
Before we see what is Terraform let's understand the difference between Configuration Management vs Infrastructure Orchestration

Ansible, Chef, Puppet are configuration management tools which means that they are primarily designed to install and manage software on existig servers.

Terraform, AWS CloudFormation, Azure Resource Manager are the infrastructure orchestration tools which basically means they can provision the servers and infrastructure by themselves.

I don't mean to say we cannot provision infra with configuration management tools, but the focus here is that some tools are going to be better fit for certain type of tasks.

### What is Terraform?
  
Terraform is a Infrastructure Orchestration tool developed by HashiCorp for **building, changing** and **versioning infrastructure** safely and efficiently. Terraform can manage existing and popular service providers as well as custom in-house solutions.

### Advantages to using Terraform

1. Suppoerts multiple platforms and has hundreds of provides
2. Easy to learn
3. Free and open source

## Les's get started

#### Installation

#### basic commands

#### Terraform statefile
All metadata are stored in statefile

#### Terraform Refresh
will fetch current status

#### Provider versioning

#### attributes and output 

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
