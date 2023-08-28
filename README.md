# [EA - Budak Ubat](https://github.com/syarief02/EA_Budak_Ubat/archive/refs/heads/main.zip)

## Table of contents
- [Overview](#overview)
  - [How it works](#how-it-works)
  - [EA Parameters](#ea-parameters)
  - [Authorized account list](#authorized-account-list)
  - [How to get authorized](#how-to-get-authorized)
  - [How to install an EA on MT4 (fastest method)](#how-to-install-an-ea-on-mt4)
- [Update Logs](#update-logs)
  - [EA Budak Ubat v1.61](#ea-budak-ubat-v161)
  - [EA Budak Ubat v1.60](#ea-budak-ubat-v160)
  - [EA Budak Ubat v1.58](#ea-budak-ubat-v158)
  - [EA Budak Ubat v1.56](#ea-budak-ubat-v156)
  - [EA Budak Ubat v1.55](#ea-budak-ubat-v155)
- [Author](#author)

## Overview
## EA Budak Ubat v1.61 - [Download](https://github.com/syarief02/EA_Budak_Ubat/raw/main/EA%20-%20Budak%20Ubat%20v1.61%20-%2020230901.ex4)

### How it works
- When the EA is active, it will analyze the chart based on the Execution Mode parameter. 

- If there are no existing positions on the chart, the EA will enter a trade based on the parameter. If the trend is bullish, it will enter a buy trade and if it is bearish it will enter a sell trade. And it will also set a Stop loss order at a certain distance from the opened trade price if the stop loss variable is greater than 0. 0 means no stop loss. 

- If there are existing positions on the chart and the last one is in loss, EA will check if the distance between the current market price and the order is at least the minimum distance set by the user, and then it will enter a trade based on the candle, lot size will be calculated using the martingale method, and will set a Stop loss order at a certain distance from the opened trade price if the stop loss variable is greater than 0. 

- If Hedging is set to false, the EA will only enter trades in one direction at a time. If the first position is a buy trade, all subsequent martingale positions must also be buy trades. If the first position is a sell trade, all subsequent martingale positions must also be sell trades. If Hedging is set to true, the EA will enter trades in both directions. 

- The EA will modify the take profit of all positions in the same direction to a single break-even point plus the take profit level set by the user. 
#
### EA Parameters
##### *Execution Mode:* 
- on Every New Bar: when the EA is active, it will analyze the chart on every new bar (candle). It enter trades only after new candle appear. it will still follow the distance setting for the new layer, but only enter trades after the candle closes.  
on Every Tick: the EA enter trades immediately when attached and also enter new layer immediately when the distance between order setting is met. 

##### *Positions Mode:* 
- by default the EA uses the Buy & Sell mode, but it can be configured to operate only on Buy or in Sell.

##### *Enable/Disable Hedging:* 
- If Hedging is set to false, the EA will only enter trades in one direction at a time. If the first position is a buy trade, all subsequent martingale positions must also be buy trades. If the first position is a sell trade, all subsequent martingale positions must also be sell trades. 
- If Hedging is set to true, the EA will enter trades in both directions. 

##### *Analysis Method:* 
- This Parameter is only for the EA to determine the FIRST DIRECTION of the entry if there are no existing positions on the chart. It can be set to uses one of the four other analysis methods: Classic Candle (Bull/Bear), SMA20, Alligator, Ichimoku. 
 
    - The older version of this EA was based on the Candle Method. If the candle is bullish, it will enter a buy trade and if it is bearish it will enter a sell trade. 

    - The SMA20 is just a simple moving average of period 20. it buy above the line and sell below the line.

    - With Alligator it uses the Alligator indicator and it buy above all the 3 lines and sell below all the 3 lines.
        - The Williams Alligator indicator is a technical analysis tool that uses smoothed moving averages. The indicator uses a smoothed average calculated with a simple moving average (SMA) to start. It uses three moving averages, set at five, eight, and 13 periods. The three moving averages comprise the Jaw, Teeth, and Lips of the Alligator. The indicator applies convergence-divergence relationships to build trading signals, with the Jaw making the slowest turns and the Lips making the fastest turns. 
            - Ref: https://www.investopedia.com/articles/trading/072115/exploring-williams-alligator-indicator.asp .

     - With Ichimoku, it uses the Ichimoku indicator. It buy above the cloud and sells below it.
        - The Ichimoku Cloud is a collection of technical indicators that show support and resistance levels, as well as momentum and trend direction. It does this by taking multiple averages and plotting them on a chart. It also uses these figures to compute a “cloud” that attempts to forecast where the price may find support or resistance in the future.
        - The Ichimoku Cloud is composed of five lines or calculations, two of which comprise a cloud where the difference between the two lines is shaded in.
        - The lines include a nine-period average, a 26-period average, an average of those two averages, a 52-period average, and a lagging closing price line.
        - The cloud is a key part of the indicator. When the price is below the cloud, the trend is down. When the price is above the cloud, the trend is up.
        - The above trend signals are strengthened if the cloud is moving in the same direction as the price. For example, during an uptrend, the top of the cloud is moving up, or during a downtrend, the bottom of the cloud is moving down.
            - Ref: https://www.investopedia.com/terms/i/ichimoku-cloud.asp

##### *Initial lot size:*
-  the size of the first order. If the Martingale multiplier is greater than 1, this value will be increased using the value of the Martingale Multiplier. If the Martingale Multiplier is set to 1, the Initial lot size will also be used as size for the following orders.

##### *Grid Trading:*
- you can switch on/off Grid Trading True or False. if this function is turned off, the EA will transform into a single entry EA.

##### *Martingale multiplier:* 
- it defines the multiplier used by the EA to increment the lot size of the orders after the first one. Set it to 1 disable the increment and the EA uses only the Initial Lot Size value

##### *Maximum Lot size:*
- when martingale lots has exceeded the Max Trade value, it will enter the Max Lot size value instead. This is just a simple solution to the uncontrollable martingale lot sizes.

##### *Take Profit & Stop Loss in pips:* 
- these two values specify the amount of pips the EA uses to calculate the Take Profit and the Stop Loss (if configured)

##### *Minimum/Maximum Distance Between Orders:*
- these two value define the distance between orders, from a minimum value to a maximum. If you see the Max Distance to 10 pips, it will stop increment at 10 pips current distance.

##### *Distance Increment Between Orders:*
- this will increase the distance between order settings for the 3rd layer, 4th layer and so on. 

##### *Max Trade:*
- this value tells the EA what is the maximum number of orders it can open in one direction.

##### *Automatic Config AI:*
- this is an AI. It will automatically adjust the best configuration for any pairs you are using. Turn this on and see the magic.

#
### Authorized account list:
please use CTRL+F shortcut to search for your account number.
> 120201094, 51407995, 231088399, 231080470, 231080474, 38003230, 2100200249, 192139837, 231074929, 339376, 339176, 231067931, 320321354, 231065509, 220748121, 24368645, 24368642, 24368628, 24368617, 141136159, 192080160, 192080166, 192087997, 192080154, 290729490, 220734699, 6748098, 290768531, 301326664, 301326668, 310359156, 301329698, 750729, 13027894, 13527690, 301329704, 301329710, 10576779, 56120025, 310402183, 320323525, 301329718, 320287929, 320287926, 300724432, 301329724, 38000971, 320305818, 320287928, 320287930, 290797780, 320293256, 999049102, 189402, 187461, 1000012579, 192079962, 46002444, 47074913, 301329729, 5015555, 10574113, 10574122, 2100199368, 2100102903, 301370702, 301364931, 301364963, 301363842, 22668478, 117043700, 271619370, 271619248, 271619247, 271619242, 169745, 301342826, 5103852, 10572601, 301338471, 301340934, 2100127831, 301338667, 301338700, 301338711, 60127544, 241334311, 301333295, 21327810, 62630015, 290811032, 290811144, 35124407, 226727, 271376212, 271589085, 290793203, 290803005, 290803011, 290803023, 290803031, 290803035, 290803042, 290803045, 290777186, 290777238, 5793561, 290797783, 280428807, 290708505, 290708508, 10565339, 22642646, 60124625, 290793095, 290776570, 290778420, 290791966, 290791971, 290791974, 290791975, 290791976, 290791978, 290791980, 290791982, 290790446, 60127270, 290783307, 50893152, 60127243, 9106202, 4561741, 766118, 290779891, 290777138, 4561464, 24333650, 271705126, 271702365, 271702356, 271701961, 271701959, 271701950, 271700614, 271700604, 271700600, 271698838, 58808192, 22620250, 22619162, 60126730, 271680740, 65209315, 60126358, 53409128, 2875737, 5711440, 5711469, 15769428, 112883, 271670101, 271663568, 250972252, 250979131, 4559342, 250972252, 3754760, 3754799, 60126208, 250966681, 250973804, 250966081, 800837865, 271628286, 260657559, 56105041, 250959657, 56105041, 250957659, 35055890, 2100198278, 2100198280, 2100197940, 250953184, 250951695, 250950477, 250949189, 56104289, 363317, 250937747, 2100198277, 330231524, 1149678, 5767394, 5618549, 60125487, 117017757, 220579967, 60124536, 13025770, 330226965, 60124742, 2100197910, 13025412, 5000445, 5763809, 60124966, 60124932, 5763058, 330215114, 330215118, 330215126, 5762992, 330213208, 13024948, 330212436, 60124502, 362926, 548188, 13024780, 290448830, 320247513, 5670568, 60124670, 280755909, 21454957, 53379729, 13024449, 13022238, 10565339, 60124033, 5527955, 5527967, 5586556, 5586494, 5586473, 5586460, 5585377, 60124032, 108151, 280742519, 280742542, 3751953, 280734909, 1148217, 5753815, 571958, 571729, 260753046, 260756315, 280730787, 280730796, 5585003, 13022980, 320207539, 46175797, 260764032, 260762646, 260758710, 310307023, 3957871, 5743926, 5434951, 241612110, 241612108, 27362937, 241612106, 241612105, 241612104, 241612103, 241612102, 241612100, 241612096, 241604510, 5742489, 241605261, 241617296, 443354, 22546495, 13021463, 13004694, 241591851, 290748564, 800833896, 241606464, 241605554, 231047192, 290589021, 241599814, 241599469, 13020888, 90307343, 90876405, 241598720, 241598716, 241598721, 241598555, 241598558, 241598559, 241596128, 231052121, 230942650, 241587481, 241587697, 241586738, 44094296, 5522658, 686468, 35050856, 330023862, 5724392, 220093895, 24110069, 47055958, 24390748, 220683034, 20890279, 231041409, 220670829, 231040169, 5711441, 290505538, 10565339, 51194337, 310200794, 231038313, 55006805, 231037934, 8963723, 88014706, 4457412, 6336708, 360439, 20314776, 890367718, 8002244, 5727022, 5727021, 5727019, 5727018, 5727017, 5724676, 5724673, 5724670, 5713913, 5713912, 53338904, 231036521, 10569792, 10569822, 10569823, 10569824, 10569825, 260675215, 3748617, 330032453, 220708708, 10570144, 10570145, 10570146, 10570181, 220680918, 220694255, 220703637, 10570143, 10569437, 46071377, 220698139, 290636244, 220696924, 310364137, 310364161, 320243283, 310367068, 220695974, 10569792, 220694810, 220694807, 220692136, 220692127, 10569667, 46070806, 220691140, 250852939, 438088, 220689347, 20829806, 220689025, 220689151, 241501008, 437814, 271557181, 250280548, 437834, 10568483, 90865412, 320183680, 220683034, 21398598, 229488, 46069257, 220680804, 220678889, 310390721, 220677774, 320258092, 10568801, 320236039, 5611439, 310360242, 310393621, 330179201, 5711441, 330019766, 310390036, 52133589, 310387193, 310382563, 310381317, 310362509, 310380447, 22224590, 5714333, 5713913, 5713912, 4558630, 5713692, 435807, 4558456, 310373184, 320239407, 22224590, 320206708, 320206716, 320206723, 320206732, 4558004, 310371777, 260600979, 5711107, 310364286, 33126040, 90866470, 5434953, 301318199, 310361207, 310360465, 435036, 310360389, 320259320, 310360242, 4557465, 310359156, 789012, 345678
#

### **HOW TO GET AUTHORIZED::**                                 

I lock the EA by account number for my client who is registered under my broker link only.  recommended account cent, laverage max.  minimum 100usd. 

CXM:
https://secure.cxmdirect.com/links/go/5062
Partner ID: 5062

fbs: https://fbs.partners?ibl=1869&ibk=BuBat. 
Partner id: 588292. 
Support: support@fbs.com

forex4you: https://account.forex4you.com/en/user-registration/?affid=4hcnvz4.
Partner code: 4hcnvz4 

GMI: https://gmi-ma.biz/my/accounts/register/?ae=MY004&ib=GMP01583
IB Code: GMP01583 

APX:
https://secure.apxprime.com/links/go/340
IB Code: 340

OctaFx
Link: https://my.octafxmy.net/change-partner-request/?partner=246630
Referral ID: 246630
Support: support@octafx.com 

InstaForex
Link: https://www.instaforex.com?x=KUSD
Affiliate code: KUSD
Support: support@instaforex.com 

LiteForex:
https://www.litefinance.com/?uid=805161060 
Partner UID: 805161060
Support: clients@litefinance.com

RoboForex:
https://my.roboforex.com/en/?a=mxyg 
Affiliate code: mxyg

Exness : 
https://one.exnesstrack.com/a/si0kd90q
IB number : 8666845 
Support: support@exness.com

Please select a broker that you have never registered.  tell me the trading account number after registering.  I will share the EA update file, and for fbs and forex4you clients you will get spread rebate of 50% of the commission that I get based on your total trade lot once a week.  Clients who have registered through my link can just PM the trading account number to me https://t.me/SyariefAzman.
#
### HOW TO INSTALL AN EA ON MT4:
[![Watch the video](https://img.youtube.com/vi/leH9PGkLc6Q/hqdefault.jpg)](https://youtu.be/leH9PGkLc6Q)
#
### **UPDATE LOGS::**

#### EA Budak Ubat v1.61
```
What's new:-

Analysis Method: the FIRST position will follow this analysis method.

Grid Trading: you can switch on/off Grid Trading True or False. if this function is turned off, the EA will transform into a single entry EA.

AutoConfig: this is an AI. It will automatically adjust the best configuration for any pairs you are using. Turn this on and see the magic.
```
![EA Budak Ubat v1.61](./screenshot/v1.61.png)
#

#### EA Budak Ubat v1.60
```
what's new:-

Position Mode :- 
you can set it up to buy only or sell only mode

buy only -  the ea will only buy
sell only - the ea will only sell
buy and sell - the ea will buy and sell.

if hedging is false while in the buy and sell mode, it will enter only one way but it will decide whether to buy or sell based on the first candle close. if it is bullish it will buy, if it bearish it will sell. whichever comes first.

Maximum Lot :- 
when martingale lots has exceeded the Max Lot value, it will enter the Max Lot value instead.this is just a simple solution to the uncontrollable martingale lot sizes.
```
#

#### EA Budak Ubat v1.58
```
what's new: 
 
Execution Mode:- 
 
on Every Tick - the EA enter trades immediately when attached and also enter new layer immediately when the distance between order setting is met. 
 
on New Bar - this is the classic EA Budak Ubat entry style. it enter trades only after new candle appear. it will still follow the distance setting for the new layer. but only enter trades after the candle closed. 
 
Distance Increment:- 
 
this will increase the distance between order settings for the 3rd layer, 4th layer and so on. 
 
Max Distance:- 
 
this is the max distance between order. if you set it to 10 pip, it will stop increment at 10 pips current distance. 
  
- bug fixes on new bar function 
- MaxTrade is now separated for buy and sell in hedging true
```
#

#### EA Budak Ubat v1.56
```
This are just update on bug fixes and added Max Trade parameter.

account that already registered can use this file and it will be no expiry. only contact me to get the update if the expiry Alert pop up.
```
#
#### EA Budak Ubat v1.55 
 ```
Here is the summary of how this EA works: 
 
 • When the EA is active, it will analyze the chart on every new bar 
 • If there are no existing positions on the chart, the EA will enter a trade based on the candle. If the candle is bullish, it will enter a buy trade and if it is bearish it will enter a sell trade. And it will also set a Stop loss order at a certain distance from the opened trade price if the stop loss variable is greater than 0. 0 means no stop loss. 
 • If there are existing positions on the chart and the last one is in loss, EA will check if the distance between the current market price and the order is at least the minimum distance set by the user, and then it will enter a trade based on the candle, lot size will be calculated using the martingale method, and will set a Stop loss order at a certain distance from the opened trade price if the stop loss variable is greater than 0. 
 • If Hedging is set to false, the EA will only enter trades in one direction at a time. If the first position is a buy trade, all subsequent martingale positions must also be buy trades. If the first position is a sell trade, all subsequent martingale positions must also be sell trades. If Hedging is set to true, the EA will enter trades in both directions. 
 • The EA will modify the take profit of all positions in the same direction to a single break-even point plus the take profit level set by the user. 
 • The EA will stop working and will display an alert message if the EA has expired. 
```
#

## Author

- Github - [Syarief Azman](https://github.com/syarief02)
- Telegram - [@SyariefAzman](https://t.me/SyariefAzman)
- Twitter - [@SyariefAzman](https://www.twitter.com/SyariefAzman)
