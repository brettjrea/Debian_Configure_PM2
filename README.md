# Debian_Configure_PM2

* You might have [Upgraded to Buster](https://github.com/brettjrea/Debian_Bullseye_Upgrade_Script)
* You might have [Upgraded to Jammy](https://github.com/brettjrea/Ubuntu_Jammy_Upgrade_Script)

---
## You will need node.
* [Install NVM](https://github.com/brettjrea/Debian_Install_NVM)
* [Install NVS](https://github.com/brettjrea/Debian_Install_NVS)
*Added 02/23 it is a cross-platform node based successor/replacement for NVM.*
---
*You should now [Install common build tools.](https://github.com/brettjrea/Debian_Install_Common_Build_Tools)*
___
*You might now want to [install Strapi.io](https://github.com/brettjrea/Debian_Strapi_Backend_API) backend*
___

A script that creates an ecosystem.config.js file in home, my-backend,and my-frontend for Strapi and Gatsby to start both processes.

```
sudo apt upgrade -y && sudo apt update -y && sudo apt autoremove -y &&
sudo apt install wget -y &&
sudo apt-get install --reinstall ca-certificates -y &&
wget https://raw.githubusercontent.com/brettjrea/Scripts_Fix/master/fixscripts.sh &&
wget https://raw.githubusercontent.com/brettjrea/Debian_Configure_PM2/master/configure-pm2.sh &&
sudo bash fixscripts.sh &&
bash configure-pm2.sh && 
sudo apt autoremove -y &&
sudo apt clean -y
pm2 start ecosystem.config.js
```


### To start any process in the ecosystem.config.js file.

```
pm2 start ecosystem.config.js
```
