# Pelion Connectivity Management Qucik Start
This guide provides a quick introduction to the Pelion CM(Connectivity Management) platform based on Mbed OS.

## 1. Prpare SIM & Activiation
This section requires a plastic SIM card. Currently, if you would like to set up new tariff agreements, please contact to [here](https://www.arm.com/products/iot/pelion-iot-platform/connectivity-management/talk-with-an-expert)

### 1.1 Ordering Stock
After you've signed in to the Connectivtivity Management, one of the first things you may want to do is order stock for your inventory. Depending on the tariff agreements you've signed up for, you can use Connectivtivity Management to order:
* SIM cards.
* eSIM profiles.
* Satellite devices.
> Here is [how to place an order](https://help.iot-x.com/quickstart/ordering-stock#OrderingStock-HowtoPlaceanOrder)

### 1.2 Subscriber Activations
When your subscribers are ready to go live, you can perform activations using Connectivtivity Management.
Activations can be performed using the platform's Inventory or Activate section. Please see [here](https://help.iot-x.com/userguide/subscriber-activations)

The following screenshot displays the Activate Overview Page and highlights the key actions that can be conducted in this section.
![ActivationPage](https://help.iot-x.com/download/attachments/3899399/Annotated%20Blurred%20Activate%20Home%20Page.png?version=8&modificationDate=1547568643000&api=v2)

  1. Click on the Activate icon to access this page.
  2. This section allows you to perform activations by uploading a CSV file to the platform.
  3. This section allows you to perform activations by pasting subscriber information into the text box.
  4. This section displays the subscribers that have recently been added to your inventory.
     Click on any of the subscribers in this panel to add it to the list of activations.

## 2. Prpare Target Board
You can find board that include cellular modem [here](https://os.mbed.com/platforms/?q=&Communication=Cellular).

### 2.1 Choose a board and connectivity method
There are various communication standards, such as WCDMA, CDMA2000, HSPA+, LTE, and so on for each country.  It is not necessary to deeply understand each communication protocol, but you should know if the cellular modem's communication method is appropriate for your country. This section uses development boards that use 3G communication, which is available in most countries. Cat M1 and NB-IoT are currently available in the UK only, with roaming services will be added for other countries.

Select cellular board for 3G telecommunications.

  1. [Seed Wio 3G](https://os.mbed.com/platforms/Seeed-Wio-3G/)
  2. [DISCO0-L495AG + UG96](https://os.mbed.com/platforms/ST-Discovery-L496AG/); [The P-L496G-CELL01 STM32 decovery pack](https://www.st.com/en/evaluation-tools/p-l496g-cell01.html)

### 2.2 Importing the example application to the Mbed Online Compiler
You’re going to use the Mbed Online Compiler to configure and build the example application. The Online Compiler needs to access your Mbed account and to know which device you're using.
![ApplicationToOnlineIDE](https://os.mbed.com/static/img/guides/connect_device_to_pelion/Mbed-Cloud-Connect-Flow-Step1.190c935101a0.svg)

  1. You need to tell the Online Compiler which device you will be targeting. Click the button below to import the Seeed Wio 3G into the Online Compiler.
  
  [Add Seeed Wio 3G to the Online Compiler](https://os.mbed.com/platforms/Seeed-Wio-3G/add/) 

  2. Click the button below to import the example application for your device into the Online Compiler.
      
  [Import Cellular example into the Online Compiler](https://ide.mbed.com/compiler/#import:/teams/Seeed/code/mbed-os-example-wio-cellular/)
      
  3. The Online Compiler Import Program dialog is displayed. Ensure Update all libraries to the latest revision is not selected and click Import.
  ![latestRevision](https://os.mbed.com/static/img/guides/connect_device_to_pelion/compiler-import-dialog.5da7bac0e16e.png)

## 3. Putting the application on your device
APN, Username and Password settings are required to use Pelion CM.

 1. Open ```mbed_app.json``` and put APN, Username and Password as below
```
     "nsapi.default-cellular-apn": "\"stream.co.uk\"",
     "nsapi.default-cellular-username": "\"streamip\"",
     "nsapi.default-cellular-password": "\"streamip\""
```

 2. Make sure your device is selected as a compilation target in the top right-hand corner. If your device is not selected, click Select a platform.
 ![SelectedImage](https://os.mbed.com/static/img/guides/connect_device_to_pelion/compiler-mcc-example-target.ae212e114295.png)
 3. To create the application binary, click Compile.
 ![Application](https://os.mbed.com/static/img/guides/connect_device_to_pelion/compiler-mcc-example-compile.4a57861ba3b2.png)
 4. Drag and drop the compiled binary to the device.
 ![DragNdrop](https://os.mbed.com/static/img/guides/connect_device_to_pelion/compiler-mcc-example-drag-n-drop.65a6ad5629fa.png)
 5. Ensure your device is connected to power and press the reset button.

## 4. Seeing the device resources in Connectivtivity Management Portal
TBD


