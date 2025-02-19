# DLR<a name="dlr-component"></a>

The DLR component \(`variant.DLR`\) contains a script that installs [Deep Learning Runtime](https://github.com/neo-ai/neo-ai-dlr) \(DLR\) and its dependencies in a virtual environment on your device\. The [DLR image classification](dlr-image-classification-component.md) and [DLR object detection](dlr-object-detection-component.md) components use this component as a dependency for installing DLR\. Component version 1\.6\.x installs DLR v1\.6\.0 and component version 1\.3\.x installs DLR v1\.3\.0\. 

To use a different runtime, you can use the recipe of this component as a template to [create a custom runtime component](ml-customization.md)\. 

## Versions<a name="dlr-component-versions"></a>

This component has the following versions:
+ 1\.6\.x
+ 1\.3\.x

## Requirements<a name="dlr-component-requirements"></a>

To deploy a component, you must meet the requirements for the component and its [dependencies](#dlr-component-dependencies)\. This component has the following requirements:<a name="ml-component-requirements"></a>
+ <a name="ml-req-glibc"></a>On Greengrass core devices running Amazon Linux 2 or Ubuntu 18\.04, [GNU C Library](https://www.gnu.org/software/libc/) \(glibc\) version 2\.27 or later installed on the device\.
+ On Armv7l devices, such as Raspberry Pi, dependencies for OpenCV Python installed on the device\. Run the following command to install the dependencies: 

  ```
  sudo apt-get install libopenjp2-7 libilmbase23 libopenexr-dev libavcodec-dev libavformat-dev libswscale-dev libv4l-dev libgtk-3-0 libwebp-dev
  ```

## Dependencies<a name="dlr-component-dependencies"></a>

When you deploy a component, AWS IoT Greengrass also deploys compatible versions of its dependencies\. You must meet the requirements for the component and all of its dependencies to successfully deploy the component\. This section lists the dependencies for the [released versions](#dlr-component-changelog) of this component and the semantic version constraints that define the component versions for each dependency\. You can also view the dependencies for each version of the component in the [AWS IoT Greengrass console](https://console.aws.amazon.com/greengrass)\. On the component details page, look for the **Dependencies** list\.

------
#### [ 1\.6\.x ]

The following table lists the dependencies for version 1\.6\.x of this component\.


| Dependency | Compatible versions | Dependency type | 
| --- | --- | --- | 
| [Greengrass nucleus](greengrass-nucleus-component.md) | >=2\.0\.0 <2\.2\.0 | Soft | 

------
#### [ 1\.3\.x ]

The following table lists the dependencies for version 1\.3\.x of this component\.


| Dependency | Compatible versions | Dependency type | 
| --- | --- | --- | 
| [Greengrass nucleus](greengrass-nucleus-component.md) | \~2\.0\.0 | Soft | 

------

For more information about component dependencies, see the [component recipe reference](component-recipe-reference.md#recipe-reference-component-dependencies)\.

## Configuration<a name="dlr-component-config"></a>

This component provides the following configuration parameters that you can customize when you deploy the component\.

`MLRootPath`  
<a name="ml-config-mlrootpath-desc"></a>\(Optional\) The path of the folder on the device where inference components read images and write inference results\. You can modify this value to any location on your device to which the user running this component has read/write access\.  
Default: `/greengrass/v2/work/variant.DLR/greengrass_ml`

## Usage<a name="dlr-component-usage"></a>

The DLR component sets up a virtual environment on your device that includes the OpenCV and NumPy libraries that are required for DLR\. 

**Note**  
The installer script in this component also installs the latest versions of additional system libraries that are required to configure the virtual environment and to run DLR on your device\. This might upgrade the existing system libraries on your device\. Make sure you review the following table for the list of libraries that this component installs for each supported operating system\.


| Operating system | Libraries installed on the device system | Libraries installed in the virtual environment | 
| --- | --- | --- | 
| Raspberry Pi OS | build\-essential, cmake, ca\-certificates, git | setuptools, wheel | 
| Amazon Linux 2 | mesa\-libGL | None | 
| Ubuntu | wget | None | 

When you deploy your inference component, this runtime component first verifies if your device already has DLR and its dependencies installed, and if not, then it installs them for you\. 

## Changelog<a name="dlr-component-changelog"></a>

The following table describes the changes in each version of the component\.


|  **Version**  |  **Changes**  | 
| --- | --- | 
|  1\.6\.1  |  <a name="changelog-dlr-1.6.1"></a>[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/greengrass/v2/developerguide/dlr-component.html)  | 
|  1\.3\.2  |  Initial version\. Installs DLR v1\.3\.0\.  | 