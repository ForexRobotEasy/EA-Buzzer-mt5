# EA Buzzer MT5

EA Buzzer MT5 is an advanced night scalping system for forex trading. This code is a sample implementation of the EA Buzzer MT5 trading strategy. Please note that ForexRobotEasy is not the official developer of this product. We only provide this code as a demonstration of how the product may work.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/review-ea-buzzer-mt5-advanced-night-scalping-system-for-forex-trading/).

## Input parameters

- `seriesCount` (int): Number of series to open
- `lotSize` (double): Lot size for each trade
- `stopLoss` (int): Stop loss level in points
- `takeProfit` (int): Take profit level in points

## Trading function

The `TradeBuySell` function is responsible for opening trades. It takes an `orderType` parameter to determine whether to open a buy or sell order. For each series, it calculates the stop loss and take profit prices based on the current ask price. It then uses the `OrderSend` function to place the order. If the order is placed successfully, it prints a success message. Otherwise, it prints the error code.

## Managing manual orders

The `ManageManualOrders` function is used to perform necessary operations on manual orders. Currently, the function is empty, but it can be modified to modify stop loss, take profit, or perform other operations on manual orders.

## Hedging positions

The `HedgePositions` function is responsible for hedging positions. It loops through all open orders and checks their types. If an order is a buy order, it opens a sell order to hedge it. If an order is a sell order, it opens a buy order to hedge it. The hedging is done using the `TradeBuySell` function.

## Main program

The `OnTick` function is the entry point of the program. It opens new series of orders by calling the `TradeBuySell` function for both buy and sell orders. It then manages manual orders by calling the `ManageManualOrders` function. Finally, it hedges positions by calling the `HedgePositions` function.

Please note that this code is just a demonstration and may need to be adapted to specific trading conditions and requirements. To find the official developer of this product, please use MQL5.
