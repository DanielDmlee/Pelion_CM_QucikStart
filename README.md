# Pelion_CM_QucikStart
This guide provides a quick introduction to the Connectivity Management platform based on Mbed OS.


## 1. Prpare SIM & Activiation
## 1.1 [Ordering Stock](https://help.iot-x.com/quickstart/ordering-stock)
After you've signed in to the Pelion Connnectivity Management, one of the first things you may want to do is order stock for your inventory. Depending on the tariff agreements you've signed up for, you can use Connectivity Management to order:
* SIM cards.
* eSIM profiles.
* Satellite devices.
* Any combination of the above.
  ```
  ** Tip

  Please contact your Account Manager if you would like to set up new tariff agreements.
  ```
## 1.2 [Subscriber Activations](https://help.iot-x.com/userguide/subscriber-activations)
When your subscribers are ready to go live, you can perform activations using Connectivity Management.
Activations can be performed using the platform's Inventory or Activate section 

The following screenshot displays the Activate Overview Page and highlights the key actions that can be conducted in this section.
![ActivationPage](https://help.iot-x.com/download/attachments/3899399/Annotated%20Blurred%20Activate%20Home%20Page.png?version=8&modificationDate=1547568643000&api=v2)

  1. Click on the Activate icon to access this page.
  2. This section allows you to perform activations by uploading a CSV file to the platform.
  3. This section allows you to perform activations by pasting subscriber information into the text box.
  4. This section displays the subscribers that have recently been added to your inventory.
     Click on any of the subscribers in this panel to add it to the list of activations.

## 2. Prpare target board
## 2.1 Choose a board and connectivity method
Select your Cellular board for 3G
  1. [Seed Wio 3G](https://os.mbed.com/platforms/Seeed-Wio-3G/)
  2. Not ready yet : [MultiTec Dragonfly](https://os.mbed.com/platforms/MTS-Dragonfly/)
  3. [DISCO0-L495AG + UG96](https://os.mbed.com/platforms/ST-Discovery-L496AG/)
  * Board descripton [The P-L496G-CELL01 STM32 decovery pack](https://www.st.com/en/evaluation-tools/p-l496g-cell01.html)

Select your Cellular board for CatM1 and NB-IoT
  1. Not ready yet : [NuMaker-IoT-M263A](https://os.mbed.com/platforms/NUMAKER-IOT-M263A/)
  
## 1.2 Add an out-of-the box example program to our online IDE.
### 1.2.1 Importing the example application to the Mbed Online Compiler
You’re going to use the Mbed Online Compiler to configure and build the example application. The Online Compiler needs to access your Mbed account and to know which device you're using.
![ApplicationToOnlineIDE](https://os.mbed.com/static/img/guides/connect_device_to_pelion/Mbed-Cloud-Connect-Flow-Step1.190c935101a0.svg)
  1. [Import the Seeed Wio 3G](https://os.mbed.com/platforms/Seeed-Wio-3G/add/) into the Online Compiler.
  2. [Import the example application](https://ide.mbed.com/compiler/#import:/teams/Seeed/code/mbed-os-example-wio-cellular/) for your device into the Online Compiler.
  3. The Online Compiler Import Program dialog is displayed. Ensure Update all libraries to the latest revision is not selected and click Import.
  ![latestRevision](https://os.mbed.com/static/img/guides/connect_device_to_pelion/compiler-import-dialog.5da7bac0e16e.png)

### 1.2.2 Configure for cellular application
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
 4. Drag and drop the compiled binary to the device. Your micro SD card is formatted, and the application is installed.
 ![DragNdrop](https://os.mbed.com/static/img/guides/connect_device_to_pelion/compiler-mcc-example-drag-n-drop.65a6ad5629fa.png)
 5. Ensure your device is connected to power and press the reset button.



Visit the Pelion Device Management portal to see IoT data from your board.
You need to have the ID of Pelion CM(Connectivity Management)

- Check service country and categories
TBD


