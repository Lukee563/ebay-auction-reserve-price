# eBay Auction Reserve Price Analysis

Empirical analysis of reserve price effects on auction revenue using eBay bid-level data,
with connections to Myerson's optimal mechanism.

## Research Question

Does the seller's opening bid (reserve price) affect final auction revenue, and is the
observed effect consistent with Myerson's optimal reserve price prediction?

## Data

eBay auction data from the companion dataset to *Modeling Online Auctions* (Jank & Shmueli,
Wiley, 2010), sourced via Kaggle. Covers four item categories across two auction formats.

- **Items:** Cartier wristwatches, Palm Pilot M515 PDAs, Xbox game consoles, Swarovski beads
- **Formats:** 3-day and 7-day auctions
- **Key variables:** `auctionid`, `bid`, `bidtime`, `bidder`, `bidderrate`, `openbid`, `price`,
  `item`, `auction_type`

> Raw data is sourced from Kaggle: https://www.kaggle.com/datasets/onlineauctions/online-auctions-dataset

## Analysis

1. **Descriptive**: Bidding dynamics by item category and auction format
2. **Revenue Regression**: Effect of opening bid on final price, controlling for item,
   duration, number of bidders, and bidder rating
3. **Structural**: Back out implied buyer valuations from the bid sequence and compare
   observed reserve prices to the Myerson optimal benchmark

## Project Structure
```
ebay-auction-reserve-price/
├── data/               # Raw data
├── notebooks/          # Exploratory analysis
├── src/                # Analysis scripts
├── output/             # Figures and tables
├── report/             # Final report (PDF or HTML)
└── requirements.txt
```
## Requirements
```
pandas
numpy
statsmodels
scipy
matplotlib
seaborn
jupyter
```
