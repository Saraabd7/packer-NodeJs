### NodeJs-Packer 💻

## Packer
• Packer is used to creating immutable images of our machines. packer has been used to create an AMI in AWS. The configuration of this specified in the packer.json.


• To install packer run command ``` brew install packer ``` then type ``` packer verify ``` to verify the installation.

• After Packer is installed, create first template, which tells Packer what platforms to build images for and how you want to build them. create a file ``` touch packer-mongo.json ```. Export  AWS credentials as the AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY environment variables.

• Give an name to AMI by editing packer.json file:

```
 "ami_name": "<NAME>-{{timestamp}}"

```
## Creating an image (Building)
• To create an image for MongoCookbookStarterCode in the command line type:


To check that everything correct go into the terminal and run the command:
```
packer validate packer.json

```

To build an AMI go into the terminal and run the command  ``` packer build packer-nodejs.json ``` will run Packer and build out an AMI image according to the "packer-nodejs.json" template. The AMI will be available in AWS account, which can be used in CloudFormation templates so can have an environment to work on.

Configurable values are located in variables.json which in this project called (packer-nodejs.json) Edit on these values as need to customise the template.


 - Launch an instance using the AMI created, name of AMI is specified in the packer-nodejs.json file.

 - To delete the AMI,  must manually delete it using the AWS console.


## Installation
Other than the prerequisites, there is nothing to install. The script will install into the region's AMI registry.


## Berksfile

• Berksfile contains the chef supermarket and the metadata and is used to manage the dependencies of the cookbook and a berks-cookbooks berks vendor

```
berks vendor
```

## Pre-requisites.

1. Git

2. Packer

3. Chef

4. oh my zssh
