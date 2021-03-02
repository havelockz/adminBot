#HATB
havelock administator telegram bot

#Overview
HATB is a modular multi-group telegram administration helper

#Setup
##Dependencies
HATB needs python-telegram-bot to works properly:

pip3 install python-telegram-bot

#Installation
First you need to clone the repository

git clone https://github.com/ExxonRsky/adminBot

Now you have to create a bot and paste the APIKEY inside the TOKEN variable inside config.py located in the same directory of bot.py

You have to create an sqlite3 file called buster.db using this command

sqlite3 busterdb < db.sql

And finally you can run you personal istance of YATAB

chmod +x bot.py

./bot

#Modules
HATB offers a modular system to integrate commands and actions to the bot, if you want to create your own module check the Wiki page

#There are 2 different kinds of modules:

##Commands modules
These modules contains only the single commands you can use with /name-of-the-command

##Current command modules:

 /ban - ban the user that wrote the quoted message
 /unban - unban the user that wrote the quoted message
 /mode +o - change the mode of the user quoted in the message to operator
 /mode -o - change the mode of the user quoted in the message from operator to user
 /op - if the user is an operator giving this command can became an administrator of the group
 /s0ng - send a random song from this YouTube Channel
 /ping - just for fun, the bot will answer pong
 /help - shows commands and controls info
 /groupinfo - show groups info
 /info - show info about the quoted user
 
##Onjoin modules
These are all the actions the bot will make every time a new user join

 nobots - if a bot not in whitelist joins the group it will be banned
 not_ascii_name - kick users with non-ascii char in first name
 
##OnMessage modules
These are all the actions the bot will do every time someone send a new message(it includes stickers, gifs, images, etc..)

 antiflood - integrates an algorithm to stop flooders inside the group
