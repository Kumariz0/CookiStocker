# CookiStocker
This is a GitHub version of the CookiStocker Cookieclicker stoks bot

*(The following description is from the original mod page on Steam Workshop)*

---

What is this?
This is a mod that will automatically trade on the Stock Market for you.



Over a sufficient length of time it will easily get you the Liquid Assets (profit 10 million $econds) and Gaseous Assets (profit 1 year of $econds) achievements, the latter of which is currently the rarest Cookie Clicker achievement of all time.

If you find this guide outside of Steam - It has been copied without my permission. Click this link to see the most up-to-date original guide.	
Installation
Option zero: Subscribe to the mod on Steam Workshop
- Workshop page -

Option one: Install the mod
- Download CookiStocker 1.5 - [drive.google.com]

To install the mod, extract the archive into your mod directory (...\Steam\steamapps\common\Cookie Clicker\resources\app\mods\local). Restart your game, go to Options -> Mods -> "Manage mods", and enable CookiStocker.
You should be greeted by the Stocker when you press "Restart with new changes".

Option two: Run the script from console
- Pastebin with the console script 1.5 -[pastebin.com]

If you do not want to install a mod, open your console, copy the whole script and paste it there and press enter.

Instructions on how to open the console in the Steam version of the game can be found here	
Changelog
Current version - 1.6
• Fixed the resting price formula

Version 1.5
• Fixed critical bug prohibiting the bot from remembering warehouse contents properly
• Fixed the formula calculating session profits
• Fixed better time display
Increasing the efficiency
Before you launch, make sure to:

1. Check if you are running the latest version of the mod.
The algorithm is constanly being improved, so using the most recent version will guarantee that all discovered bugs and suboptimal expressions are fixed and optimised.
1. Leave some spare cookies in the bank.
The bot will try to buy as much stock as it can when it detects an opportunity, so make sure you have the cookies to fill up a full warehouse of your most expensive stock.
1. Max out your brokers.
Obviously, they will increase the efficiency of your trading.
1. Level your offices.
Warehouse space is very important if you do not want to wait 7 hours to sell 100 stock. If you want to get the best results - you should focus your lumps on getting cursors to level 12.
1. Level your bank.
Bank level increases the resting value of all stocks. Getting it to level 10 should be on your priority list, but not as high as the cursor level.
Options
To access options, open the main.js file inside the mod folder. You will see all of the avaliable options at the start of the file.
Some options can either be turned on or off by writing "true" or "false" respectively, and some require a number.

• Transaction Notifications
Turns on/off the notifications for every transaction, like in the gif above. Default - on

• Activity Report
Turns on/off the activity report (shown below). Default - on, every 60 minutes.


• Fast Notifications
Makes the mod's notifications fade away quickly on their own.
If you have 'Fast notes' option of the base game turned off - the notifications will stay up until closed manually. Default - off

• Console Announcements
Shows more info about the algorithm's logic in the game console. Default - off

• Loop Frequency
This option controlls the frequency at which the algorithm looks at the market.
The market itself updates every 60 seconds, so it is set to 30 seconds (30000 in milliseconds) to make sure the logic triggers every update no matter when the mod initialised.

You should not touch the Loop Frequency, to be honest. It is placed there only because there are instructions on how to make this mod into a cheat on the line 121 of main.js	
How it works
Too Long, Didn't Read
The stocks can behave in a limited amount of ways, called 'modes' in the code.
By knowing the future trend of any individual stock the algorithm makes its decidions on what to buy, what to hold and what to sell, and does so more efficiently than any real stock bot ever could.

In depth
People with clearly too much spare time on Cookie Clicker Wiki have done a better job at explaining the fundamentals of the market behaviour.[cookieclicker.fandom.com]
In brief, there are 6 possible modes: stable, slow rise, slow fall, fast rise, fast fall and chaotic.
The algorithm activates when the mode changes, and decides what to do:
If a fall stopped, and the price is lower than the resting price - buy.
If a rise stopped, and the price is higher than the resting price - sell.
If a chaotic behavior changed into a fall or a rise while above or below the resting - sell or buy respectively.
Troubleshooting & FAQ
Q: The mod is not doing anything, have I installed it correctly?
A: That can be easily checked by checking the Mod Manager menu. If it does not show up there - you did not install it properly.
Check that you have unarchived the folder properly, the directory should look like /mods/local/CookiStocker/ with main.js & info.txt in it.

Q: The mod is installed correctly, but it is still not doing anything.
A: If it shows you this notification when launched - that means it has initialised and is working.

The stocks market changes very slowly and in a stroke of bad luck it can run up to twelve hours without triggering the bot.
Keep in mind that the gif in the first section shows more than 10 hours of idling.

Q: Some stock's price dipped / peaked and it did not buy / sell. Did the bot not see it?
A: The bot only triggers when the trend of a stock changes, e. g. when the slow or fast trend changes into growing or stable, it buys at the minimum price. That means it can miss dips or peaks if they are happening during a chaotic trend, where the algorithm can not predict the future reliably, waiting for it to end and seeing where the price lands instead.
Actually, if you think that you are smarter than the bot, you can try trading goods on your own, when the bot declared the stock unstable and started ignoring it. This is not even a sarcasm. It is unlikely to break the bot also.

Q: I closed the game. Will it remember the purchases it made?
A: Kind of. Straignt answer - no, but it will not disrupt its work.
It functions with the market it has in the moment, not the market it remembers, so even if you buy or sell something yourself it should still function properly, although the report will not register profits made by the player.

Q: Does this mod disable achievements?
A: No.

Q: Does this mod conflict with any other mods?
A: No conflicts have been detected with any popular mods and it is unlikely that they ever will.

Do not be alarmed if the bot runs for extended periods of time without buying anything
It is looking for any stock's trend to change in order to buy it at its lowest and sell it at its highest price. Luck on that can vary from a couple of purchases per hour to no purchases in a couple of hours. But still,
make sure you are running the latest version to decrease the probability of such behaviour being caused by bugs

If you are still having issues - write a comment below.
If the mod is working correctly - write a comment as well and show off your success.
