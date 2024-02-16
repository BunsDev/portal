# ckETH FAQ

The following questions and answers are from the POV developer who wants to know things such as "how does a canister send ckBTC?" or how to write code for smart contracts to hold, send, or receive, please see the other FAQs.

For questions from the POV of a user who wishes to know how to hold, send, receive these tokens, please see the user FAQs.

## How do I write a smart contract that uses ckETH?

For detailed information and potential code examples, check out out the [ICP documentation](https://internetcomputer.org/docs), the [DFINITY forum](https://forum.dfinity.org), and the [ckETH minter documentation](https://github.com/dfinity/ic/blob/master/rs/ethereum/ckETH/minter/README.adoc).

## What is the purpose of ckETH? What specific problem does ckETH aim to solve within the ETH ecosystem?

ckETH, or chain-key Ether, is an Internet Computer (ICP)-native token that represents Ether (ETH), the native token of Ethereum. It serves as a digital twin of ETH on the Internet Computer blockchain. The purpose of ckETH is to address some of the challenges associated with using Ethereum, particularly in terms of usability and transaction costs.

One of the main issues it addresses is the high transaction fees (or "gas fees") on the Ethereum network. By allowing Ethereum holders to interact with ckETH on the Internet Computer, which has significantly lower gas fees, users can enjoy fast and cheap transactions. They can then convert back to Ethereum whenever they want to transact on the Ethereum network.

Another problem that ckETH aims to solve is the complexity and friction involved in using blockchain systems, particularly for mainstream users who are not familiar with the intricacies of tokens and wallets. The process of acquiring and using ckETH is designed to be straightforward and user-friendly, removing many of the barriers that can deter people from engaging with blockchain technology.

Furthermore, ckETH enables direct interaction between ICP canister smart contracts and Ethereum, bypassing potential attack vectors by directly calling Ethereum RPCs through HTTPS outcalls.

In summary, ckETH aims to enhance the usability of the Ethereum ecosystem by providing a more accessible, cost-effective, and secure way for users to engage with blockchain technology.
Sources:
- [A Data-Driven Exploration of ckETH](https://medium.com/dfinity/a-data-driven-exploration-of-ckETH-the-digital-twin-of-ether-on-the-internet-computer-36b762be72e7#b197)
- [The Purposes of the Internet Computer](https://medium.com/dfinity/announcing-internet-computer-mainnet-and-a-20-year-roadmap-790e56cbe04a#0289)

## How does ckETH relate to ETH? How is ckETH different from a regular ETH transaction? Can I use ckETH just like I would use ETH?

The main difference between a ckETH transaction and a regular ETH transaction lies in the transaction fees and the blockchain they operate on. Regular ETH transactions occur on the Ethereum network and are subject to Ethereum's gas fees, which can be quite high. On the other hand, ckETH transactions occur on the Internet Computer blockchain, which has significantly lower transaction fees.

Yes, you can use ckETH just like you would use ETH, but within the Internet Computer ecosystem. You can deposit your ETH to a specific function in the ckETH helper contract on Ethereum, which then triggers the ICP ckETH canister smart contract to mint the same amount of ckETH to the specified ICP principal or wallet address. This ckETH can then be used natively on the Internet Computer, and can be converted back to ETH at any time.

However, it's important to note that while ckETH can be used in a similar manner to ETH, the platforms and services that accept ckETH might be different from those that accept ETH, as they are operating on different blockchains.
Sources:
- [A Data-Driven Exploration of ckETH](https://medium.com/dfinity/a-data-driven-exploration-of-ckETH-the-digital-twin-of-ether-on-the-internet-computer-36b762be72e7#b197)
- [How does ckETH work?](https://medium.com/dfinity/a-data-driven-exploration-of-ckETH-the-digital-twin-of-ether-on-the-internet-computer-36b762be72e7#e978)
- [How to Acquire ckETH](https://medium.com/dfinity/how-to-acquire-ckETH-02d863c835fc#e10f)
- [Ethereum + ICP > Multi-chain DeFi](https://internetcomputer.org/ethereum-integration)

## What are the benefits of using ckETH over traditional Bitcoin transactions? 

The benefits of using ckETH over traditional Bitcoin transactions primarily revolve around transaction speed, cost, and interoperability with the ICP ecosystem.

1. **Lower transaction fees**: One of the main advantages of using ckETH is the significantly lower transaction fees compared to Bitcoin. Bitcoin transactions can sometimes be expensive, especially during periods of high network congestion. On the other hand, ckETH transactions occur on the Internet Computer blockchain, which has significantly lower transaction fees.

2. **Faster transaction speed**: The ICP blockchain has a faster transaction speed compared to the Bitcoin network. This means that transactions using ckETH can be processed more quickly, providing a smoother and more efficient user experience.

3. **Interoperability**: ckETH allows for seamless interaction between the Ethereum and ICP ecosystems. This interoperability can potentially unlock new use cases and applications, such as decentralized finance (DeFi) platforms that span multiple blockchains.

4. **Usability**: The process of acquiring and using ckETH is designed to be straightforward and user-friendly, removing many of the barriers that can deter people from engaging with blockchain technology.

However, it's important to note that while ckETH provides these benefits, it's not a direct replacement for Bitcoin or ETH. Each has its own unique features and use cases, and the choice between them will depend on your specific needs and circumstances.

Sources:
- [A Data-Driven Exploration of ckETH](https://medium.com/dfinity/a-data-driven-exploration-of-ckETH-the-digital-twin-of-ether-on-the-internet-computer-36b762be72e7#b197)
- [The Purposes of the Internet Computer](https://medium.com/dfinity/announcing-internet-computer-mainnet-and-a-20-year-roadmap-790e56cbe04a#0289)
- [Internet Computer for Ethereum Developers](https://wiki.internetcomputer.org/wiki/The_Internet_Computer_for_Ethereum_Developers#A_very_brief_introduction_to_the_Internet_Computer)
- [Extend Bitcoin, Ethereum and other blockchains](https://wiki.internetcomputer.org/wiki/Extend_Bitcoin,_Ethereum_and_other_blockchains#firstHeading)

## Why should I choose ckETH for my application or service? 

Choosing ckETH for your application or service can provide several benefits:

1. **No need for bridges**: ckETH eliminates the need for bridges. It uses the HTTPS outcalls feature, which allows ICP canister smart contracts to call API requests directly. This bypasses potential attack vectors by directly calling Ethereum RPCs through [HTTPS outcalls](https://medium.com/dfinity/a-data-driven-exploration-of-ckETH-the-digital-twin-of-ether-on-the-internet-computer-36b762be72e7#b197).

2. **Lower transaction fees**: Ethereum holders can interact with ckETH on the Internet Computer, which has significantly lower gas fees than on Ethereum. This allows for more [cost-effective transactions](https://medium.com/dfinity/a-data-driven-exploration-of-ckETH-the-digital-twin-of-ether-on-the-internet-computer-36b762be72e7#b197).

3. **Manage an Ethereum wallet directly in an ICP canister**: ICP canister smart contracts can create and manage an Ethereum wallet address using threshold ECDSA. This provides a seamless way to manage [Ethereum wallets](https://medium.com/dfinity/a-data-driven-exploration-of-ckETH-the-digital-twin-of-ether-on-the-internet-computer-36b762be72e7#b197).

4. **Seamless conversion**: ckETH allows you to enjoy the benefits of fast and cheap transactions and higher security on the Internet Computer, while still being able to seamlessly [convert back to your ETH anytime](https://medium.com/dfinity/a-data-driven-exploration-of-ckETH-the-digital-twin-of-ether-on-the-internet-computer-36b762be72e7#b197).

5. **Multi-chain environment**: ICP enables a multi-chain environment where centralized bridges are obsolete and smart contracts can seamlessly communicate across blockchains. This provides increased asset liquidity, expanded market access, improved scalability and throughput, and access to [ICP’s unique capabilities](https://internetcomputer.org/ethereum-integration).

6. **Gasless token swaps**: Using ckETH, users can swap tokens for a few cents with [0 gas fees](https://internetcomputer.org/ethereum-integration).

7. **Web2 integration**: Connect smart contracts to the world outside blockchain. Fetch real-time price data and more from Web2.

8. **Signing Ethereum transactions**: ICP smart contracts are capable of offering the on-chain Ethereum full node API by using the HTTPS outcalls feature to securely query the Ethereum blockchain, and send transactions to it.

In summary, ckETH provides a secure, cost-effective, and efficient way to interact with the Ethereum blockchain, making it a great choice for your application or service.

## What advantages does ckETH offer in terms of speed, fees, and security?

ckETH offers several advantages in terms of speed, fees, and security:

1. **Speed:** ckETH transactions on ICP have significantly lower latency compared to Ethereum. They can be transferred with 1-2 seconds finality, making them almost instant .

2. **Fees:** Ethereum holders can interact with ckETH on ICP, which has significantly lower gas fees than on Ethereum. Users can swap tokens for a few cents with 0 gas fees .

3. **Security:** ckETH bypasses attack vectors by directly calling Ethereum RPCs through HTTPS outcalls, a feature that enables ICP canister smart contracts to call API requests directly. This minimizes the risk of data leaks, hacks, and breaches . Additionally, issuing and redeeming ckETH goes through Know Your Transaction (KYT) checks to ensure no tainted bitcoin enters the Internet Computer blockchain or is transferred out to tainted Bitcoin addresses .

4. **Integration:** ckETH can be directly processed by smart contracts hosted on ICP, and can be seamlessly converted back to ETH anytime .

Sources:
- [Internet Computer for Ethereum Developers](https://wiki.internetcomputer.org/wiki/The_Internet_Computer_for_Ethereum_Developers#mw-toc-heading)
- [A data-driven exploration of ckETH](https://medium.com/dfinity/a-data-driven-exploration-of-ckETH-the-digital-twin-of-ether-on-the-internet-computer-36b762be72e7#b197)
- [How to Acquire ckETH](https://medium.com/dfinity/how-to-acquire-ckETH-02d863c835fc#c324)
- [Trustless multi-chain on ICP](https://internetcomputer.org/multichain)
- [Ethereum &lt;&gt; ICP](https://internetcomputer.org/ethereum-integration)
- [Multi-chain DeFi](https://internetcomputer.org/defi)
- [Why Bitcoin needs smart contracts](https://medium.com/dfinity/why-bitcoin-needs-smart-contracts-5191fbec294a#acf6)

## How can I integrate ckETH into my existing applications or platforms?

To integrate ckETH into your existing applications or platforms, you can follow these steps:

1. **Obtain an ICP principal or wallet address.**
2. **Deposit your ETH**: Ethereum holders can deposit Ether to the *deposit* function in the ckETH helper contract on Ethereum and specify their ICP principal or wallet address where they want their minted ckETH to appear.
3. **Mint ckETH**: The ICP ckETH canister smart contract will then mint the same amount of ckETH to the indicated ICP principal or wallet address.
4. **Use ckETH**: The ICP principal or wallet address can now use ckETH natively on the Internet Computer.
5. **Convert back to ETH any time**: When the ICP principal wants to convert ckETH back to ETH, they can request the ckETH canister smart contract with the ETH amount and Ethereum address to which they want to send the ETH.

[Learn more about how ckETH works](https://forum.dfinity.org/t/ckETH-a-canister-issued-ether-twin-token-on-the-ic/22819).

Please note that the ckETH integration is part of a larger Ethereum integration on ICP. [Learn more about the Ethereum integration on ICP](https://internetcomputer.org/ethereum-integration).

Also, remember that the Internet Computer makes it possible to build almost any online service fully on-chain, in a full stack decentralization model. This is because canister smart contracts can hold up to 400GiB of memory each, and run in parallel with great efficiency. Moreover, they can directly serve interactive web-based user experiences to users by processing HTTP requests, thanks to ICP’s reverse-gas model (canister smart contracts pay for their own execution using “cycles” that they have been charged with). Now they can also be trustlessly combined with DeFi and other functionality [Ethereum hosts in a World Computer paradigm](https://internetcomputer.org/multichain).

## What are the technical requirements for developers to work with ckETH?

:::info
This answer is a work in progress. Please check back later for an updated response.
:::

## How does ckETH ensure the security of the funds it handles?

ckETH ensures the security of the funds it handles in several ways:

1. **No need for bridges**: ckETH uses a feature called HTTPS outcalls that enables ICP canister smart contracts to call API requests directly. This bypasses attack vectors by directly calling Ethereum RPCs, eliminating the need for potentially insecure bridges. 

2. **Managing an Ethereum wallet directly in an ICP canister**: ICP canister smart contracts can create and manage an Ethereum wallet address using threshold ECDSA. This means that the ICP ckETH minter canister smart contract can generate an address that holds ETH and signs transactions, adding an extra layer of security.

3. **NNS DAO governance**: The development of ckETH includes measures to guarantee long-term maintenance and provide more security to ETH through NNS DAO governance. This ensures that the management and development of ckETH are in the hands of a decentralized community, reducing the risk of malicious actions by a single party. 

4. **Chain-key signatures**: ICP has the ability to sign native transactions on other blockchains without using risky bridges. This feature is used in the operation of ckETH, further enhancing its security. 

Remember, while these features enhance the security of ckETH, it's always important to exercise caution and good security practices when dealing with cryptocurrencies.

## Can I trust that my funds are safe when using ckETH?

Yes, you can trust that your funds are safe when using ckETH. ICP offers several features that enhance the security and trustworthiness of its canister smart contracts, such as ckETH.

However, as with any blockchain technology, it's important to do your own research and understand the risks involved.

## Can I build smart contracts that interact with ckETH? What kind of functionalities can these smart contracts provide?

Yes, you can build smart contracts that interact with ckETH on the Internet Computer. These smart contracts, also known as canisters, can provide a wide range of functionalities. Here are some of the key capabilities:

1. **Minting ckETH**: When you deposit your ETH to the ckETH helper contract on Ethereum, the ICP ckETH canister smart contract will mint the same amount of ckETH to your specified ICP principal or wallet address.

2. **Using ckETH**: Once the ckETH is minted, it can be used natively on the Internet Computer. This means that your smart contracts can interact with ckETH just like they would with any other token on the Internet Computer.

3. **Converting ckETH back to ETH**: If you want to convert your ckETH back to ETH, you can do so by requesting the ckETH canister smart contract with the ETH amount and Ethereum address to which you want to send the ETH.

4. **Interacting with Ethereum smart contracts**: ICP canisters can interact with Ethereum smart contracts. This is made possible by the Internet Computer's ability to make HTTPS outcalls to Ethereum APIs to securely query and send transactions to the Ethereum network.

5. **Managing an Ethereum wallet**: ICP canister smart contracts can create and manage an Ethereum wallet address using threshold ECDSA. This means that your smart contracts can hold ETH and sign transactions.

6. **Processing and storing large volumes of data**: Smart contracts can process and store large volumes of data at a relatively stable cost that is a tiny fraction of that on traditional blockchain.

7. **Serving web experiences directly to end users**: Smart contracts on ICP can serve web experiences directly to end users, providing end-to-end blockchain security.

8. **Creating and managing other Ethereum asset twins**: In addition to ckETH, you can also create and manage "twins" of other Ethereum assets, such as ckUSDC, ckUSDT, ckUNISWAP, ck1INCH, ckAAVE .

Please note that the ICP ETH integration is still in development, and more functionalities will be added in the future.

**Additional reading**

- [A data driven exploration of ckETH](https://medium.com/dfinity/a-data-driven-exploration-of-ckETH-the-digital-twin-of-ether-on-the-internet-computer-36b762be72e7#e978).
- [Developer Journey: 5.2: ICP ETH tutorial](https://internetcomputer.org/docs/current/tutorials/developer-journey/level-5/5.2-ICP-ETH-tutorial#overview).
- [ICP Ethereum integration explained](https://medium.com/dfinity/internet-computer-ethereum-integration-explained-6967456e35f9#58f6).

## What are the transaction fees associated with ckETH?

The transaction fees associated with ckETH on the Internet Computer are significantly lower compared to those on Ethereum. This is one of the key advantages of using ckETH. 

When you use ckETH on ICP, you can send and receive ETH value on ICP DEXs for a few cents with 1-2s finality, and no gas fees . This is in contrast to Ethereum, where the average transaction fees for USDC and USDT were $4.21 and $5.46 respectively in June 2023.

Moreover, the "chain key" versions of Ethereum assets, including ckETH, live on ledgers created by Internet Computer smart contracts, where they can be transferred with 1 second finality and at near zero cost.

Please note that while the transaction fees on ICP are low, there may still be costs associated with converting ETH to ckETH and vice versa, as well as interacting with Ethereum smart contracts from the Internet Computer.

## How quickly can transactions be finalized?

ICP is designed to finalize transactions very quickly. Specifically, it can finalize transactions that update canister smart contract state in 1–2 seconds. This is a significant improvement over traditional blockchains like Bitcoin and Ethereum, which can take much longer to finalize transactions.

In addition, ICP splits canister function execution into two types: "update calls" and "query calls". Update calls, which we are already familiar with, take 1–2 seconds to finalize their execution. On the other hand, query calls work differently because any changes they make to state are discarded after they run. This allows query calls to execute in milliseconds.

ICP is capable of processing up to 11,500 transactions per second, executed with an average 1-second finality on dapp subnets and a 2-second finality on the Network Nervous System (NNS) subnet.


## Who controls the development and governance of ckETH?

The development and governance of ckETH, the digital twin of ETH on the Internet Computer (ICP), is managed by the ICP ecosystem. The ICP ckETH canister smart contract is responsible for minting ckETH and managing the conversion of ckETH back to ETH. 

The governance of the Internet Computer, and by extension ckETH, is decentralized. The evolution of the system depends on the governance mechanism that defines how a system can change. In the case of the Internet Computer, the NNS canisters define the governance mechanisms, including the parameters for staking, voting, and rewards. Users can stake ICP to participate in voting. The DFINITY foundation and the ICA are the parties with the highest voting power in the ecosystem, together holding less than 23% of the total voting power.

For more information on the governance and tokenomics of the Internet Computer, you can refer to the [Internet Computer Wiki](https://wiki.internetcomputer.org/wiki/NNS_Canisters) and [Tokenomics of a DAO](https://wiki.internetcomputer.org/wiki/Tokenomics_of_a_DAO).

**Additional reading**

- [Internet Computer Wiki - Decentralization](https://wiki.internetcomputer.org/wiki/Decentralization#firstHeading)

## Can you provide examples of current applications that utilize ckETH?
:::info
This answer is a work in progress. Please check back later for an updated response.
:::

# What is the current state of ckETH project?

ckETH is live on the Internet Computer mainnet. It has been added to the ICP dashboard and is also supported in the ICRC-1 wallet. However, with the current ckETH integration, you cannot withdraw to ETH directly from the ICRC-1 wallet. 

The integration is being carried out in phases. Phase 0, which enables chain-key signing and HTTPS outcalls, is already complete. Phase 1 is being built to allow ETH API calls by accessing Web-2 based API providers through HTTPS outcalls. This phase also includes designing and building ckETH and ckERC-20 tokens. The final phase, Phase 2, will revolve around native ETH integration.

For more information on the current state of the ckETH project, you can join the forum discussion or check out the Ethereum integration page on the ICP website.

**Additional reading**

- [Internet Computer Blog - ckETH: now live!](https://internetcomputer.org/blog/2023/12/06/news-and-updates/update#ckETH-now-live).
- [Dfinity - Global R&D: May 2023 Edition - ETH Integration: Status update](https://medium.com/dfinity/global-r-d-may-2023-edition-d96859039ca6#a28d).
- [Ethereum + ICP - Multi-chain DeFi](https://internetcomputer.org/ethereum-integration).
- [Ethereum + ICP - Build your own Ethereummulti-chain solution - Tutorial](https://internetcomputer.org/ethereum-integration).