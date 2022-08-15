---
description: A recap of the July Airdrop and plans for the August airdrop
cover: ../.gitbook/assets/squad.jpeg
coverY: 0
---

# August Notes

## Lessons Learned
We’ve tried to be upfront about the fact that these initial airdrops (especially the very first one) would be highly experimental. In fact, our dapp attempting to do a lot of things which have never been done before on the IC. We’re doing our best to learn from our early mistakes so that we can kick-start a robust and sustainable gameplay economy.

### #1 We Need To Communicate Better
The fact is, with only 5.77% of dSquad Avatar holders scoring more than 0, we should have done a better job reaching out to our community leading up to the MVP (Minimum Viable Product) launch, and we need to prioritize the automatic tracking of more types of IC activity as quickly as possible. 

### #2 Our Missions Feature Had Bugs
We ran into serious issues validating Missions for the Mint/Burn events of our own collection. Seb had to completely rebuild our Mission validation feature during July, but there are still some users being affected and we are actively troubleshooting.

Once fully resolved, Seb will make sure the impacted users will be able to validate the missions they’ve earned. Their Mint/Burn history is not lost so they will still be able to claim the engagement points they deserve.

We believe this bug is due to the exceptions made in the CAP log which distinguish between Accessory vs Material events for minting and burning. Everything we are doing is experimental, so we appreciate your patience when things like this happen.

### #3 We Airdropped Too Many Materials
Going into July, we assumed our material and accessory supply was far too low compared to the amount of users who would be active on the leaderboard. This was based on the total number of Principals with Avatars (5,432), and the [economy design detailed in our documentation](https://dsquad.gitbook.io/docs/earn/economy-design#leaderboard-and-rewards). In addition, many materials lacked enough liquidity in the market to make it possible to mint most of the newly added accessories. The initial supply up to this point was distributed to all the Principals which placed preorders late last year, and many of those assets never made it onto Entrepot.

Since we had no leaderboard history to go off of, we ended up overestimating how much participation we would get from our existing holders. In short, August 2022 is a very different market than when we launched our presale in late 2021.

The result is that anyone who wore even the most basic accessory was handsomely rewarded. So it might be a good idea to participate while competition is still low and we are still making adjustments to build our economy!

### #4 We need to fast-track external rewards
In short, to prevent/limit a downward spiral in floor prices we need to incentivize users to wear accessories by including ICP rewards and NFTs from other collections in the ecosystem.

### #5 We Need To Clarify & Recalibrate The Daily Engagement Score
During July, we enabled a feature to track NFT activity on CAP and automatically add either 0 or 1 Point per day to Avatar holders based on their NFT trading activity. A Principal had to either trade a total volume of at least 1 ICP or trigger a Mint event within the previous 24 hours to qualify for earning 1 Point for that day. Due to the privacy by default nature of the IC, we can only track activity for the 200+ NFT collections which are integrated with both DAB and CAP. 

Unfortunately, we didn’t clearly communicate this with the community or anticipate how few users would to meet these requirements during the entire month. 

Part of this has to do with the limited and inconsistent adoption of DAB and CAP. While over 200 collections are integrated with these resources ([you can see a list on DAB](https://dab.ooo/nfts/)) not all of them choose to fully integrate. For example, we found a top IC project which doesn’t log any Buy or Sell transactions in CAP, and only logs other types of transactions like transfers. Without both DAB (the registry of NFT canisters) and CAP (the provenance of NFT transactions), it’s not possible to track a collection’s activity.

However, the unfortunate truth is that overall NTF trading activity on the Internet Computer is still very low.

## Distribution Plan for 3rd Party NFTs
From August moving forward we will be including NFTs from our vault (gained during past collaborations) in the monthly prize pools. These will not be randomized like materials, but rather go to the top ranking players on the leaderboard.

If you own an NFT collection and would like to include prizes in an upcoming airdrop, please [reach out to us](https://x3ul6-2aaaa-aaaah-abjda-cai.ic0.app/partners).

August prizes for top 25 players (floor prices as of 8/13):
- (1) ICPunk | floor 9.8 ICP
- (1) ICPuppies | floor 2.99 ICP
- (5) ICPCS | floor 2.4 ICP
- (5) Infernal Vampire Colony | floor 1.19 ICP
- (5) Dfinity Space Apes | floor 1 ICP
- (2) “THE” EGGs | floor 0.95 ICP
- (2) Drakon NFT | floor 0.92 ICP
- (2) Mutant Space Apes | floor 0.65 ICP
- (2) ICSnakes | floor 0.6 ICP
- Total Estimated Value = ~41.98 ICP

Rewards will be distributed to the top 25 players on the leaderboard based on the value of each collection’s floor price at the time of the snapshot. Player #1 will get an item from the collection with the highest floor price (most likely ICPunk) and player #25 will get an item from the collection with the lowest floor price. 

Multiple items from the same collection may have different rarities/properties which effect their value but dSquad cannot take on the task of appraising individual NFTs across the ecosystem, so we will distribute items within the same collection based on their mint number (ascending). For example, based on current floor prices we would give out (5) ICPCS to players #3-#7, where the NFT with the lowest mint number would go to player #3, and the NFT with the highest mint number would go to player #7. 

If two players are tied for the same rank on the leaderboard because they have the same combined total of style and engagement points, their position for receiving 3rd party NTFs will be determined by the estimated value (floor price * quantity) of dSquad assets held in their wallets based on current market floor prices.

## Determining the August Material Allocation
Now that we have data from July, we can use the total number of style points earned in the previous month to help us determine the total number of materials for each upcoming airdrop. This is because style points directly correlate to how many materials were consumed (via decreasing the wear value of accessories) during the previous month.

While the [economy design](https://dsquad.gitbook.io/docs/earn/economy-design) defines the parameters of our inflation mechanism, right now we are still trying to figure out the right number of materials to airdrop each month as we kick-start the project. The goal is to define a programmable algorithm, but during these initial months, we will need to derive the right algorithm through experimentation by manually determining the magnitude of each airdrop.

A total of 18,780 style points were earned in July. Based on this, adding 1,075 materials should replace what was consumed within the dSquad economy during this period. Since we still need to balance the material ratios towards their targets and provide more trading liquidity for materials like circuits, we’ve chosen to airdrop a total of 2,150 materials (2x what was consumed in July) for August.

Originally we had hoped to gradually bring materials closer to their target ratios by airdropping 4,000-5,000 materials across each of the first 4 months. However, based on current engagement it seems this would inflate the economy way too quickly, and we also need to match the target supply ratios as fast as possible.

After crunching the numbers on our spreadsheets, we found that this allocation for the 2,150 materials would be the fastest way to bring the target ratios back into balance after August:
- 159 Cloth | from 57.42% to 47.37% of materials (target = 48%)
- 974 Wood | from 18.56% to 23.68% of materials (target = 24%)
- 414 Metal | from 7.86% to 11.84% of materials (target = 12%)
- 595 Glass | from 9.98% to 11.84% of materials (target = 12%)
- 30 Circuit | from 3.83% to 3.32% of materials (target = 3%)
- 5 Dfinity Stones | from 2.35% to 1.93% of materials (target = 1%)

As you can see, while there's still room for improvement the August airdrop will bring the actual material supply much closer the their target supply.
