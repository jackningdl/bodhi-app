# Install and Usage
Download the last binary at our releases page: https://github.com/bodhiproject/bodhi-app/releases

## Mac

1. Run `Bodhi-x.x.x.dmg`
2. Drag the Bodhi icon to the `Applications` folder
3. You may get a warning dialog that says "Bodhi can't be opened because it is from an unidentified developer." If you do, find the `Bodhi` app in the Finder and right-click it and `Open`. This will open another dialog, which you will press `Open` again.
4. Enjoy!

## Windows

1. Please disable your antivirus, or whitelist the Bodhi app from your antivirus program. Some antiviruses will come back as a false positive so if you don't disable it, it could automatically quarantine the app. This will make the app disappear.
2. Run `Bodhi-x.x.x.exe`
3. Enjoy!

## Linux

1. Run `Bodhi-0.3.0-i386.AppImage` or `Bodhi-0.3.0-x86_64.AppImage`
2. Enjoy!

# Winning Rates Formulae
Here are the formula calculations for determining how much BOT and QTUM you will win on an Event.

QTUM Return Rate:
```
// 1% percent of losing QTUM gets split by BOT winners
losersQtumReward = totalLosingQtumBets * 1 / 100

// total losing QTUM less the 1% reward that goes to BOT winners
losersAdjustedQtum = totalLosingQtumBets - losersQtumReward

// QTUM won from QTUM bets only
qtumWon = (yourQtumWinningBets / totalQtumWinningBets * losersAdjustedQtum) + yourQtumWinningBets
```

BOT Return Rate:
```
// BOT won from your BOT winning votes
botWon = (yourBotWinningBets / totalBotWinningBets * losersTotal) + yourBotWinningBets

// QTUM reward won from BOT winning votes
botQtumWon = yourBotWinningBets / totalBotWinningBets * losersQtumReward
```

Total Return:
```
qtum = qtumWon + botQtumWon
bot = botWon
```
