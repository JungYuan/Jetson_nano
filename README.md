<h3>First build a boot-disk</h3>
  - https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit
  
<h3>Install Fan and install Fan control service</h3>
  - https://github.com/Pyrestone/jetson-fan-ctl
  
<h3>Chinese input iBus-chewing</h3>
  - #install iBus-chewing
  - $sudo apt-get install ibus-chewing
  - #reboot
  - $sudo shutdown -r
  - #in X-shell setup -> Region/Language -> input -> more -> other -> select Chinese(chewing)
 
<h3>Install google chrome</h3>
  - $wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb 
  - #lunch chrome
  - #update google chrome
  - $cat /etc/apt/sources.list.d/google-chrome.list
  ### THIS FILE IS AUTOMATICALLY CONFIGURED ###
  # You may comment out this entry, but any other modifications may be lost.
  deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main
 
<h3>Learn Hello AI world</h3>
  - https://github.com/dusty-nv/jetson-inference
