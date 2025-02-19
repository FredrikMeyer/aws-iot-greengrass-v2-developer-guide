# Lambda manager<a name="lambda-manager-component"></a>

The Lambda manager component \(`aws.greengrass.LambdaManager`\) manages work items and interprocess communication for AWS Lambda functions that run on the Greengrass core device\.

**Note**  <a name="lambda-component-dependency-note"></a>
When you deploy a Lambda function component to a core device, the deployment also includes this component\. For more information, see [Run AWS Lambda functions](run-lambda-functions.md)\.

**Topics**
+ [Versions](#lambda-manager-component-versions)
+ [Requirements](#lambda-manager-component-requirements)
+ [Dependencies](#lambda-manager-component-dependencies)
+ [Configuration](#lambda-manager-component-configuration)
+ [Changelog](#lambda-manager-component-changelog)

## Versions<a name="lambda-manager-component-versions"></a>

This component has the following versions:
+ 2\.1\.x
+ 2\.0\.x

## Requirements<a name="lambda-manager-component-requirements"></a>

To deploy a component, you must meet the requirements for the component and its [dependencies](#lambda-manager-component-dependencies)\. This component has the following requirements:
+ <a name="core-device-lambda-function-requirements"></a>Your core device must meet the requirements to run Lambda functions\. If you want the core device to run containerized Lambda functions, the device must meet the requirements to do so\. For more information, see [Requirements to run Lambda functions](setting-up.md#greengrass-v2-lambda-requirements)\.

## Dependencies<a name="lambda-manager-component-dependencies"></a>

When you deploy a component, AWS IoT Greengrass also deploys compatible versions of its dependencies\. You must meet the requirements for the component and all of its dependencies to successfully deploy the component\. This section lists the dependencies for the [released versions](#lambda-manager-component-changelog) of this component and the semantic version constraints that define the component versions for each dependency\. You can also view the dependencies for each version of the component in the [AWS IoT Greengrass console](https://console.aws.amazon.com/greengrass)\. On the component details page, look for the **Dependencies** list\.

------
#### [ 2\.1\.x ]

The following table lists the dependencies for version 2\.1\.x of this component\.


| Dependency | Compatible versions | Dependency type | 
| --- | --- | --- | 
| [Greengrass nucleus](greengrass-nucleus-component.md) |  >=2\.0\.0 <2\.2\.0  | Soft | 

------
#### [ 2\.0\.x ]

The following table lists the dependencies for version 2\.0\.x of this component\.


| Dependency | Compatible versions | Dependency type | 
| --- | --- | --- | 
| [Greengrass nucleus](greengrass-nucleus-component.md) |  >=2\.0\.3 <2\.1\.0  | Soft | 

------

For more information about component dependencies, see the [component recipe reference](component-recipe-reference.md#recipe-reference-component-dependencies)\.

## Configuration<a name="lambda-manager-component-configuration"></a>

This component provides the following configuration parameters that you can customize when you deploy the component\.

`getResultTimeoutInSecond`  
\(Optional\) The maximum amount of time in seconds that Lambda functions can run before they time out\.  
Default: `60`

## Changelog<a name="lambda-manager-component-changelog"></a>

The following table describes the changes in each version of the component\.


|  **Version**  |  **Changes**  | 
| --- | --- | 
|  2\.1\.0  |  Version updated for Greengrass nucleus version 2\.1\.0 release\.  | 
|  2\.0\.3  |  Initial version\.  | 