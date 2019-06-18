---
templateKey: blog-post
title: Current State & Capabilities of the Liquid Sidechain
date: 2019-03-21T03:51:46.062Z
description: >+
  More and more functionalities are being built on top of Bitcoin's existing
  protocol. In this week's publication, we provide an explanation to Bitcoin's
  sidechain Liquid, how it works, its applications, features and the revenue
  model behind it. Enjoy!

featuredpost: true
featuredimage: /img/wire-2019-05-17-at-18.05.58-ts1558131201.jpeg
---
IMPORTANT NOTICE : We have corrected inaccuracies about how the Liquid network works, particularly in the governance and revenue model. We would like to thank Blockstream, especially Neil Woodfine, Mario Gibney and Allen Piscitello.



 



How to try it

 

At first, we were going to construct a tutorial to build Liquid and a guide to using it for issuing and transferring L-BTC and assets while experiencing Confidential Transactions. This isn’t necessary anymore because Liquid Core is finally out for every desktop platform, as a GUI version and command-line.  The GUI version has a simple limitation: you can’t issue assets on it but you can transfer them. It's only on the CLI that you can issue assets. To try the Liquid Network today, download the package associated to your desktop platform, extract it and launch either liquidd for the CLI or liquid-qt for the GUI. Use this practical guide to get started, here.



 



It’s important to keep in mind that these are Liquid Full Nodes thus have to sync and are somewhat heavier than a light version would be. If you’d rather use the light version or want a Liquid Full node on Android, the recently renamed Blockstream Green and Abcore will add Liquid support eventually. When? Soon says Lawrence Nahum, Chief Architect at Blockstream and we will take his word because Liquid-qt was released imminently as he said!  



![](/img/f6ed73ae488d82fcceeeb66599140dc0_600x418.png)



Strong Federation Technology 

 

Briefly, the Liquid Network is a federated sidechain that works as an inter-exchange settlement network. It has 1-minute blocks and each block is of the same weight as on Bitcoin: 4 MWU.  L-BTC is the main asset on the Liquid Network and it is fully backed in bitcoin since it is a sidechain. Liquid is built on the Elements platform and it has components such as Issued Assets and Confidential Transactions on it. There are three categories of parties on Liquid : Functionaries, Members and Users. There are 15 Functionaries, who always remain online, and they serve two main roles : Blocksigning and Watchmen. This means that the Functionaries are in charge of creating the blocks on the network. It also means that they are in charge of watching the funds on the mainnet when a peg-out is done.  They govern the network and they can peg-in and peg-out. There are currently 23 Members on the network but many more are on the way, you can find the current list here. They do not mine blocks, but they can peg-in and peg-out. Users can either use Liquid through a full-node software or through a light-client and they can peg-in but can't peg-out.



 



The technology behind Liquid is called Strong Federations. It is a sidechain structure that replaces Proof-of-Work and works in a trusted way towards the Federations Functionaries. They replace the miners so they are in charge of creating the blocks interchangeably and then 11 out of 15 of them have to sign for a block to propagate. The Functionaries use hardware modules in their servers to complete this action and are pseudo-anonymous and distributed around the globe. Reorganizations of the chain don't happen in Liquid since there is a predictable established protocol for creating blocks that isn't random like Bitcoin's is.  The tradeoff for this technology is obviously that it is a trusted network where the Functionaries are the only ones to direct consensus on the network but Blockstream has been very transparent about this so we don't see an issue with it.



 



Peg-out Process & Trading

 

The other function of the Strong Federation is the peg-out process, this also, isn't a trustless process. Liquid Members (including Functionaries)  are the only ones to be able to peg-out bitcoin, held in an 11 of 15 multi-sig wallet. Peg-out means that one has L-BTC on Liquid and wants to get BTC on the mainchain. A regular user can't peg-out by himself, he has to pass through a Member and currently only The Rock Trading is available. This exchange requires a 100-EUR annual fee to trade on it. Not exactly a bad deal for a trader but if one simply wants to unpeg L-BTC, this is far from being good UX. I contacted Blockstream’s support to know if other exchanges are available yet, you can see their answer for yourselves on the image below. I’m guessing an announcement will be made soon since they are very consistent with their roadmap and engagements.



Blockstream proposes to users to do p2p trades on the IRC chat sidechains-dev or on the Telegram channel Liquid community. Eventually, Blockstream hopes it will be possible to atomic swap L-BTC for BTC on the Lightning Network. The second-layer scaling solution can be implemented on Liquid too since it has segregated witness implemented. Also, sideshift.ai, who's currently in test pilot, will eventually allow instant trading of L-BTC and BTC among other coins, in a shapeshift-like fashion.



 



