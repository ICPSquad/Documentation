---
description: A detailed guide on how we designed our economy.
---

# 📐 Economy Design

Most projects would keep this type of advanced material private, but since this is a community project we’re committed to being 100% transparent with everything! In addition, we believe that a game should be so well designed that even insiders can’t get an unfair advantage.

That said, if you’re nerdy enough to read all this material you should have all the knowledge you need to fully understand how it all works so you can maximize your gameplay. In addition, please share any feedback you might have so that we can make this the strongest project ever!

## Advanced Design Goals

### Accessory rewards/win rate

Accessories need to provide a strong probability of getting more back in rewards than a player has put in so that they are worth collecting, but if they 100% guarantee gains then whales/bots will be able to suck all of the value out of the system and that’ll ruin the fun for the majority of players. In addition, we want to have as many individual winners as possible during each airdrop, since that’ll maximize enthusiasm and engagement for the community of holders.

As mentioned before, we introduced the “Max Advantage Cap” at the very beginning of the project. After designing the economy, we discovered that the math works out great in terms of making sure there’s a large distribution of winners. In one of our early simulations for the first full airdrop, the top ranked player had about a 168% chance of winning a material (meaning they’d get at least 1-2) and the lowest ranked player had a 0.84% chance.

However, the problem here is that the highest ranked player would have significantly reduced the wear value of a lot of valuable accessories to earn that rank, and the average accessory costs \~21 materials to mint but only lasts 100 days. Since they would only be winning 1-3 materials each month, we’ll need to make sure the top ranked players have a very high probability of getting the rarest materials so that they have a chance of winning more value in rewards than they spent on accessories.

The end result is that increasing your rank will improve both your odds of winning a prize as well as the value of the prizes you’d win. The highest ranked players will win the rarest materials and then need to choose between either buying the more common materials off the market to mint new accessories, or to sell their rare materials for profit. This is ideal because it means the most involved players (higher ranked) will need to buy the common accessories off the market from the less active (lower ranked) players, creating demand which reinforces the project. Why not mint an Avatar for the chance of occasionally winning a little extra ICP?

### Accessory Rarity & Diversity

We need to make sure accessories remain rare, without constraining them to a fixed supply. This is because we want to create an inclusive NFT project where everyone on the Internet Computer can have an avatar and a chance to win prizes while exploring the ecosystem. A fixed supply wouldn’t be able to scale with the number of players. In this context, “rare” means “the supply is always less than the demand”.

We design this rarity into the game by setting limits on the ratios between players and accessories, making sure that the supply of accessories is always much lower than the number of players who will want to use them.

## Accessory Recipe Design

### Players vs Avatars

Right now, a player is a user who is identified by the principal ID they use to log into our platform. An avatar is the NFT character they use to wear accessories and earn prizes.

While one player might own multiple avatars, only one avatar can be “active” per player (they pick which one in their profile). Therefore, the total number of players is meant to more closely represent the number of individual humans involved, and it’ll be less than the total supply of avatars. Effective Materials “Effective Materials” refers to the number of materials which effectively make up a group of materials and/or accessories. It’s calculated by adding up any material cards, and then adding up all of the materials which would need to be burned to mint any accessories (taking their wear value into account).

For example, if a particular accessory has a recipe which requires 10 materials to mint and it’s wear value is only 50 out of 100 (it’s half way worn out), then it’s counted as 5 “Effective Materials”. We would say that someone who owns 2 of these accessories in this condition and 2 material cards owns 12 Effective Materials.

An easier way to think of this might be if we said materials were “staked” to mint accessories, the “total effective materials” in the economy would be how many materials exist both “staked” and “unstaked”. The reason we say materials must be “burned” to mint accessories is because the process isn’t reversible (you can never get back your materials after using them to mint and accessory), and the word “stake” generally implies something could be “unstaked” in the future.

### Total Effective Materials Per Player Ratio (TEMPR)

By dividing the total number of effective materials which exist in our economy by the number of players, we gain a metric which helps us measure the size of our economy relative to the number of players. We use this metric in our calculations to keep an eye on inflation/deflation, so that we can keep the economy balanced as the number of players increases or decreases.

For example, if there are 10,000 players and 100,000 total effective materials in the economy, the TEMPR value is 10 effective materials per player.

Generally, we’ve set a goal of having a TEMPR value of 10-12, but during the initial launch we’ll be a bit more flexible and allow a value in the 10-15 range.

### Percent Minted Ratio (PMR)

This is the percentage of total effective materials in the economy which exists as accessories, and it essentially helps determine liquidity of materials.

We needed a baseline assumption for this value to do our calculations when creating the recipes, so we assumed that roughly 75% of materials will exist as accessories. In practice, this will be a measured value. It’s used in a lot of calculations, and in the future the accessory minting fee will probably be based on this parameter (increasing when it gets too high or decreasing when it gets too low). For now, we’ll be keeping an eye on this metric to try and find out what a healthy and natural range for it is, but this can only be done through live experimentation.

### Material Supply Target Ratios

