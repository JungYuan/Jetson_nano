<h3>First build a boot-disk</h3>
  - https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit<cr>
  
<h3>Install Fan and install Fan control service</h3>
  - https://github.com/Pyrestone/jetson-fan-ctl<cr>
  
<h3>Chinese input iBus-chewing</h3>
  - #install iBus-chewing<cr>
  - $sudo apt-get install ibus-chewing<cr>
  - #reboot<cr>
  - $sudo shutdown -r<cr>
  - #in X-shell setup -> Region/Language -> input -> more -> other -> select Chinese(chewing)<cr>
 
<h3>Install google chrome</h3>
  - $wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb <cr>
  - #lunch chrome<cr>
  - #update google chrome<cr>
  - $cat /etc/apt/sources.list.d/google-chrome.list<cr>
  ### THIS FILE IS AUTOMATICALLY CONFIGURED ###<cr>
  # You may comment out this entry, but any other modifications may be lost.<cr>
  deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main<cr>
 
<h3>Learn Hello AI world</h3>
  - https://github.com/dusty-nv/jetson-inference
