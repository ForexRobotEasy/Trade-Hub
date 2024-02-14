# Trade Hub - Forex Trading Tool

This code is a sample implementation of a Forex trading tool called Trade Hub. It allows traders to open and close trades with one click, calculate lot sizes based on risk percentage, and automate certain trading processes.

## How it Works

The code utilizes the MQL5 language and includes the necessary libraries to execute trades. Here is a breakdown of the main functions and variables:

### Global Variables

- `riskPercentage` (double): Represents the percentage of risk for each trade.
- `isAutomatedLots` (bool): Determines whether to use automated lot sizes or fixed lot sizes.

### Function `OneClickTrade()`

This function is responsible for executing a trade with one click. It performs the following steps:

1. Retrieves the current symbol and timeframe.
2. Calculates the appropriate lot size based on the risk percentage.
3. Opens a buy trade with the calculated lot size, entry price, stop loss price, and take profit price.
4. Waits for a certain time (in this case, 5 seconds).
5. Closes the trade using the `CloseOrder()` function.

### Function `CalculateLotSize()`

This function calculates the lot size based on the risk percentage, account balance, account equity, and stop loss value. It takes the following parameters:

- `accountBalance` (double): The current account balance.
- `accountEquity` (double): The current account equity.
- `stopLoss` (double): The desired stop loss value.
- `riskPercentage` (double): The desired risk percentage per trade.

The function returns the calculated lot size.

### Function `CloseOrder()`

This function is used to close an open order. It takes the following parameters:

- `ticket` (int): The ticket number of the order to be closed.
- `price` (double): The current price of the symbol.
- `comment` (string): A comment to be attached to the order.

The function checks if the order ticket is valid and then attempts to close the order at a specified close price.

### Function `OnInit()`

This function is executed when the Expert Advisor is initialized. It initializes the Trade library and creates a button on the chart for one-click trading.

### Function `OnChartEvent()`

This function is called when a chart event occurs. It checks if the button on the chart is clicked and, if so, executes the `OneClickTrade()` function.

### Function `OnDeinit()`

This function is executed when the Expert Advisor is removed from the chart. It deletes the button from the chart.

## Product Description

Trade Hub is a powerful Forex trading tool that enhances trading efficiency and simplifies the trading process. It provides traders with the ability to execute trades with just one click, calculate lot sizes based on desired risk percentages, and automate certain trading actions.

Key Features:
- One-click trade execution: Easily open and close trades with just a single click, saving time and effort.
- Automated lot sizing: Utilize automated lot sizing based on risk percentage, account balance, and stop loss value for optimal risk management.
- Customizable parameters: Adjust various parameters such as risk percentage, stop loss, and take profit to adapt the tool to your trading preferences.
- Chart integration: The tool seamlessly integrates with your trading chart, providing a user-friendly interface for quick and efficient trading.

Please note that ForexRobotEasy is not the official developer of this product. We are showcasing this sample code to demonstrate the functionality described in the product. For detailed reviews and trading results of the official Trade Hub product, please visit [Forex Robot Easy - Trade Hub Review](https://forexroboteasy.com/forex-robot-review/trade-hub-review-enhance-forex-trading-with-cyber-capitals-software/). To find the official developer of this product, please refer to the MQL5 platform.
