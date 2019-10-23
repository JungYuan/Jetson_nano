<h3>First build a boot-disk</h3>
  - https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit<br>
  
<h3>Install Fan and install Fan control service</h3>
  - https://github.com/Pyrestone/jetson-fan-ctl<br>
  
<h3>Chinese input iBus-chewing(pinyin)</h3>
  - #install iBus-chewing<br>
  - $sudo apt-get install ibus-chewing(pinyin<br>
  - #reboot<br>
  - $sudo shutdown -r<br>
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
