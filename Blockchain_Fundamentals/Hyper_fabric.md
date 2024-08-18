# Hyperledger Fabric

![](https://learn.kba.ai/wp-content/uploads/2024/04/Hyperledger_Fabric.png)

Before we dive into technology let us identify and analyze an industry where [**Hyperledger Fabric**](https://www.hyperledger.org/use/fabric) could become a game-changer.

Boeing 737 holds the record for the most-produced commercial airliner in history with over 10000 units built since 1967. The airplane once known for its impeccable safety records lost its goodwill over frequent accidents in the recent past. Boeing is now struggling to get back the lost reputation.

The above-said scenario can be fatal. In most situations, the companies fail to identify the root cause behind. At times, poor quality products supplied by a third party vendor is pointed. However, the supply chain isn’t mature to identify the source of individual parts caused the accident. Even a faulty part is recognized, it is difficult to trace other planes with the same part supplied by the vendor.

Using Hyperledger Fabric, the aviation industry can create an efficient supply chain and inventory management network to bring absolute traceability to the parts supplied. The sector can restrict the network to only trusted and quality party vendors. In the case of fatality with any part failure, all the aircrafts using the part can be quickly grounded and repaired before any other mishap occurs.

# Why Hyperledger Fabric?

We learned that [Hyperledger Fabric](https://learn.kba.ai/course/blockchain-foundation-program/lessons/hyperledger-fabric/) could bring more efficiency and absolute traceability from the previous unit.

Now let’s see why the blockchain for the aircraft supply chain.

The aviation industry is prone to specific vulnerabilities. The industry is exposed to a robust network of vendors, suppliers, and necessary partners making it a weak link. Here, the supply chain information, its requirements, origins are vital and should be confidential. However, a lack of secure and traceable solutions puts things at risk.

Hyperledger Fabric leverages a modular architecture that provides enterprises plug-and-play solutions for confidential transactions and contracts within a network of associates. The feature allows industries like aviation to bring together all the stakeholders within their ecosystem under one architecture. Hyperledger Fabric can restrict data access, preventing it from reaching the wrong hands. Also, it offers a stable, and scalable framework that includes smart contracts and data privacy. Hyperledger Fabric got membership service providers (MSP) aka Certificate Authority (CA), to manage the identity and permissioned access into the network. The Endorsing peers validate the transaction’s authenticity coming into the network. The Fabric channels enable sharing of highly confidential information within the network on a need-to-know basis.

In our example, if a particular spare part producer wants to share the invoice in private without letting the competitors know, they can make use of the channels.  
All these features make Fabric an ideal permissioned blockchain for the domains needing better transparency, traceability, privacy, and improved transaction speed. Among Hyperledger umbrella projects, Fabric is considered the most popular enterprise blockchain platform designed for businesses.

#   Why Hyperledger Fabric?

We learned that [Hyperledger Fabric](https://learn.kba.ai/course/blockchain-foundation-program/lessons/hyperledger-fabric/) could bring more efficiency and absolute traceability from the previous unit.

Now let’s see why the blockchain for the aircraft supply chain.

The aviation industry is prone to specific vulnerabilities. The industry is exposed to a robust network of vendors, suppliers, and necessary partners making it a weak link. Here, the supply chain information, its requirements, origins are vital and should be confidential. However, a lack of secure and traceable solutions puts things at risk.

Hyperledger Fabric leverages a modular architecture that provides enterprises plug-and-play solutions for confidential transactions and contracts within a network of associates. The feature allows industries like aviation to bring together all the stakeholders within their ecosystem under one architecture. Hyperledger Fabric can restrict data access, preventing it from reaching the wrong hands. Also, it offers a stable, and scalable framework that includes smart contracts and data privacy. Hyperledger Fabric got membership service providers (MSP) aka Certificate Authority (CA), to manage the identity and permissioned access into the network. The Endorsing peers validate the transaction’s authenticity coming into the network. The Fabric channels enable sharing of highly confidential information within the network on a need-to-know basis.

In our example, if a particular spare part producer wants to share the invoice in private without letting the competitors know, they can make use of the channels.  
All these features make Fabric an ideal permissioned blockchain for the domains needing better transparency, traceability, privacy, and improved transaction speed. Among Hyperledger umbrella projects, Fabric is considered the most popular enterprise blockchain platform designed for businesses.

# Smart Contracts in Fabric

We have already seen what a [smart contract](https://learn.kba.ai/course/blockchain-foundation-program/lessons/smart-contracts/) is in the blockchain. How they play their role in conditioning the transactions. Smart contracts allow the performance of credible transactions without any third party. The computer programs define the business logic of a network. They can self validate the specified conditions required for a transaction and can perform the associated actions required by the transaction to take place. Hyperledger Fabric smart contracts are called [**chaincode**](https://hyperledger-fabric.readthedocs.io/en/v1.0.0-beta/chaincode.html) and are mainly written in Go, Nodejs, and Java. Apart from serving as the business logic for the fabric network, the chaincode also helps in defining the assets used in an application.