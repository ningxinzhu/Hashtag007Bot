# JamesBondBot
A Twitter bot ([@JamesBondBot](https://twitter.com/JamesBondBot)) that likes and retweets tweets with hashtags related to James Bond, such as #JamesBond and #007. A Node.js web app running on a Raspberry Pi 3. The following is derived almost entirely from [this tutorial](https://hackernoon.com/create-a-simple-twitter-bot-with-node-js-5b14eb006c08#.dj4gkz86k) and from Issue #20 of Raspberry Pi Geek Magazine.

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
- Back in the normal shell, install [twit](https://www.npmjs.com/package/twit):
```
sudo apt-get install npm
npm update
npm install twit
```

## Setup
- Make the bondbot directory and configure it with a package.json file:
```
sudo mkdir bondbot
cd bondbot
sudo npm init
```
- Create bot.js and config.js (using `sudo touch`) in the same directory and edit the `main` field in package.json to
```
{  
  "main": "bot.js",  
},
```
