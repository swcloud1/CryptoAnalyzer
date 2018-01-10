# CryptoAnalyzer
Using a combination of webscrapers, APIs, custom algorithms and databases to look for CryptoCoins that are likely to increase in value over time.

# Problem Statement
Cryptocurrencies are the biggest hype in the world right now. There are thousands of different coin, each with their own promises and unique selling points. The problem is that each not a lot of markers are used to displayed how big the chance of the coins' success are. And even if there was, everyone would be using those markers, thus intervening with its effects.

# Proposed Solution
Using multiple custom webscrapers and APIs, indicators of a coins success are created and uploaded to a Firebase database. This database is used for the IOS app, in which all coins will be shows in a table, and the user will be able to sort the list by there preferred markers. The custom markers will be displayed alongside other markers in a graph. 

If enough time is left, users will be able to register and add certain coins to a watchlist. 

# Functies van CryptoAnalyzer (nog vertalen naar engels)

- Zie ontwikkelaarsactiviteit en volumehandelverandering voor alle cryptomunten in 1 overzicht

- Bekijk een grafiek van het verloop van deze waarden t.o.v elkaar en als functie van tijd

- Sla een cryptocoin op en voeg deze daarmee toe aan een persoonlijke volglijst

- Exporteer/Deel je eigen lijst met anderen via populaire messaging platformen

## Data Sources
The original data sources are Coinmarketcap.com(a site that indexes all cryptocurrencies) and Github.com.
The data will be modified fairly heavily. Repositories and commits will be analyzed for trends for each coin. Coinmarketcap is used as a source for the Github URL for each coin. It is also used to get the tradevolume for each coin for the past 52 weeks.

After the data is modified and the new data is calculated, all data is uploaded to a Firebase database. This database is then used as the primary source for the IOS App. Seeing as this might technically count as using a single database, a second Firebase database will be used to allow for user registration. 

[Coinmarketcap](www.coinmarketcap.com/)
[Github](www.github.com/)
[Firebase](firebase.google.com/)

## External Components
Firebase will need to be implemented in the IOS app. [Firebase](firebase.google.com/)
(Python is the primary language for creating the back-end, but it probably doesnt count seeing as creating a custom back-end was not part of the assignment.)

## Similar Apps
In here lies the beauty of the CoinAnalyser. An app that allow for finding potentially profitable coins using markers doesn't exist. There are websites that do something similar. [Tradingviewer](https://www.tradingview.com/markets/cryptocurrencies/quotes-all/) for example sorts cryptocurrencies in a table and list markers used in the Stock and Currency trade to give an advice. There are apps that show all cryptocurrencies. [BlockFolio](https://www.blockfolio.com/) for example. They use a Tableview and a new viewcontroller to display details for each app. CoinAnalyser will also use this principle. 

## Hardest Parts
The Hardest part of this project is getting the back-end fully functioning. Seeing as this is not a requirement of the assignment, it does not count. The hardest part in creating the app is creating a graph for each Coin using the IOS Framework that displays multiple values in a easy to view manner. An other difficulty might be keeping the app quick, responsive and fun to use, whilst displaying 800+ unique tablecells. Though this hasn't been tested yet. 

# Mockup Images
![Alt text](https://github.com/swcloud1/CryptoAnalyzer/blob/master/screenshot.png "Optional title")
