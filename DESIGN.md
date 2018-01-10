# Design Document

## APIs, Frameworks and Plugins
UIKit-library . 
Firebase-library . 
Charts .  

## Data Sources
[Firebase Database: project-528131060307](https://coinscraper-55bab.firebaseio.com) for storing all coinnames and their indicators.
The data originates from [Coinmarketcap Website](www.coinmarketcap.com/) and the [Github API](www.github.com/).
The data will be implemented through Google's own Firebase module for swift. The data will only be represented as dictionairies, so some data will be converted to more logical formats. Commits per week and Tradevolume per week wil be converted to an array for example. The coins will be stored in their own custom struct. All coins will go into an array of this struct type. 

## Database details
The Firebase database is set in a Parent<->Child format made up of dictionairies. 
The children of the root are all the coinnames. Each coinname then has a field for: All tradevolume and commits per week in a list under the children "volume" and "commits".
Each coin also has two other children called "commitschange12weeks" and "volumechange12weeks" that show the change in value in the past 12 weeks in relation to the prior year.

## Diagram of modules, classes and functions

| ImportDatabase| 
| ------------- | 
| Fir.database  | 
|               | 
| dictToStruct()|
| dictoToArray()|

| UserAddsCoin  | 
| ------------- | 
| coin object   | 
|               | 
| saveuserdata()|
| appendcoin()  |
| table.reload()| 

| CoinDetails   | 
| ------------- | 
| CoinStruct    | 
| CommitArray   |
| VolumeArray   |
|               | 
| Grafiek()     |
| UserAddsCoin()|

## Advanced sketches
![Alt text](https://github.com/swcloud1/CryptoAnalyzer/blob/master/docs/advanced.png "Optional title")
