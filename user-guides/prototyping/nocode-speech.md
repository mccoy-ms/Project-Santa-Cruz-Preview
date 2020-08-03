# QuickStart: Creating a Voice Assistant with the Project Santa Cruz Devkit

In this quickstart, you make your own voice assistant using the Project Santa Cruz Development Kit (DevKit) and [Speech services](https://docs.microsoft.com/en-us/azure/cognitive-services/speech-service/overview).

## Prerequisites

* Hardware: 
  * Devkit with an Ear SOM connected.
  * Speaker connected to the Ear SOM (not included in the package).
* Configuration steps: 
  * [OOBE (out of box experience)](../getting_started/oobe.md) setup completed.
* Organization Azure tenant id enrolled in the Project Santa Cruz private preview.
* The following resource provides registered in the Azure subscription:
  * Cognitive Services
  * Storage
  * Web 

## Go to Azure Edge Devices in the Azure portal

The first step in creating a voice assistant is to navigate to the Project Santa Cruz in Azure portal.

1. Start your browser and go to the [Azure preview portal](https://preview.portal.azure.com/#home).
2. Sign into your Azure account. 
2.	Use the Search box at the top of the page, enter *Azure Edge Devices*.
3.	In the list that appears, choose *Azure Edge Devices*. Your browser displays the Azure Edge Devices Overview page.

Alternatively, you can navigate directly to the [Azure Edge Devices Overview page](https://preview.portal.azure.com/#blade/AzureEdgeDevices/AEDBlade/overview).


![Azure Edge Devices Portal](https://github.com/microsoft/Project-Santa-Cruz-Private-Preview/blob/main/user-guides/getting_started/getting_started_images/aed-portal-home-page.png)


## Create voice assistant using templates

You can build a voice assistant using available templates. The Hospitality template is available for the private preview. Healthcare is also scheduled to be released soon.

1.	Open **Demos & Tutorials** tab. 
2.	Click **Try out speech themes** under **Speech tutorials and demos**.
3.	Select IoT hub to which your device is connected from the **IoT hub** list.
4. Choose the device from the list.
5.	Select one of the speech templates.
6. Click the **I agree to terms & conditions for this project.** checkbox.
7.	Click **Create** button. The portal deploys the resource to the device.


![Azure Edge Devices Portal](https://github.com/microsoft/Project-Santa-Cruz-Private-Preview/blob/main/user-guides/getting_started/getting_started_images/aed-try-speech-themes.png)

8. Select the Azure subscription in the **Subscription** box.
9. Select the resource group to use from the **Resource group** list.
10. Enter name for the voice assistant. It will be used as a prefix to resource names.
11. Select the region to deploy resources to from the **Region** list.
12. Choose the pricing tier from the **Tier** list. (We recommend **Standard**).
13. Click the **Create** button. Resources for the voice assistant application will be deployed to your subscription. <br/>
   
**WARNING:** Do not close the pane until the portal finish deploying the resource. Closing the pane can result in unexpected behavior of voice assistant.
   
At this point, the portal displays the speech demo.

## Configure a keyword for your device

Next, you can add a keyword to your device so that you can activate it using voice. You can use prebuilt keywords and custom keywords created in [Speech Studio](https://speech.microsoft.com/).

1. Click on **change** link near **Custom keyword**.
2.	Select one of the available keywords. 

## Test out your voice assistant

Try any of the following commands to interact with your voice assistant. Always start with the keyword that you configured. For example - *Computer, turn on TV*.
* "Turn on lights."
* "Turn off lights."
* "Turn on TV."
* "Turn off TV."
* "Turn on AC."
* "Turn off AC."
* "Open blinds."
* "Close blinds."
* "Set temp to 75."

## Troubleshooting

### Azure Edge Devices is not available in the Azure portal

1.	Verify the Azure portal link. For the Project Santa Cruz private preview you must use the preview version of the Azure portal at  https://preview.portal.azure.com.
2. Make sure that the onboarding process for your organization is completed. 
  * Contact your lead PM or support team to find the latest status. 
  * Request onboarding to the Project Santa Cruz developer experience in Azure portal. 

### Voice assistant application cannot be created - resource deployment fails

1. Verify that the following resource providers are registered in the subscription:
  * Cognitive Services
  * Storage
  * Web
2. Register resource providers if they are not registered.

#### How to register resource providers

1. Select **Subscriptions** from the left navigation menu
2. Find the subscription that use for private preview and click on it to open detailed info
3. Select **Resource Providers** in the left navigation menu
4. Find each of the resource providers below and **Register** if they are not registered
  * Cognitive Services
  * Storage
  * Web

### Voice Assistant was created but does not respond to commands

1. Check led lights on the Ear SOM. 
  * 3 bright blue lights indicate that voice assistant is ready and waiting for the keyword
  * no lights when devkit is powered indicate that devkit completed initialization and needs to be configured
  * any combination of green lights indicates that Ear SOM did not complete initialization 

### Documentation links are not working

1. Make sure that the onboarding process for your organization is completed. 
  * Contact your lead PM or support team to find latest status. 
  * Request onboarding to the private preview documentation.

## Clean up resources

Follow these steps to clean up resources you deployed in this quickstart: 

1. From the Azure portal, select **Resource group** from the left menu.
2. Enter the resource group name (selected in step 9) in the **Filter by name** field.
3. Select the resource group from the list.
4. Open the resource group to view its resources.
5. Select 6 resources with the name starting with prefix selected in step 10.  
6. Click **Delete** action in the top menu.
7. Confirm delete operation.
8. Press **Delete** to delete resources.

**WARNING:** This will remove any custom keywords you created in Speech Studio and voice assistant will no longer function. 


## Next Steps

Now that you have created a voice assistant, you could try creating a [Vision project](https://github.com/microsoft/Project-Santa-Cruz-Private-Preview/blob/main/user-guides/prototyping/create-nocode-vision.md).