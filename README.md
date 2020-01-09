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
  Please check the file append.xml <br>
  ##after saved file, we need to compile##<br>
  -$sudo glib-compile-schemas /usr/share/glib-2.0/schemas<br>
  ## modify setting ##<br>
  -$gsettings set org.gnome.Vino enabled true<br>
  -$gsettings set org.gnome.Vino prompt-enabled false<br>
  -$gsettings set org.gnome.Vino require-encryption false<br>
  ## Create/Modify ~/.config/autostart/vino-server.desktop ##<br>
  -$sudo vi ~/.config/autostart/vino-server.desktop<br>
  ## to add following code for autorun after login Xwin, please check append.desktop##<br>
  -$sudo reboot
  
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

<h3>Install hardware information show</h3>
  - sudo pip install jetson-stats<br>
  - sudo jtop<br>
  
<h3>Install virtualenv, virtualenvwrapper</h3>
  - sudo pip install virtualenv virtualenvwrapper<br>
  - vim ~/.bashrc<br>
     # virtualenv and virtualenvwrapper<br>
     export WORKON_HOME=$HOME/.virtualenvs<br>
     export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3<br>
     source /usr/local/bin/virtualenvwrapper.sh<br>
     
<h3>Install Jupyter notebook/Lab</h3>
  - sudo apt install nodejs npm<br>
  - sudo pip3 install jupyter jupyterlab<br>
  - sudo jupyter labextension install @jupyter-widgets/jupyterlab-manager<br>
  - sudo jupyter labextension install @jupyterlab/statusbar<br>
  - jupyter lab --generate-config<br>
  - jupyter notebook password<br>
  - jupyter lab or jupyter notebook <b>#start jupyter server</b><br>
  
<h3> Install Jupyter virtualenv</h3>
  - workon $envs$ <b>#$envs$ fill your virtualenv name</b><br>
  - pip install ipykernel<br>
  - python -m ipykernel install --user --name=$vens$<br>
  
<h3>Learn Hello AI world</h3>
  - https://github.com/dusty-nv/jetson-inference<br>

<h3>link cv2 to virtualenv</h3>
  - sudo find / -name "cv2*"<br>
  - cd ~/envs/AI/lib/python3.6/site-packages<br>
  - ln -s /usr/lib/python3.6/dist-packages/cv2.cpython-36m-aarch64-linux-gnu.so<br>
  
<h3>using more memory by swapfile</h3>
  - df -h <b>#check disk size</b><br>
  - free -h <b>#check memory usage status</b><br>
  - sudo fallocate -l 4G /swapfile<br>
  - sudo chmod 600 /swapfile<br>
  - ls -lh /swapfile<br>
  - sudo mkswap /swapfile<br>
  - sudo swapon /swapfile<br>
  - sudo swapon -show<br>
  - free -h<br>
  - sudo cp /etc/fstab /etc/fstab.bak<br>
  - echo '/swapfile none swap sw 0 0'| sudo tee -a /etc/fstab<br>
  
<h3>Useful information link</h3>
  <li>https://www.hackster.io/news/getting-started-with-the-nvidia-jetson-nano-developer-kit-43aa7c298797</li>
  <li>https://juejin.im/post/5cd01844e51d453a6c23b076</li>
  <li>short prompt PS1="\w $: " https://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html </li>
  <li><a href="https://www.pyimagesearch.com/2019/05/06/getting-started-with-the-nvidia-jetson-nano/">OpenCV and AILearn reference</a></li>
