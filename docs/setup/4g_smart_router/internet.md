# INTERNET

There are total 4 types of connection method that you can use to access the Internet: **Cable**, **Repeater**, **3G/4G Modem** and **Tethering**.

![](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/4ways.jpg)

Click `INTERNET` to create an Internet connection.

![internet](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/internet.jpg)



---

##1) Cable

Connect the router to the modem or main router via Ethernet cable to access the Internet. 

Before plugging the Ethernet cable into the WAN port of the router, you can click `Use as LAN` to set the WAN port as a LAN port. That is useful when you are using the router as a [repeater](internet#2-repeater). As a result, you can have one more LAN port.

![cable](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/cable.jpg)



Plug the Ethernet cable into the WAN port of the router. The information of your connection will be shown on the Cable section. DHCP is the default protocol. You can click `Modify` to change the protocol.

![cable](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/dhcp_page.jpg)



### DHCP

DHCP is the default and most common protocol. It doesn't require any manual configuration.

![dhcp](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/dhcp.jpg)



### Static

Static is required if your Internet Service Provider (ISP) has provided a fixed IP address for you or you want to configure the network information such as IP address, Gateway, Netmask manually.

The current settings will be automatically filled once you choose Static. Change it according to your needs and then click `Apply`.

![static](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/static.jpg)



### PPPoE

PPPoE is required by many Internet Service Providers (ISP). Generally, your ISP will give you a modem and provide you a username & password that you needed when you are creating the Internet connection.

Under PPPoE protocol, enter your username and password, then click `Apply`.

![PPPoE](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/pppoe_page.jpg)



---

##2) Repeater

Using Repeater means connecting the router to another existing wireless network, e.g. when you are using free Wi-Fi in a hotel or cafe.

It works in WISP (Wireless Internet Service Provider) mode by default, which means that the router will create its own subnet and act as a firewall to protect you from the public network.

In Repeater section, click `Scan` to search for the available wireless networks nearby.

![scan wifi](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/wisp1.jpg)



Choose a SSID from the drop-down list and enter its password. You can also enable the **Remember** button to save the current chose wireless network. Finally, click `Join`.

![connect wifi](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/wisp2.jpg)



---

##3) 3G/4G Modem

GL-MiFi has different options of 3G/4G module which you can choose before purchase. If your GL-MiFi has a built-in modem, the 3G/4G modem section will be activated automatically.

You can also connect to the Internet using a USB 3G/4G modem. Insert your SIM card into the USB modem. Plug the USB modem into the USB port of the router. Once it has been detected, you will be able to find several additional options in the drop-down list of **Device**.

Be aware that some USB modems work in host-less mode, which have to be configured through [Tethering](internet.md#4-tethering) but not 3G/4G modem.

In General, you can set up your 3G/4G modem by the three basic parameters below. Click `Apply` to connect.

- **Device**: For built-in modem, please choose **/dev/cdc-wdm0 (qmi)** or **/dev/ttyUSB3**. For USB modem, please try the additional options one by one.
- **Service Type**: indicate the service of your SIM card.
- **APN**: Confirm with your SIM card carrier.

![modem](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/modem1.jpg)

Advanced Settings:

- **Dial Number**: Generally, it is a default value and you don't need to set it manually. However, if you have this info, please input it.
- **Pincode, Username and Password:** Generally, these are not necessary for an unlocked SIM card. However, if you have a locked SIM card, please consult your service provider.

![modem](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/modem4.jpg)



It is connected when the IP address of your SIM card shows up.

![modem connect](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/modem2.jpg)

![modem connected](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/modem3.jpg)



### Compatible Modems

Here is a list of supported modems that we had tested before. 

| Model                                  | 3G/4G | Tested | Tested by       | Comments* |
| -------------------------------------- | ----- | ------ | --------------- | --------- |
| Quectel EC20-E, EC20-A, EC20-C         | 4G    | Yes    | GL.iNet         |           |
| Quectel EC25-E, EC25-A, EC25-V, EC25-C | 4G    | Yes    | GL.iNet         |           |
| Quectel UC20-E                         | 3G    | Yes    | GL.iNet         |           |
| ZTE ME909s-821                         | 4G    | Yes    | GL.iNet         |           |
| Huawei E1550                           | 3G    | Yes    | GL.iNet         |           |
| Huanwei E3276                          | 4G    | Yes    | GL.iNet         |           |
| TP-Link MA260                          | 3G    | Yes    | GL.iNet         |           |
| ZTE M823                               | 4G    | Yes    | Arnas Risqianto |           |
| ZTE MF190                              | 3G    | Yes    | Arnas Risqianto |           |
| Huawei E3372                           | 4G    | Yes    | anonymous       |           |
| Pantech UML290VW (Verizon)             | 4G    | Yes    | GL.iNet/steven  | QMI       |
| Pantech UML295 (Verizon)               | 4G    | Yes    | GL.iNet/steven  | Host-less |
| Novatel USB551L (Verizon)              | 4G    | Yes    | GL.iNet/steven  | QMI       |
| Verizon U620L (Verizon)                | 4G    | Yes    |                 | Host-less |
|                                        |       |        |                 |           |

*QMI: This modem supports QMI mode. Please choose **/dev/cdc-wdm0** in the **Device** list.

*Host-less: This modem supports tethering mode, please set up by using Tethering but not 3G/4G modem.

You can also refer to [http://ofmodemsandmen.com/supported.html](http://ofmodemsandmen.com/supported.html) for a well supported modem list.



### AT Command

The built-in modem supports AT command for the management and configuration of the modem. In 3G/4G Modem section, Click `AT Command`.

![at command](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/modem1.jpg)



- **Shortcut:** There are several pre-configured AT commands that you can use directly. If you want to run your own AT command, choose **Manual command**.
- **AT Command:** The place where you can input AT command. For the list of AT command, please refer to the AT command manual of the built-in modem.
- **Port:** The default port for AT command is **/dev/ttyUSB2**.

![AT command](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/at_command.jpg)



---

##4) Tethering

Using USB cable to share network from your smartphone to the router is called Tethering. Host-less modem works in Tethering during the setup of the modem as well.

For host-less modem tethering, plug it into the USB port of the router.

For smartphone tethering, connect it to the USB port of the router and click **Trust** to continue when the message pops up in your smartphone.

After plugging in your device, the Tethering section will update and your device will be shown on the device list. The device name will begin with **eth** or **usb** such as **eth2**, **usb0**. Choose your device and click `Connect`.

![tethering](https://static.gl-inet.com/docs/en/3/setup/4g_smart_router/internet/tethering.jpg)



### EasyTether

Some carriers prohibit the sharing of the data so that you may not be able to use tethering. However, you can try [easytethering](/app/tether.md). 

*Note: Easytether is not a free service and we have no affiliation with them.*