I asked Instagibbs, the Liquid Engineering Manager, about the future of the peg-out process and he answered that he might envision a day where users would be able to peg-out by themselves if they were willing to wait like a week, but that it couldn’t possibly be done under the current security model. Then, Adam Back, the CEO of Blockstream, jumped on the conversation to explain how the peg-out process works.



Business Model

 



Blockstream was created with the purpose of building a sidechain in a profitable way, Liquid is the product of that pursuit. It's then important to keep in mind that Liquid is, first and foremost, a business product of the company. The current revenue model behind Liquid isn't completely clear since it mostly involves private deals with the Members for the moment, but Blockstream has confirmed to us that it consists of an annual fee charged to the Members for technical support, which includes a lease of the necessary hardware to run Liquid. The Members aren’t forced to pay for the technical support services and could work on Liquid themselves. Blockstream is actually working towards giving more independence to the Members, so that together they can make decisions regarding the introduction of new Members. They also receive the fees from the Liquid Network but mostly use them for paying the peg-out process on the Bitcoin's blockchain. In the future, Blockstream envisions that their revenue model will be mostly on providing added-value products and services for users of the Liquid Network. We can’t wait to find out what they are preparing for us, the Users.



 



Applications

 



Liquid is mostly branded as a product for exchanges because that’s its main function: an interexchange settlement network. Traders are also encouraged to use Liquid, but this can’t be done yet since only one exchange supports it. Recently, the Liquid Network is getting some serious traction from firms that want to issue their own security token or tokenized fiat since issuing assets on the Liquid Network is easier than on any other platform and transactions have a lot of privacy benefits. Crypto Garage, a collaboration firm between Blockstream and Digital Garage, a japanese financial firm, is creating Settlenet, a platform to easily issue assets on the Liquid Network.  You might be wondering why they would do that when they can use Ethereum or another altcoin’s blockchain that has had a way to issue tokens for years.



 



Issuing a token isn’t a decentralized process, whether it’s a security token or a stable coin, there is some serious trust towards the issuer. These tokens have to be backed by a tangible asset and that has to be assured by a corporation which is centralized by design. There is no need to issue this on a blockchain’s base layer since it doesn’t require complete decentralization. A federated sidechain fully backed by BTC makes perfect sense for this application by not creating an unnecessary monetary system that is competitive to bitcoin while allowing for the desired blockchain characteristics of auditing of the network by running a Liquid Full Node.



 



Features

 



Liquid isn’t fully auditable though since it implements Confidential Transactions by default. Confidential Transactions are a cryptographic technique that uses homomorphic encryption and rangeproofs in order to make it possible to hide the amounts of the transactions while allowing observers to verify that no extra coins have been created. It also hides the type of asset being transferred. One can choose to disable it for a transaction of any kind or to share the view key with any party. This creates a design of privacy by default that allows one to reveal himself to the world in the way he wishes to. Here is how it appears like on the explorer.



All these traits can also be found on the Elements Platform, an open-source platform for building sidechains or blockchains based on the Bitcoin protocol. Research projects from Blockstream such as Simplicity and Musig will get added on Elements and on Liquid eventually. This is fantastic as it serves as a way to try out bitcoin technology before it gets activated on Bitcoin’s mainnet. To learn more about Musig, check out our visual diagram right here, that fully explains ECDSA, Schnorr signatures, and Musig. I recommend to experienced users to try out Elements and start playing with it if they haven’t yet, since possibilities are endless, and who knows, maybe you will develop the next hot sidechain project. To talk more about Elements, join the Bitcoin Core Slack, and then the Elements channel.



 



In conclusion, we believe Liquid has a lot of potential at becoming a successful inter-exchange settlement network, a platform to issue assets and a sidechain to test Bitcoin research projects. Nonetheless, Liquid will remain a federated chain that isn’t completely decentralized and that will be directed by its Members. Blockstream has a considerable influence over it for the moment but they plan to give more and more power to the rest of the Members as time goes on. As long as they remain transparent, this project will be beneficial for them and for the extended Bitcoin community. We would like to thank Blockstream for their quick answers to our questions and particularly Mario Gibney for his great advice on the Revenue Model and Confidential Transactions. To continue the discussion about Liquid, join the community telegram group here and feel free to contact us to talk further about this promising and exciting bitcoin technology!



 



References

https://blockstream.com/assets/ downloads/strong-federations.pdf  

https://github.com/ ElementsProject/elements 

https://www.youtube.com/watch?v=9pyVvq-vrrM

https://www.youtube.com/watch?v=GwnFfp5xIag

https://cryptogarage.co.jp/en/

https://settlenet.io/

https://liquid.horse/

https://blockstream.com/ categories/en/liquid/
