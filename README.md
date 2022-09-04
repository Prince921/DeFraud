# DeFraud

## Inspiration

Recently, Valve founder Gabe Newell banned NFTs from Steam, citing 'out of control fraud.' (https://www.forbes.com/sites/paultassi/2022/02/26/valves-gabe-newell-takes-a-flamethrower-to-the-metaverse-and-nfts/) Blockchain technology is can be an important democratizing tech in enterprise computing. However, its lawless nature leads to many scams and fraud. Detecting this fraud can allow blockchain technology to spread into new sectors by helping to reduce the possibility of scams and make people more trusting of blockchain.

## What it does

Our system consists of a live feed on the DeSo blockchain that makes a post whenever a transaction is suspected to be fraudulent. The live feed is summarized in a web app that summarizes the state of DeSo coin and displays what transactions are happening on the blockchain.

## How we built it

- Many REST API calls to the DeSo python library to get transactions. usernames and calculated average amount transferred, min money going in/out, max money going in/out, etc. These calls are used to collect data for our machine learning model to detect whether or not a transaction is fraudulent.
-  Machine learning logistic regression model using scikitlearn that was trained on a dataset of ethereum transactions that contained known scams and frauds. Class imbalance in the dataset was addressed by using the SMOTE algorithm to oversample fraudulent transaction.

## Challenges we ran into

- Reverse engineering blockchain exploration API calls due to lack of proper/clear documentation from Deso.
- We ran out of DeSo credits
- We were not familiar with web3 and DeSo blockchain. We had to intensively look through the documentation but even then it took time.
- Front-end web development is not our strong skill.
- Many of the DeSo examples, such as the guide on how to run a node, did not have functioning code
- Our computers were not powerful enough to run DeSo nodes


## Accomplishments that we're proud of

- We received plenty of engagement from the community
- We employed machine learning to classify fraud with approximately 80% accuracy
- We were able to record our data on the blockchain and provide an interesting way to view the data

## What we learned

- DeSo is a very interesting blockchain seeking to decentralize social media, but it's not without cost
- If you repeatedly @ people on social media, they will consider it spam
-  When you are making software that interacts with the public, you should develop it in a test environment rather than in the production environment(in this case the mainnet of DeSo)
- Utilizing tools to make web-app, bots, and machine learning models

## What's next for Defraud

Cloud integration will allow DeFraud to continue monitoring fraudulent transactions 24/7. The project can also be used on other cryptocurrencies, such as Ethereum where there are more transactions to monitor. In addition, one idea we had was to create a crypto-reputation system where accounts found to be involved in many scams and frauds would lose reputation and have their account flagged in a dApp where people can verify that they aren't going to lose their crypto unfairly.