For each material, we’ve set the target percentage of the total effective material supply which should be that material. This supply target is also listed on every material card, they are as follows:

* **Cloth** should make up 48% of all effective materials in the economy
* **Wood** should make up 24%
* **Glass** should make up 12%
* **Metal** should make up 12%
* **Circuit** should make up 3%
* **Dfinity Stone** should make up 1%

As players mint and burn materials, the actual supply of each material in the economy may vary by small amounts occasionally. During the monthly airdrops, we’ll make sure to add materials to the economy so that these supply targets are constantly preserved.

One thing to keep in mind is that the supply of a specific material for sale in the marketplace might not always match the supply targets if people mint too much of specific accessories, but this is a self-balancing mechanism for the economy since it’ll make other recipes more cost effective.

For example, let’s say people get too excited about the Juggalo Facemask and start to mint too many. The recipe for that accessory is **26 Cloth** & **1 Circuit**. If players start minting too many of these, the liquidity for cloth on the market will start to run out and the price for cloth will spike. This will make it increasingly expensive to mint the Juggalo Facemask and more cost effective to mint recipes which require little or no Cloth. This’ll continue until the irrational market is brought back into balance.

### Accessory Slot Target Ratios

Each player can only equip 1 accessory per slot, and by making it increasingly difficult to fill each incremental slot we ensure a competitive game since very few players will be able to completely fill all slots. These are the supply targets for each Accessory Slot:

* **Eyes** | Enough supply to equip 30-40% of the player population.
* **Head** | Enough supply to equip 20-30% of the player population.
* **Face** | Enough supply to equip 10-20% of the player population.
* **Body** | Enough supply to equip 10-20% of the player population.
* **Misc** | Enough supply to equip 2-5% of the player population.

### ICP/Star Ratios

In addition, to keep the game competitive and diverse we need to make sure that the more valuable items are increasingly expensive. To measure this we divide the estimated-comparative cost of a recipe by the star rating of the accessory to get the cost-per-star.

For example, if the floor price of 2 star accessories for the eye slot is 10 ICP, then this category of accessories has a ICP/Star ratio of 5 ICP. Likewise, if 5 star accessories for the eye slot have a floor price of 50 ICP, then that’s a ICP/Star ratio of 10 ICP. This means you’d get the most stars for your money by starting with lower star items, but once you fill all slots the only way to improve further is to spend more on higher star value accessories.

To help drive the market to meet the accessory slot target ratios, we’ve designed the recipes to also become increasingly expensive for rarer slots. This means a 2 star accessory for the Eyes slot will have a lower ICP/Star ratio than a 2 star accessory for the Body slot.

### Recipe Supply Limits

This is one of the most genius aspects of our economic design because it limits the supply of accessories, even if the market starts acting irrationally! Describing it is hard though, which is why we needed to define so many other terms first. Assuming a Percent Minted Ratio (PMR) of 75% and a Total Effective Materials Per Player Ratio (TEMPR) of 10, no recipe is able to mint more than +10% above the Accessory Slot Target Ratio of its slot, EVEN IF ALL EFFECTIVE MATERIALS WERE USED JUST TO MINT THIS ONE RECIPE.

Alright, I’m sure that’s confusing so here’s an example. Let’s say there are 10,000 players and 100,000 effective materials. The Boring Mask accessory is in the Face slot, which has a supply target of 10-20%. The recipe for boring mask requires (4) metal, and in this situation only 12,000 metal would exist in the economy. Even if every single Metal was used up trying to mint Boring Masks, only 3,000 could possibly be created (since that would use up all the metal), which is enough for only 30% of the player population (10% more than the slot’s target). Obviously, it’s incredibly unlikely that the market would collectively devote itself toward minting one recipe, but even if it did the economy would still be tightly constrained by a limitation built into that recipe.

We’ve designed every Accessory recipe to be constrained within the +10% limitation described above. This means no single recipe, even if abused and/or irrationally over-minted, could be used to break the economy by making accessories too common.

### Recipe Demand Balance

We took all of the above into consideration and put it into a complex spreadsheet full of calculated fields so that we could simulate the economy within a rational economy. In this spreadsheet we tweaked every recipe until all the requirements above were met, all while keeping the overall expected demand for materials needed for accessory recipes as close as possible to the Material Supply Target Ratios.

For example, let’s assume a Percent Minted Ratio (PMR) of 75% and a Total Effective Materials Per Player Ratio (TEMPR) of 10. Assuming a balanced and rational market, we designed the recipes so that:

* No single recipe would completely run out at this level.
* The Effective Materials within the total supply of accessories would closely match the Material Target Supply Ratios.

While markets are inherently chaotic and can behave irrationally for short periods of time, they also tend to be efficient at balancing supply and demand (in a rational way that makes sense) on average over the long term. Therefore, the goal is to make sure the actual mint demand for any given material generally matches the supply target ratio it’s labeled with.

In other words, cloth (which has a target ratio of 48%) should make up both 48% of the effective supply of materials and 48% of the demand for accessory minting across all recipes as a whole. The goal of this is to reduce the occurrence of shortages and provide a stable foundation for material valuations.

