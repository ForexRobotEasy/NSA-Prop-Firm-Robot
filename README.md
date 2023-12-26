# NSA Prop Firm Robot

## Developer: Forex Robot Easy Team
## Developer's Site: [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/nsa-prop-firm-robot-review-conquer-trading-with-expert-ea/)

---

This is the source code for the NSA Prop Firm Robot, developed by the Forex Robot Easy Team. This expert advisor (EA) is designed to automate trading in the forex market.

### Input Parameters

- `LotSize` (double): Trading lot size.
- `StopLoss` (int): Stop loss in pips.
- `TakeProfit` (int): Take profit in pips.
- `UseNewsFilter` (bool): Flag to enable news filter.

### Global Variables

- `g_magicNumber` (int): Magic number for trade identification.

---

## Detailed Description

The NSA Prop Firm Robot is an expert advisor that automates trading in the forex market. It uses a combination of technical analysis and news filtering to place buy and sell orders on specific currency pairs and commodities.

### Expert Advisor Initialization Function

The `OnInit()` function is called during the initialization of the expert advisor. In this function, the trading hours are set using the `SetTradeTime()` function. If the news filter is enabled, the `InitializeNewsFilter()` function is called to initialize the news filter.

### Expert Advisor Start Function

The `OnTick()` function is called on each tick of the price data. In this function, the expert advisor checks if it is the right trading hour using the `IsTradeTime()` function. If it is not the right trading hour, the function returns.

Next, the expert advisor checks if there is any high-impact news event occurring using the `IsHighImpactNews()` function. If the news filter is enabled and a high-impact news event is occurring, the function returns.

The expert advisor then checks if the current symbol is either AUDCAD or NZDUSD. If it is not, the function returns.

After that, the expert advisor checks if the symbols for Gold (XAUUSD) and US30 are available for trading using the `SymbolIsAvailable()` function. If either of the symbols is not available, the function returns.

If all the conditions are met, the expert advisor places a buy order for Gold and a sell order for US30. The stop loss and take profit levels are calculated based on the input parameters. The orders are sent using the `OrderSend()` function.

Finally, the expert advisor checks if the orders are successfully placed and prints a message accordingly.

### Utility Functions

- `IsTradeTime()`: Checks if it is the right trading hour based on the current time.
- `IsHighImpactNews()`: Checks if a high-impact news event is occurring.
- `InitializeNewsFilter()`: Initializes the news filter.
- `SymbolIsAvailable(symbol)`: Checks if a symbol is available for trading.

---

**Note**: ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please refer to the [MQL5](https://www.mql5.com/) website.

For detailed reviews and trading results of this product, please visit the [NSA Prop Firm Robot Review](https://forexroboteasy.com/forex-robot-review/nsa-prop-firm-robot-review-conquer-trading-with-expert-ea/) on the Forex Robot Easy website.
