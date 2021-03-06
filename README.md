I'm completely new to crypto development. After having done a bunch of research about the space, I decided that Ethereum development is the right first-step because of the robust ecosystem & because it's proven. I also digged into Polkadot and that seems legit. Other chains like Solana and Avalanche seem interesting but from an innovation standpoint they don't have anything interesting to offer other than the obvious (ie less gas fees + faster transactions). Polkadot seems much more interesting. Future is multi-chains for sure. Bridges and etc will enable an efficient multi-chain world. There won't be an Eth or any other killer. Less than 2% of the world population use crypto. Barely any crypto devs. Things are still new, but Eth is catching up.

Best use of my time is to learn Ethereum (solidity) dev only. A little bit of FE too y not. Here's my game-plan:

- Follow [this](https://docs.scaffoldeth.io/scaffold-eth/)
- Spend **4 hours a day** coding and going through other peoples' codebases
- Don't spend time degenning. HODL whatever I have. Discord/Twitter/etc is mostly waste of time atm. Use Stackoverflow for questions, and sure use Twitter to get updates on what's happening.

Goal is to be able to code 'anything' (esp defi) with confidence in **3 months from now**.

Start: 1/11/2022
End: 4/11/2022

After learning enough basics, start contributing. Apply for grants, submit PRs, and do whatever. Update this doc to update goal.

### Logs
- 1/11/2022: Locked in game-plan. Time to get coding. Setup [scaffold-eth](https://github.com/scaffold-eth/scaffold-eth) complete. Finished [mapping](https://solidity-by-example.org/).
- 1/12/2022: Spent 4.5 hours following [this](https://solidity-by-example.org/). Finished [multi-sig wallet](https://solidity-by-example.org/app/multi-sig-wallet/). Much more confident now!
- 1/13/2022: Ugh spent like 3 hours working on [this](https://solidity-by-example.org/app/merkle-tree)... but I finally got it. Main issue was odd number of nodes in the Merkle tree was constructed incorrectly with the algorithm provided. Learning: I should have re-reviewed Merkle Tree construction again with the odd numbers to understand what was going wrong instead of trying to tweak the inputs of verification method to have a valid output.
- 1/14/2022: No work. OHM crashed hard so I spent time researching (ie tweets, reaffirming belief, etc).
- 1/15/2022: Only did 3 hrs work. Stopped at ERC721
- 1/16/2022: Only 1 hour. Got distracted w/surfing Escort websites and porn :(. Missed opportunity. OHM crashed HARD. But HOLDing.
- 1/17/2022: ~3.5 hours studying how contract creation works (added notes below). OHM crashed super hard. Spent 1-2 hours digging.
- 1/18/2022: Spent 4 hours - up until "Bi-directional Payment Channel" section. _Note:_ Wasted an entire hour by including a wrong openzapplin import from tutorial. Researched for an hour by googling error code instead of checking Openzapplin Github page to make sure import is correct. Ugh.



### Contract Creation (notes) (1/17/2022)
#### Accounts:
* Can be external or contract accounts
* All contain addresses
* Only external accounts have corresponding private keys
* All contain balance, nonce, bytecode, sorage data
* Nonce gets incremented at every OUTGOING transaction, starting with 0. Ex. 10 outgoing transactions => 9 nonce.
* Bytecode & stoarge data is empty for external accounts
* For contract accounts, storage data is root of merkle tree

#### Contract creation:
- Contracts creation is done by sending a transaction to address 0 with compiled bytecode as the payload data.
- The bytecode contains <initcode><runtime_code>params
- Contract creation happens in this order:
  - EVM creates contract account with the address corresponding to hash of sender address + nonce
  - The initializtion code is executed, and the returned array of bytes (ie bytecode) is stored as the bytecode of the contract account.

#### Initialization code:
- Set up contract code (ex initialize state variables)
- Place runtime bytecode somewhere in the memory and add appropriate metadata on stack to help EVM refer to that bytecode (ie offset + length).
- Once placed in memory, executes return statement with the metadata on stack.

  
### Skin in the game as a contributor (1/18/2022)
Its crazy how much of an impact my bags had on me as a contributor in the last few days. My eyes were constantly on prices of my bags and that prevented me from learning and growing. I have 2 years of personal runway, and the last thing I need to do is look at my bag's valuations. I need to completely stop looking at prices and focus on learning and development. I'm literally getting nothing out of looking at my bags. Let the eggs rest and hatch when time's right. I shouldn't even have to worry about liquidations because I literally borrowed like less than 10% of my OHM. Even if OHM hits as low as $40 I STILL wouldn't be liquidated! Most VCs and angel investors drop their money into something that takes a long time to liquidate. I need to also think like an angel and stop worrying too much about price volitility. From now on, I'll do my best to ignore prices and stay grounded and focus on my original mission and goal.
