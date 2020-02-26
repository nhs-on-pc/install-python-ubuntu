#History of fix errors when using Ubuntu, Pycharm and coding Python ...

##1. Install Ubuntu beside Windows:
- Use GPT to create usb flash boot 
- No need efi partition

##2. No modules name: distutils.core while create virtual environments or install packages
- sudo apt-get install python3-distutils<br>
- sudo apt install python3-pip

##3. UserWarning: Matplotlib is currently using agg, which is a non-GUI backend, so cannot show the figure.
>https://www.pyimagesearch.com/2015/08/24/resolved-matplotlib-figures-not-showing-up-or-displaying/ <br>
- in venv: <br>
- python setup.py install

##4. Ubuntu 19.04 did not remember volume levels after reboot
>https://bugs.launchpad.net/ubuntu/+source/pulseaudio/+bug/410446 <br>
1. Remove all pulseaudio related files from your home directory, so .pulse_cookie and .pulse/* leave the .pulse directory in tact for the next step.
2. Create /home/your-username/.pulse/client.conf and add the following line to it: <br>
    - autospawn = no <br>
    - This is so that when we kill pulseaudio, it won't start right back up again when we don't want it to.
3. Kill pulseaudio with "pulseaudio -k"
4. Reset your alsa volume settings with the following command: "sudo /etc/init.d/alsa-utils reset". You will be asked for your password due to using the sudo command.
5. Start pulseaudio again with "start-pulseaudio-x11".

##5. Reset mực máy in Brother HL-2240D: 
- Tutorial: https://youtu.be/XECkWU2bRw0
- Tốt hơn hết là làm với máy tính boot windows

##6. Usb cannot eject although completed copy files on Ubuntu:
- Try ls /media and see if the drive shows there. If it does, sudo umount /media/drivename – douggro
- https://askubuntu.com/questions/395186/unable-to-eject-safely-unmount-usb-drive

##7. Increase mouse scroll:
- http://www.webupd8.org/2015/12/how-to-change-mouse-scroll-wheel-speed.html



