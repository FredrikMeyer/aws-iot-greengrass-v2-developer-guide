# Uninstall the AWS IoT Greengrass Core software<a name="uninstall-greengrass-core-v2"></a>

You can uninstall the AWS IoT Greengrass Core software to remove it from a device that you don't want to use as a Greengrass core device\. You might also do this to clean up an installation that fails\.

**To uninstall the AWS IoT Greengrass Core software**

1. If you run the software as a system service, you must stop and disable the service\. Run the following command\.

   ```
   sudo systemctl stop greengrass.service && sudo systemctl disable greengrass.service
   ```

1. Remove the root folder from the device\. Replace */greengrass/v2* with the path to the root folder\.

   ```
   sudo rm -rf /greengrass/v2
   ```