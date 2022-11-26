# ubuntu_easy_install_anydesk
<b>a short script for easy install anydesk on ubuntu server with LXDE</b><br>
solved errors:
desk_rt_ipc_error, display_server_not_supported anydesk.<br>
tested on ubuntu 20.04

# IMPORTANT Tip:
Select <b>lightdm</b> on installing proccess.<br>
<img src="https://github.com/DrKei1/ubuntu_easy_install_anydesk/blob/main/anydesk-set-lxde.jpg?raw=true">

# Code:
in line 1 of the below code, change user and password(anydesk) to your liking then copy all strings to terminal:<br><br>
<code>
USER=user1; PASS=xAbNc@2cz; sudo adduser $USER; sudo adduser $USER sudo;sudo apt update -y; apt install lxde -y; apt install wget -y; wget -qO - https://keys.anydesk.com/repos/DEB-GPG-KEY | sudo apt-key add -; echo "deb http://deb.anydesk.com/ all main" | sudo tee /etc/apt/sources.list.d/anydesk-stable.list; apt update; apt install anydesk -y; sed -i ''  -e "s/#WaylandEnable/WaylandEnable/g" -e "s/#  AutomaticLoginEnable = true/AutomaticLoginEnable = true/g" -e "s/#  AutomaticLogin = user1/AutomaticLogin = $USER/g" /etc/gdm3/custom.conf;echo $PASS | anydesk --set-password;echo -e "\n\033[33mAnydesk Address:\033[m";anydesk --get-id;echo -e "\n\033[33mrebooting...\033[m"; reboot;
</code>

# Login with LXDE:
after reboot, login with anydesk, and select LXDE:<br>
<img src="https://github.com/DrKei1/ubuntu_easy_install_anydesk/blob/main/anydesk-set-lxde.jpg?raw=true">