## Leaderboard & Rewards

### Airdrop Algorithm

To make this easier to both explain and understand, we will be describing the reward algorithm using the language of a “raffle”. In a raffle you get one or more tickets with random numbers and then winning numbers are randomly selected and called, and if you hold a ticket which matches a winning number you win. This general idea is essentially how our reward system works on a basic level. Therefore, we’ll use the word “ticket” and “winning ticket”, but these are not tangible assets and all of this happens “under the hood”. From the player’s perspective, at the end of each month they either do or don’t get a reward, the information here is just to explain how we are distributing those prizes.

#### Step 1: Measure Effective Material Actual vs Target

As users wear accessories, they reduce the wear value of those accessories and burn them when that value drops to 0. This is a constant deflationary force on the number of effective materials in the economy.

We determine the monthly prize pool by rebalancing the economy to fit within a healthy range for the Total Effective Materials Per Player Ratio (TEMPR). We expect this to be 10-12, but during the first 4-6 months we’ll aim for 10-15. For example, if 3,000 effective materials left the economy last month and the population of players stayed the same, then we’ll need to add \~3,000 effective materials in prizes this month to balance last month’s deflation.

#### Step 2: Calculate # each material to achieve balanced effective material supply and # winning tickets

Once we determine how many effective materials to add to the prize pool, we then need to determine how much of each type material we need to add. This essentially means we rebalance the total effective materials in the economy to match the material supply target ratios.

For example, each Juggalo Facemask requires 26 cloth to mint. If 100 of these got burned in a single month, it’ll remove a lot of cloth from the total effective material supply in the economy, making cloth rarer and more expensive than it should be. To prevent this we simply add additional cloth to the next reward pool.

#### Step 3: Retrieve leaderboard rankings & generate winning tickets for each player

At the end of each month, we pull the ranking results. The lowest ranked player is granted 100 “tickets” and the highest ranked player is granted 20,000 “tickets”. This limits the top player to having a 200x advantage over the lowest ranked player.

The number of tickets for each rank increments linearly from 100 to 20,000. For example, if there are 10,000 players and your rank is 5,000, then you get 10,000 tickets.

#### Step 4: Draw winning tickets & sort users based on # winning tickets

Materials are valued as follows:

* **Cloth** = 1 winning ticket
* **Wood** = 2 winning tickets
* **Glass** = 4 winning tickets
* **Metal** = 4 winning tickets
* **Circuit** = 16 winning tickets
* **Dfinity Stone** = 48 winning tickets

We then draw the number of winning tickets based on the materials in the prize pool. For example, if the prize pool was just 100 Cloth + 100 Wood, then we’d draw 300 winning tickets. In reality the prize pools will be much bigger but the math works the same way.

Since a lot of winning tickets are drawn, many players will have multiple winning tickets. We’ll then sort players first by #winning tickets they got, then by rank, so if two players both got the same number of winning tickets, then they are sorted based on rank.

#### Step 5: Distribute materials, from rarest to least rare, to players with winning tickets.

We’ll distribute materials in the prize pool starting with the player who has the most winning tickets and then go down the line until all prizes are distributed. We’ll reward each player the best combination of materials possible which would account for all of the winning tickets they hold.

For example, if the top player had 96 winning tickets they’d get (2) Dfinity stones (assuming there were at least 2 in the prize pool for that month). However, if they only had 50 winning tickets, they’d get (1) Dfinity Stone and (1) Wood, since after the Dfinity Stone they had two tickets left and Wood was the best item which could consume those 2 leftover winning tickets.

Another example would be if they had a total of 67 winning tickets, then their prizes would be:

* (1) Dfinity Stone (consumes 48 winning tickets and leaves 19 remaining)
* (1) Circuit (consumes 16 winning tickets and leaves 3 remaining)
* (1) Wood (consumes 2 winning tickets and leaves 1 remaining)
* (1) Cloth (consumes the last 1 winning ticket)

## Initial Economy Launch

### Accessory focus

As we continue dev work, we’ll be constantly adding more ways to track activity, and the goal will be for engagement to be the primary way of maximizing rewards. However, during the first months of the MVP we expect the leaderboard will be heavily influenced by accessories. This will help jump start our accessory economy while we work to build in integrations, and over time the rankings will be more and more impacted by activity and missions on other dapps in the ecosystem.

### Wider tolerances for parameters

When designing this economy we had to make a lot of assumptions, but our goal during the initial months of the MVP will be to allow for natural market discovery so that we can learn what the right levels are for all the parameters that keep the economy balanced. This means there will likely be a lot of volatility and price fluctuations early on as the MVP matures into a more complete product. When we get things wrong we’ll need to experiment and innovate to solve problems as they arise. This will help us reach our ultimate goal of creating an algorithmically balanced economy based on real market dynamics and historical data. In the long run, this will lead to a more stable and robust economy than any other NFT platform out there, one that’s designed for long term scalability and sustainability.
