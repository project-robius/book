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

<div>
<br>
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-1wig{font-weight:bold;text-align:left;vertical-align:top}
.tg .tg-baqh{text-align:center;vertical-align:top}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-amwm{font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-7btt{border-color:inherit;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-1wig"></th>
    <th class="tg-amwm">Android</th>
    <th class="tg-amwm">iOS</th>
    <th class="tg-amwm">Linux</th>
    <th class="tg-amwm">MacOS</th>
    <th class="tg-amwm">Windows</th>
    <th class="tg-7btt">Web</th>
    <th class="tg-7btt">OpenHarmony</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Basic build tool</td>
    <td class="tg-baqh">MP DX OS</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-baqh">MP DX OS</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-baqh"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Basic UI</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-c3ow">MP DX</td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0lax">UI live/hot reload</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-baqh">MP DX</td>
    <td class="tg-baqh"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Multiwindow</td>
    <td class="tg-baqh">—</td>
    <td class="tg-baqh">—</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Input Events</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Timers, Alarms</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Camera</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Audio Input</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Audio Output</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh"></td>
    <td class="tg-c3ow">MP</td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Video Playback</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Storage/Filesystem</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Networking</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Permissions mgmt</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Geolocation</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Clipboard (text)<br></td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-baqh">MP</td>
    <td class="tg-c3ow">MP</td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Notifications</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Drag &amp; Drop</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow">MP</td>
    <td class="tg-c3ow">MP</td>
    <td class="tg-c3ow">MP</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Accelerometer/Gyro</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-0pky"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Vibration/haptics</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-0pky"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Biometric</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-0pky"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0pky">WiFi mgmt</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-0pky"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Bluetooth</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-0pky"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Display brightness</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-0lax"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Power/Battery state</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-0lax"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Ambient light sensor</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-0lax"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Proximity sensor</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-0lax"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
  </tr>
  <tr>
    <td class="tg-0lax">Physical buttons</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-0lax"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
  </tr>
</tbody>
</table>
</div>
