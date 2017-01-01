# JamesBondBot
A Twitter bot ([@JamesBondBot](https://twitter.com/JamesBondBot)) that likes and retweets tweets with hashtags related to James Bond, such as #JamesBond and #007. A Node.js web app running on a Raspberry Pi 3.

## Getting started
- [Grab and uncompress the latest ARMv7 version of Node.js](https://nodejs.org/en/download/) (at this time of writing, it was v6.9.2) and make Node.js's tools accessible from anywhere on the Pi
  - This involves renaming the directory to something much simpler, like 'nodejs', and including nodejs in the PATH variable
```
wget https://nodejs.org/dist/v6.9.2/node-v6.9.2-linux-armv7l.tar.xz
tar xvf node-v6.9.2-linux-armv7l.tar.xz
mv node-v6.9.2-linux-armv7l.tar.xz nodejs
sudo nano /home/pi/.bashrc
export PATH=$PATH:/home/pi/<path/to>/nodejs/bin/
source .bashrc
```
- Now you can simply type `node` into Terminal to open the Node shell and run JavaScript commands
- Create a Twitter account with a verified phone number
- [Create a new Twitter app](https://apps.twitter.com/app/new) and copy down the Consumer Key / Consumer Secret / Access Token / Access Token Secret

## Setup
- Make the /home/pi/bondbot directory and work from within it
```
sudo mkdir bondbot
cd bondbot
sudo touch bot.js
sudo touch config.js
sudo apt-get install npm
npm update
sudo npm install twit
```
