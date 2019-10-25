<h3>First build a boot-disk</h3>
  - https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit<br>
  
<h3>Install Fan and install Fan control service</h3>
  - https://github.com/Pyrestone/jetson-fan-ctl<br>
 
<h3>Setup VNC server</h3>
  - ##Difficulty is hight##<br>
  #Make sure vino is install<br>
  - $sudo apt-get update<br>
  - $sudo apt-get install vino<br>
  #edit file to creat key<br>
  - sudo vi /usr/share/glib-2.0/schemas/org.gnome.Vino.gschema.xml<br>
  ##Add following code into file##<br>
  Please check the file append.xml 
  ""
      <key name='enabled' type='b'>
        <summary>Enable remote access to the desktop</summary>
        <description>
          If true, allows remote access to the desktop via the RFB
          protocol. Users on remote machines may then connect to the
          desktop using a VNC viewer.
        </description>
        <default>false</default>
      </key>
  </xmp>
  
  
<h3>Chinese input iBus-chewing(pinyin)</h3>
  - #install iBus-chewing<br>
  - $sudo apt-get install ibus-chewing(pinyin)<br>
  - $sudo ibus restart<br>
  - #reboot<br>
  - $sudo shutdown<br>
  - #in X-shell setup -> Region/Language -> input -> more -> other -> select Chinese(chewing)<br>
  - # or $ibus-setup<br>
 
<h3>Install google chrome</h3>
  - $wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb <br>
  - #lunch chrome<br>
  - #update google chrome<br>
  - $cat /etc/apt/sources.list.d/google-chrome.list<br>
  ### THIS FILE IS AUTOMATICALLY CONFIGURED ###<br>
  # You may comment out this entry, but any other modifications may be lost.<br>
  deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main<br>
 
<h3>Learn Hello AI world</h3>
  - https://github.com/dusty-nv/jetson-inference<br>
