# TensorFlow Lite object detection model store<a name="tensorflow-lite-object-detection-model-store-component"></a>

The TensorFlow Lite object detection model store \(`aws.greengrass.TensorFlowLiteObjectDetection`\) is a machine learning model component that contains a pre\-trained Single Shot Detection \(SSD\) MobileNet model as a Greengrass artifact\. The sample model used in this component is fetched from the [TensorFlow Hub](https://tfhub.dev/) and implemented using [TensorFlow Lite](https://www.tensorflow.org/lite)\.

The [TensorFlow Lite object detection](tensorflow-lite-object-detection-component.md) inference component uses this component as a dependency for the model source\. To use a custom\-trained TensorFlow Lite model, [create a custom version](ml-customization.md#override-public-model-store) of this model component, and include your custom model as a component artifact\. You can use the recipe of this component as a template to create custom model components\. 

## <a name="tensorflow-lite-object-detection-model-store-component-versions"></a>

This component has the following versions:
+ 2\.1\.x

## Requirements<a name="tensorflow-lite-object-detection-model-store-component-requirements"></a>

To deploy a component, you must meet the requirements for the component and its [dependencies](#tensorflow-lite-object-detection-model-store-component-dependencies)\. This component has the following requirements:<a name="ml-component-requirements"></a>
+ <a name="ml-req-glibc"></a>On Greengrass core devices running Amazon Linux 2 or Ubuntu 18\.04, [GNU C Library](https://www.gnu.org/software/libc/) \(glibc\) version 2\.27 or later installed on the device\.
+ On Armv7l devices, such as Raspberry Pi, dependencies for OpenCV Python installed on the device\. Run the following command to install the dependencies: 

  ```
  sudo apt-get install libopenjp2-7 libilmbase23 libopenexr-dev libavcodec-dev libavformat-dev libswscale-dev libv4l-dev libgtk-3-0 libwebp-dev
  ```

## Dependencies<a name="tensorflow-lite-object-detection-model-store-component-dependencies"></a>

When you deploy a component, AWS IoT Greengrass also deploys compatible versions of its dependencies\. You must meet the requirements for the component and all of its dependencies to successfully deploy the component\. This section lists the dependencies for the [released versions](#tensorflow-lite-object-detection-model-store-component-changelog) of this component and the semantic version constraints that define the component versions for each dependency\. You can also view the dependencies for each version of the component in the [AWS IoT Greengrass console](https://console.aws.amazon.com/greengrass)\. On the component details page, look for the **Dependencies** list\.

The following table lists the dependencies for version 2\.1\.x of this component\.


| Dependency | Compatible versions | Dependency type | 
| --- | --- | --- | 
| [Greengrass nucleus](greengrass-nucleus-component.md) | >=2\.0\.0 <2\.2\.0 | Soft | 

## Changelog<a name="tensorflow-lite-object-detection-model-store-component-changelog"></a>

The following table describes the changes in each version of the component\.


|  Version  |  Changes  | 
| --- | --- | 
|  2\.1\.0  |  Initial version\.  | 