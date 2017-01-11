# Installing console dash on raspberry pi

##### If RPI is a fresh install you might need to expand your file system

`sudo raspi-config`

`choose option 1 (expand file system)`

`reboot`


##### Install node

`sudo apt-get update`

`sudo apt-get upgrade`

`sudo apt-get install nodejs npm`


##### Install Chromium

`wget -qO - http://bintray.com/user/downloadSubjectPublicKey?username=bintray | sudo apt-key add -`

`echo "deb http://dl.bintray.com/kusti8/chromium-rpi jessie main" | sudo tee -a /etc/apt/sources.list`

`sudo apt-get update`

`sudo apt-get install chromium-browser rpi-youtube -y`

##### Install Dash

`git clone https://github.com/MichLass/LassConsult.git`

`cd LassConsult`

`npm install`


##### Install script for mausberry circuit

`http://mausberrycircuits.com/pages/car-setup`

Open Menu > Preferences > Default applications for LXSession

Add these two entries to Autostart

`@/home/pi/LassConsult/startScript.sh`

`@chromium-browser —kiosk --incognito file:///home/pi/LassConsult/re-direct-page.html`


# How to run for development

This will loop through KPH RPM and Temp so you can style things without being connected to a car :)

`npm run dev`

# CREDITS

Most of the work has been done by Greg Mathews, creator of the original consultDash.
I just added more.
