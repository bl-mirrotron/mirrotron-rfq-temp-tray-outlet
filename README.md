# RFQ Outlet Temperature Tray
* <a href="https://github.com/bl-mirrotron/mirrotron-rfq-temp-tray-outlet" target="_blank">Source code</a>
* [Cooling system overview](https://docs.bl-mirrotron.com/#cooling-system)
* [Control system overview](https://docs.bl-mirrotron.com/)

The function of the RFQ Outlet Temperature Tray is to receive data and check alarm status from the <a href="https://docs.bl-mirrotron.com/mirrotron-rfq-temp-cube/">RFQ Temperature Cube</a> mounted on the outlet header as shown in Figure 1. The tray is installed on a Raspberry Pi ZeroW as shown in Figure 2. The Raspberry Pi ZeroW is actually mounted on the underside of the temperature cube as shown in Figure 3.

Because the cooling headers are located far from any Ethernet connection, the tray communicates with the <a href="https://docs.bl-mirrotron.com/mirrotron-box/">Mirrotron application server</a> via wireless connections. A continuously changing watchdog signal verifies that the communication link is intact. The tray code is written in the <a href="https://nodered.org/" target="_blank">Node-RED</a> programming environment. The tray code uses the standard Blinky-Lite template for serial communication using Blinky-Bus as shown in Figure 4.

<p></p><p style="text-align:center;font-size: large;"><span style="font-weight: bold;color: green;">Figure 1. </span> <span style="font-style: italic;">Outlet Cooling Header.<br>From left to right: Temperature cube and tray, 5V power, 24V power, Flow cube and tray</span></p>
<div style="width:100%;text-align:center;"><img width="100%" style="border-style:solid;border-color:#1c6e97;" src="doc/RFQCoolingOutletHeader.jpg"/></div><br>

<p></p><p style="text-align:center;font-size: large;"><span style="font-weight: bold;color: green;">Figure 2. </span> <span style="font-style: italic;">Raspberry Pi ZeroW tray along with temperature cube</span></p>
<div style="width:100%;text-align:center;"><img width="100%" style="border-style:solid;border-color:#1c6e97;" src="doc/tempCubeWithRPi.jpg"/></div><br>

<p></p><p style="text-align:center;font-size: large;"><span style="font-weight: bold;color: green;">Figure 3. </span> <span style="font-style: italic;">Raspberry Pi ZeroW tray mounted on temperature cube</span></p>
<div style="width:100%;text-align:center;"><img width="100%" style="border-style:solid;border-color:#1c6e97;" src="doc/TempCubeWithTray.jpg"/></div><br>

<p></p><p style="text-align:center;font-size: large;"><span style="font-weight: bold;color: green;">Figure 4. </span> <span style="font-style: italic;">RFQ Outlet Temperature Tray Node-RED flow</span></p>
<div style="width:100%;text-align:center;"><img width="100%" style="border-style:solid;border-color:#1c6e97;" src="doc/mirrotron-rfq-temp-tray-outlet.png"/></div><br>
