---
author_info:
  image: images/author/vicky.jpg
  name: Vicky Wu
date: "2021-07-13"
draft: false
image: images/blog/stock.jpg
title: Order Driven Markets
---

One of the main types of markets is an Order Driven Market. This can actually have many names including: Auction Market or Limit Order Market.

An Order Driven Market features a centralized and direct access to an auctioneer which will execute and match opposing orders with each other.

To understand Order Driven Markets, let's first take a look at the different types of orders a market participant can place:

![Order Types](images/ordertypes.jpg)

Order Driven Markets can be further split into two different markets: Call auctions and continuous auctions.

## Call Markets

A call or batch auction allows market participants to place orders for a certain period of time. Buy orders are arranged by decreasing price and sell orders by increasing price. These orders may overlap and are not executed until the specified time of the call market known as a **call.**

![It's Call time!](images/whistle.jpg)

Once a call occurs, a price is determined that equalizes supply and demand. Commonly, this will be determined by maximizing the trading volume and secondly minimizing the net order imbalance. This is known as the **IEP** (Indicative equilibrium price). All buy orders greater than this price and all sell orders less than this price are executed against one another.

![It's Call time!](images/callmarket.jpg)

As you can see, there is part of the book that is overlapped. From there, we can tell that the IEP will be 100 as the most volume will trade at that price. Buy orders above this will execute against sell orders below this value. After all shares are executed, there is extra quantity on the sell side of 50 shares. This will become the best ask at 100 with 99 becoming the best bid.

But what happens to the remaining orders? If this is the first call during the day, open orders may be placed into the limit order book, also known as the continuous market to be described in the next section. If it is the final call, outstanding orders will be expired back to the client.

## Continuous Market

Unlike Call Markets, Continuous Markets also known as Order Driven Markets, allow market participants to place orders and execute them while the market is open. Participants can place any type of order specified in the Order Types section which will interact differently with the Limit Order Book.

Let's take an example where the bid (buying price) is 99 and the offer (selling price) is 100.

![It's Call time!](images/contmarket.jpg)

If another limit buy order is placed at or below \$99, it will sit passively on the book and join the back of the queue. Similarly, if a limit sell order is placed at or above \$100, it will also sit passively on the book. However, if a buy market order is sent or a limit order with price greater than 99, it will execute against the 500 sell side shares at \$100. This is known as a marketable order.

Execution is determined by priority rules.

1.  Price priority will always occur first where the highest bid price and lowest ask price will execute first
2.  At a single price level, the execution of different orders can be determined by
    1.  Time priority - Earliest placed orders execute first
    1.  Size priority - Largest orders execute first
    1.  Pro-rata allocation - Executions are calculated as a percentage of their total volume
    
