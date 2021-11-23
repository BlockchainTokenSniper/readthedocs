Welcome to the BlockchainTokenSniper documentation!
===================================

**BlockchainTokenSniper** is a set of tools written in Python to snipe tokens on the BSC, ETH and Polygon blockchains and sell later to make a profit.

This project is currently in Beta and only the BSC blockchain is supported at the moment (BSCTokenSniper), but ETH and Polygon will be supported in the future.


<!-- ABOUT THE PROJECT -->
## About The Project
BSCTokenSniper is a completely free collection of 2 tools (BSCMultiSniper and BSCLaunchSniper) programmed in Python and Web3 which aim to automatically buy newly listed tokens and auto sell tokens when profitable.

BSCMultiSniper detects new tokens as soon as liquidity is added. It will check if it is not a scam and if not will buy it. It will then monitor the price of the token and auto sell at the specified profit margin (eg. 1.5x, 2x, 10x etc).

BSCLaunchSniper allows you to snipe new token launches paired with any token (eg. BNB, BUSD). It has the ability to mempool snipe and will instantly buy when liquidity is added. It constantly updates the price and shows you the profit you've made, has the ability to autosell at a specified profit margin (eg, 2x, 10x etc) and also allows you to sell manually with your keyboard. You can use the spacebar to sell 100% of your tokens or use keys 1-9 to sell 10-90% of your tokens.

BSCLaunchSniper features:
- Programmed in Python so can support a wide variety of systems
- Either use mempool sniping (wait for liquidity to be added) or buy as soon as token address is entered
- Auto sell (either manual with hotkeys or automatically with autosell multiplier eg. 2x profit)
- Stop loss
- Honeypot repeat checker (repeatedly checks the token until it is available for trading / isn't a scam)
- Sniping with BNB or other liquidity pair eg. BUSD, USDT
- Partial sell (eg. sell 10-90% of tokens with hotkeys then sell the rest later)
- Configurable anti-bot delay
- Easy to use config file to change wide variety of settings eg. wallet address / private key, gas price / limit, node URL, liquidity pair address etc
- Price updates multiple times a second showing profit multiplier (eg. 1.5x, 2x), current value of tokens and profit percentage

 The multisniper is able to check if:
 - Token is a honeypot
 - Token's buy/sell fees are too large
 - Token has any scams / exploits in code
 - Token's code is verified
 - Token's ownership is renounced
 - Token's liquidity is locked

The user can decide whether to enable the mini audit or turn it off (bear in mind you will likely be investing in a lot of scams / rugpulls / honeypots if you don’t).
Once the token has/hasn't been through a mini audit the bot will then attempt to buy X amount of tokens with the specified amount of BNB.
The bot will buy the tokens directly through the Binance Smart Chain using the PancakeSwap v2 router and factory address, so it is much quicker than the PancakeSwap web interface.

By avoiding web interfaces & Metamask and directly with nodes you can snipe tokens faster than any of the web-based platforms. This allows tokens to be sniped almost instantly. During our testing we found the bot would typically be within the first 3 buy transactions of all tokens it finds.
The bot buys the tokens using the user's wallet address and private key. This information is kept secure, is only stored locally on your computer, and is only ever used to buy tokens.

The bot does not incur any additional fees except from the dev fees on profit made, only fees are BSC / PancakeSwap gas fees.

The bot's source code is heavily obfuscated and compiled to prevent people stealing code and scammers trying to bypass this system as this has happened before. If you have concerns about the security of this bot then you should create a new wallet with a small amount of BNB and use that wallet's details in the config file. If you make a profit then that can be transferred to your main wallet. You can also use a virtual machine if you like. Another reason the code is obfuscated is that it prevents people from ripping off the code and trying to make / promote their own bot which would cause the developers to lose out on income, and preventing people from disabling the dev fee as alot of effort has gone into making this bot.

How do the developers make money? What are the fees?

- From v1.4 onwards, the bot will have a 10% tax when profit is made: both bots will have a sell fee of 10% of profits made. The fee is only sent when profit is made and there is no dev fees if you break even or lose money. This allows us to offer everyone the bot free of charge, as most people do not want to pay hundreds or thousands of dollars for sniper bots that they can't even trial first. The fees made massively support the project and allow us to test out new features.
 
© Copyright 2021 - any attempt to sell, modify, decompile, copy or replicate this code is strictly forbidden and will result in legal action being taken.

### Built With

This project is built with:

* [Python3.9](https://www.python.org/downloads/)
* [Web3](https://web3py.readthedocs.io/en/stable/)
* [Keyboard Module](https://pypi.org/project/keyboard/) (for launch sniper)

