# Current status
Robius is a brand new vision -- we're just getting off the ground.

Currently, the best way to get started is to directly use one of the [recommended UI toolkits](#key-community-members) to build out your application's UI and define its UX behavior.
For now, everything else beyond UI will require you to add the missing pieces yourself, e.g., network connectivity, async multitasking, and access to other device peripherals or system services. 

Everything is developed right here in the open, so check back for updates often!
We plan to introduce a pre-alpha version of the full Robius system stack (everything beneath the application) by early-to-mid 2024, which will enable easier access to and integration of other platform/OS features alongside the UI toolkits.


## Platform support

The following table indicates which projects in the Robius community currently support a given feature on each given platform.

The key/legend for this table is as follows:
* MP : supported by Makepad.
* DX : supported by Dioxus.
* OS : supported by Osiris.
* —  : feature not applicable or not planned for the given platform.
* Blank table cells indicate the feature has not been started.

<!-- cspell:disable -->
<div>
<br>
<style type="text/css">
.tg th{border-color:black;border-style:solid;border-width:2px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-bold-center{font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-left{border-width:2px;text-align:left;vertical-align:top}
.tg .tg-center{text-align:center;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-bold-center"></th>
    <th class="tg-bold-center">Android</th>
    <th class="tg-bold-center">iOS</th>
    <th class="tg-bold-center">Linux</th>
    <th class="tg-bold-center">MacOS</th>
    <th class="tg-bold-center">Windows</th>
    <th class="tg-bold-center">Web</th>
    <th class="tg-bold-center">OpenHarmony</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-left">Basic build tool</td>
    <td class="tg-center">MP DX OS</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center">MP DX OS</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Basic UI</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">UI live/hot reload</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center">MP DX</td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Multiwindow</td>
    <td class="tg-center">—</td>
    <td class="tg-center">—</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Input Events</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Timers, Alarms</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Camera</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Audio Input</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Audio Playback</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">MIDI Output</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Video Playback</td>
    <td class="tg-center">MP</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Storage/Filesystem</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Networking</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Permissions mgmt</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Geolocation</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Clipboard (text)<br></td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Notifications</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Drag &amp; Drop</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center">MP</td>
    <td class="tg-center">MP</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Accelerometer/Gyro</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Vibration/haptics</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Biometric</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">WiFi mgmt</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Bluetooth</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Display brightness</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Power/Battery state</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Physical buttons</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Proximity sensor</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
  <tr>
    <td class="tg-left">Ambient light sensor</td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
    <td class="tg-center"></td>
  </tr>
</tbody>
</table>
</div>
<!-- cspell:enable -->

