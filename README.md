# OWBProject

This repo contains Open World Builders project to be delivered on August 28, 2020 by group #20 Jared, JeanClaudel, Hendrik

#Product
##Mission Statement:

Everyone has an identity in life, everyone is a unique individual.  A Photo turned NFT to represent, reaffirm, and foster this concept of value is gratifying, fun, and establishes an inherent concept that others are unique individuals as well. A photo, minted into a NFT(s) of individuals has value, and after entering NiFTree, has scarcity!
The Family Tree Photo concept is a beginning, a baby step towards a larger, much larger plan of inclusion.  Friends, large groups of friends, organizations, clubs, sport clubs and so many others can get in on the action as well!

######Link to recorded presentation on Youtube:
<a href="https://www.youtube.com/watch?v=qpdWmAlYGFc" target="_blank">Youtube Presentation</a>

######Link to Google Slides presentation (Public):
<a href="https://docs.google.com/presentation/d/1_uZHEz2w2oEb2xmsR_WvHk7nTEpayRAXm8VWkMNoUhU/edit#slide=id.g92384450cf_3_212">Presentation Slides</a>

##Use case/Summary Overview:

The problem we are trying to solve is large social media corporations are gathering data on users and using and/or selling persons photographs and pertinent data at their profit. We hope to solve this problem, by bringing value back to the Photographers.  With a NiFTree the user gets to keep photos, store them and trade them and build photo albums, and they have value.
    Identity Value
    Monetary Value (Trade, Sell, Gift)
A sense of being an individual with a stake, share, in something bigger.
This appeals to all our natures, people want to be recognized as an individual, and also want to belong to something, some group that has meaning, focus, fun!

##Methodology:

Build a smart contract using Cadence > using Resources and Mint a NFT of a Photo(s) and resend to Member (Photographer) for storage. (NonFungibleToken.cdc)
  (A family Member or Photographer sends Photos to a Publisher (NiFTree) for minting and recieves a Framed Photo)
  (The color of the Frame will denote scarcity)
Establish collections of pictures via transactions to trade, share, and contain (store) and add to a Photo Collection, or Photo Album.
When a Photo Album is created and multiple members have completed and shared, a group vote for best of show takes place.
Winner recieves special (diamond) Framed Photo.

Current Limitations:
Product - Marketing, Established Competitors, Onboarding Test Markets, Proof-Of-Concept
Technical - Updating NFT's and Technologies (Database, Servers, Languages and Frameworks)

Future Additions:
Competitions (ex. America's funniest home videos, Family/Community Competitions for Summarizing a Years Moments, Community/Global Competitions for moments of Families vs Families, Best Top Shot Dunks of 2020 Season, Biggest Loser for Health Crossing Dapp, Artist Competitions for Competition Photoframes)
Moment Frames - Adding value to incentivize engagement 
Connection to companies
Scarcity - Bronze, Silver, Gold, Platinum, Diamond
Marketplace


How to deploy/run
TODO 
Link to Wireframe: Our Demo Link


Future Additions

Create community to facilitate peer to peer encouragement and habit focused micro-communities
Automated Avatar updates - e.g. press an action in app which updates profile pictures live
Investigate Avatar standards e.g. can we have a central Avatar identity across platforms
Create a Flow-based NFT marketplace for collectables
Building community of designers and Avatar designer developer kit
Technical
Demo
https://play.onflow.org/4d94b80c-62d7-45b2-89fc-cba2c8b3fbdf

Deploy HealthCrossingCore to 0x01
Setup any account missing an Avatar with txn 1_setup_account
Ensure you see an Avatar in your resources window
Update an account's health stats with txn 2_update_avatar_progress
See that your Avatar stats have been updated and also with new NFTs. Note: A Playground bug exists that may set your Avatar to null. GH#54.
The repo itself contains 4 directories: api, smart-contracts, infra, and web.

api
The api dir is not a true API, but has a local dataloader that ingests Apple HealthKit data in CSV form. It successfully marshals the data into stable data structures. It is still missing the steps that creates a new wallet for an account and runs the two relevant transactions setup_account.cdc and update_avatar_stats.cdc.

Future state: Create the necessary endpoints for user onboarding and user interactions for Health Crossing transactions.

smart-contracts
Playground: https://play.onflow.org/4d94b80c-62d7-45b2-89fc-cba2c8b3fbdf

The smart-contracts is the core Cadence contracts.

Future state: Create a robust progression system and CRUD APIs for the varying NFTs. Our work is heavily dependent on unique creations of avatar outfit NFTs.

infra
The infra dir uses the AWS nodejs CDK to create an infrastructure stack on AWS. At the moment it only deploys an S3 that stores users' HealthKit data in CSV format.

web
The web dir is still a barebones NextJS project. The initial goal was to create an onboarding UI for users to create their avatars, see their avatars, and update their avatars. Frankly speaking, it may be better to start with a native mobile app to read data directly from users' HealthKit store.
