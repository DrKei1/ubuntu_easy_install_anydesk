# ubuntu_easy_install_anydesk
a short script for easy install anydesk on ubuntu server with lxde

# IMPORTANT Tips:
1-in line 1 of the below code, change user and password (anydesk) then copy all strings to terminal.<br>
2-<b>IMPORTANT Warning:</b> select <b>lightdm</b> on installing proccess.<br>
<img src="https://github.com/DrKei1/ubuntu_easy_install_anydesk/blob/main/select-lightdm.jpg?raw=true">

# Code:
<br>
<code>
USER=user1; PASS=xAbNc@2cz; sudo adduser $USER; sudo adduser $USER sudo;sudo apt update -y; apt install lxde -y; apt install wget -y; wget -qO - https://keys.anydesk.com/repos/DEB-GPG-KEY | sudo apt-key add -; echo "deb http://deb.anydesk.com/ all main" | sudo tee /etc/apt/sources.list.d/anydesk-stable.list; apt update; apt install anydesk -y; sed -i ''  -e "s/#WaylandEnable/WaylandEnable/g" -e "s/#  AutomaticLoginEnable = true/AutomaticLoginEnable = true/g" -e "s/#  AutomaticLogin = user1/AutomaticLogin = $USER/g" /etc/gdm3/custom.conf;echo $PASS | anydesk --set-password;echo -e "\n\033[33mAnydesk Address:\033[m";anydesk --get-id;echo -e "\n\033[33mrebooting...\033[m"; reboot;
</code>
<br>

