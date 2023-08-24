# cf-conditions
This repository stores CloudFormation templates created as examples for the article *Use Conditions to create reusable CloudFormation templates* posted on www.thenindiecoder.cloud.

## Prerequisites
You need to have the AWS CLI installed and properly configured.

## Conditions at the resource level
Template file: *cf-conditions-resource-level.yml*.

To create a cloudFormation stack from this template, one for each environment, run the following commands:
### create stack in the test environment
```shell
aws cloudformation create-stack --stack-name cf-conditions-resource-test --template-body file://cf-conditions-resource-level.yml --parameters ParameterKey=Environment,ParameterValue=test
```
### create stack in the prod environment
```shell
aws cloudformation create-stack --stack-name cf-conditions-resource-prod --template-body file://cf-conditions-resource-level.yml --parameters ParameterKey=Environment,ParameterValue=prod
```

## Conditions at the property level
Template file: *cf-conditions-property-level.yml*. 

To create a cloudFormation stack from this template, one for each environment, run the following commands:
### create stack in the test environment
```shell
aws cloudformation create-stack --stack-name cf-conditions-property-test --template-body file://cf-conditions-property-level.yml --parameters ParameterKey=Environment,ParameterValue=test
```
### create stack in the prod environment
```shell
aws cloudformation create-stack --stack-name cf-conditions-property-prod --template-body file://cf-conditions-property-level.yml --parameters ParameterKey=Environment,ParameterValue=prod
```
## Conditions on property level -  Including or Excluding a Property
Template file: *cf-conditions-property-level-noValue.yml*. 

To create a cloudFormation stack from this template, one for each environment, run the following commands:
### create stack in the test environment
```shell
aws cloudformation create-stack --stack-name cf-conditions-property-noValue-test --template-body file://cf-conditions-property-level-noValue.yml --parameters ParameterKey=Environment,ParameterValue=test
```
### create stack in the prod environment
```shell
aws cloudformation create-stack --stack-name cf-conditions-property-noValue-prod --template-body file://cf-conditions-property-level-noValue.yml --parameters ParameterKey=Environment,ParameterValue=prod
```

## Working with Nested Conditions
Template file: *cf-conditions-nested-conditions.yml*.

To create a cloudFormation stack from this template, one for each environment, run the following commands:
### create stack in the dev environment
```shell
aws cloudformation create-stack --stack-name cf-conditions-nested-conditions-dev --template-body file://cf-conditions-nested-conditions.yml --parameters ParameterKey=Environment,ParameterValue=dev
```
### create stack in the test environment
```shell
aws cloudformation create-stack --stack-name cf-conditions-nested-conditions-test --template-body file://cf-conditions-nested-conditions.yml --parameters ParameterKey=Environment,ParameterValue=test
```
### create stack in the prod environment
```shell
aws cloudformation create-stack --stack-name cf-conditions-nested-conditions-prod --template-body file://cf-conditions-nested-conditions.yml --parameters ParameterKey=Environment,ParameterValue=prod
```

## Clean up
🚨 **Stacks CLEAN UP: Remember to delete all your stacks to avoid unwanted costs** 🚨 

Run the following command for each of the stacks you created. Replace *myteststack* with the actual name of the stack you want to delete.
```shell
aws cloudformation delete-stack --stack-name myteststack
```
