# Lambda runtimes<a name="lambda-runtimes-component"></a>

The Lambda runtimes component \(`aws.greengrass.LambdaRuntimes`\) provides the runtimes that Greengrass core devices use to run AWS Lambda functions\.

**Note**  <a name="lambda-component-dependency-note"></a>
When you deploy a Lambda function component to a core device, the deployment also includes this component\. For more information, see [Run AWS Lambda functions](run-lambda-functions.md)\.

**Topics**
+ [Versions](#lambda-runtimes-component-versions)
+ [Requirements](#lambda-runtimes-component-requirements)
+ [Dependencies](#lambda-runtimes-component-dependencies)
+ [Configuration](#lambda-runtimes-component-configuration)
+ [Changelog](#lambda-runtimes-component-changelog)

## Versions<a name="lambda-runtimes-component-versions"></a>

This component has the following versions:
+ 2\.0\.x

## Requirements<a name="lambda-runtimes-component-requirements"></a>

To deploy a component, you must meet the requirements for the component and its [dependencies](#lambda-runtimes-component-dependencies)\. This component has the following requirements:
+ <a name="core-device-lambda-function-requirements"></a>Your core device must meet the requirements to run Lambda functions\. If you want the core device to run containerized Lambda functions, the device must meet the requirements to do so\. For more information, see [Requirements to run Lambda functions](setting-up.md#greengrass-v2-lambda-requirements)\.

## Dependencies<a name="lambda-runtimes-component-dependencies"></a>

This component doesn't have any dependencies\.

## Configuration<a name="lambda-runtimes-component-configuration"></a>

This component doesn't have any configuration parameters\.

## Changelog<a name="lambda-runtimes-component-changelog"></a>

The following table describes the changes in each version of the component\.


|  **Version**  |  **Changes**  | 
| --- | --- | 
|  2\.0\.4  |  Version updated for Greengrass nucleus version 2\.1\.0 release\.  | 
|  2\.0\.3  |  Initial version\.  | 