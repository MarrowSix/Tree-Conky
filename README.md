# Tree-Conky
A conky theme transport from “https://www.reddit.com/r/Conkyporn/comments/4gkr0b/tree_conky/”， and I fix som problem on my system (Ubuntu 16.04 with gnome3).

### Use
1、Install Conky<br>
**Ubuntu** 
  ``` 
  sudo apt-get install conky
  ``` 
  
**Other**<br>
[conky github](https://github.com/brndnmtthws/conky)

2、Open Double Buffer<br>
The deault vga drive of ubuntu was not support double buffer, you need install other drive of your video card, like nvidia. after install completed, you need open file "/etc/X11/xorg.conf" and modified. if you didn't find this file, you kan use command : 
<br>
  ```shell
  sudo nvidia-xconfig 
  ```
to init and create it. Now type command to backup your xorg.conf and modified it.
  ```shell
  sudo cp /etc/X11/xorg.conf ~/Document/xorg.conf.bak
  ```
**Modified**
  ```shell
  sudo vim /etc/X11/xorg.conf
  # find "Module" and add "Load "dbe"", as follower
  # Section "Module"
   #   Load    "dbe"
   # EndSection
  ```

then restart system and you can use command
  ```shell
  conky conky.conf
  ```
to use that.
