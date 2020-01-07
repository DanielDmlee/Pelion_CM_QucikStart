# Pelion Connectivity Management Quick Start
This guide provides a quick introduction to the Pelion CM(Connectivity Management) platform based on Mbed OS.

# 1. Prepare the SIM card and Activiation
In this quick start guide, requires a plastic SIM card. Currently, if you would like to set up new tariff agreements, please contact to [here](https://www.arm.com/products/iot/pelion-iot-platform/connectivity-management/talk-with-an-expert).


## 1.1 Prepare the SIM card 
There is two designs, and both are can use Connectivtivity Management.

<center> 
<img src="./Pictures/PelionCM_SimCard.png" width="40%"></img>
    or    
<img src="./Pictures/PelionCM_SimCard2.png" width="40%"></img>
</center> 

## 1.2 Activations 
After you've signed in to the Connectivtivity Management, one of the first things you may want to do is activation your plastic SIM cards. Activations can be performed using the platform's Inventory or Activate section.

> More detailed description of each item and each steps, can be found [here](https://help.iot-x.com/userguide/subscriber-activations).

# 2. Importing the example application to the Mbed Online Compiler
You’re going to use the Mbed Online Compiler to configure and build the example application. The Online Compiler needs to access your Mbed account and to know which device you're using.

<center> 
<img src="https://os.mbed.com/static/img/guides/connect_device_to_pelion/Mbed-Cloud-Connect-Flow-Step1.190c935101a0.svg"></img>
</center> 
ß
## 2.1 Choose a board for each connectivity method
There are various communication standards, such as WCDMA, CDMA2000, HSPA+, LTE, and so on for each country, and it depends on policy of each country.

It is not necessary to deeply understand each communication protocol, but you should know if the cellular modem's communication method is appropriate for your country. 

This section uses development boards that use 3G communication, which is available in most countries. Cat M1 and NB-IoT are currently available in the United Kingdom only, with roaming services will be added for other countries soon.

You can find board that include cellular modem [here](https://os.mbed.com/platforms/?q=&Communication=Cellular). In this session, it going to be use a board that can use 3G communication.

  1. [Seed Wio 3G](https://os.mbed.com/platforms/Seeed-Wio-3G/)
  2. [DISCO0-L495AG + UG96](https://os.mbed.com/platforms/ST-Discovery-L496AG/); [The P-L496G-CELL01 STM32 decovery pack](https://www.st.com/en/evaluation-tools/p-l496g-cell01.html)

## 2.2 Importing target board and the example code
  a. You need to tell the Online Compiler which device you will be targeting. Click the button below to import the `Seeed Wio 3G` into the Online Compiler.

> [Add Seeed Wio 3G to the Online Compiler](https://os.mbed.com/platforms/Seeed-Wio-3G/add/) 

  b. Click the button below to import the example application for your device into the Online Compiler.
      
> [Import Cellular example into the Online Compiler](https://ide.mbed.com/compiler#import:https://github.com/ARMmbed/mbed-os-example-cellular)
      
  c. The Online Compiler Import Program dialog is displayed. Ensure Update all libraries to the latest revision is not selected and click Import.    

<center> 
<img src="./Pictures/compiler-import-dialog.png" width="60%" ></img>
</center>  

# 3. Putting the application on your device
In this section, you can compile and binary download onto target board. If you are unfamiliar with how to compile and load code, [Mbed OS Quickstart tutorial](https://os.mbed.com/docs/mbed-os/v5.15/quick-start/index.html) would be help to you.

You are now ready to build the application and flash it to your device over USB.

<center> 
<img src="./Pictures/AppDownToDevBoard.png" ></img>
</center>  

 a. Make sure your device is selected as a compilation target in the top right-hand corner. If your device is not selected, click Select a platform.

![SelectBoard](./Pictures/SelectBoard.png)
  
 b. APN, Username and Password settings are required to use Pelion CM.
 Open `mbed_app.json` and put APN, Username and Password as below

```
            "nsapi.default-cellular-apn": "\"stream.co.uk\"",
            "nsapi.default-cellular-username": "\"streamip\"",
            "nsapi.default-cellular-password": "\"streamip\""
```

 c. To create the application binary, click Compile.

![Compile](./Pictures/Compile.png)

 d. The binary is downloaded to your browser's default download location. Drag and drop the compiled binary to the device.

<center> 
<img src="./Pictures/Wio3G_board.png" width="40%" ></img>
<img src="./Pictures/BinaryCopy.gif"></img>
</center> 

 e. Ensure your device is connected to power and press the reset button.
 
  Once your code is up and running, you should see output to the following on your serial terminal such as [CoolTerm](http://freeware.the-meiers.org/), [TeraTerm](https://osdn.net/projects/ttssh2/releases/) and [putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/).

```
    mbed-os-example-cellular
    Establishing connection ......

    Connection Established.
    TCP: connected with echo.mbedcloudtesting.com server
    TCP: Sent 4 Bytes to echo.mbedcloudtesting.com
    Received from echo server 4 Bytes


    Success. Exiting
```

## 4. Seeing the device resources in Connectivtivity Management Portal
<center> 
<img src="./Pictures/PelionCM-Flow.png"></img>
</center> 

The following screenshot displays the Active page.
You access this page by navigating to `Devices > Active`.

Subscribers that can connect to the network and are included as part of the account's invoice.

<center> 
<img src="./Pictures/PelionCM_Devices_Active.png"></img>
</center> 

You are now connected and can use Pelion Connectivity Management!

You have:

* Prepare the SIM card and Activiation.
* Imported the example application for your device to the Online Compiler.
* Put the application onto your device.
* Checked the device resources in the Connectiviy Management Portal.
