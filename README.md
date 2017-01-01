# JamesBondBot
A Twitter bot ([@JamesBondBot](https://twitter.com/JamesBondBot)) that likes and retweets tweets with hashtags related to James Bond, such as #JamesBond and #007. Running on Node.js on a Raspberry Pi 3 . The following is derived almost entirely from [this tutorial](https://hackernoon.com/create-a-simple-twitter-bot-with-node-js-5b14eb006c08#.dj4gkz86k) and from Issue #20 of Raspberry Pi Geek Magazine.

## Getting started
- [Grab and uncompress the latest ARMv7 version of Node.js](https://nodejs.org/en/download/) (at this time of writing, it was v6.9.2) and make Node.js's tools accessible from anywhere on the Pi:
```
wget https://nodejs.org/dist/v6.9.2/node-v6.9.2-linux-armv7l.tar.xz
tar xvf node-v6.9.2-linux-armv7l.tar.xz
mv node-v6.9.2-linux-armv7l.tar.xz nodejs #This renames the directory to the much simpler 'nodejs'
sudo nano /home/pi/.bashrc
export PATH=$PATH:/home/pi/<path/to>/nodejs/bin/ #This includes nodejs into the PATH variable; save the .bashrc file after adding this line
source .bashrc
```
- Now you can simply type `node` into Terminal to open the Node shell and run JavaScript commands
