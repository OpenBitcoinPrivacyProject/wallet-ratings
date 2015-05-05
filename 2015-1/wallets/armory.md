Bitcoin Wallet Privacy Rating - Spring 2015
============================================

<dl>
    <dt>Rank</dt>
    <dd></dd>
    <dt>Name</dt>
    <dd></dd>
    <dt>Type</dt>
    <dd></dd>
    <dt>Version</dt>
    <dd></dd>
    <dt>Score</dt>
    <dd>
        <dl>
            <dt>Overall</dt>
            <dd></dd>
            <dt>Quality</dt>
            <dd></dd>
            <dt>Usability</dt>
            <dd></dd>
            <dt>Feedback</dt>
            <dd></dd>
        </dl>
    </dd>
</dl>

##Description##

Armory is a high-end wallet with features suitable for an experienced user. In addition to its excellent security properties, Armory is good at preserving privacy as well. It connects to the network through Bitcoin Core, which means that the user stores the whole block chain on his own computer and does not need to query servers to learn his balance. It supports wallets with deterministic address generation and does not reuse addresses by default. It can easily be used with Tor. 

To improve its privacy, Armory must enable its users to use some mixing protocol such as CoinJoin and must be more careful about how it joins change addresses and about how it warns users when redemption of change addresses might compromise the user’s privacy. 

##Questionnaire Response ##

Armory's responses are listed in bold.

1: Please classify your application as one of the three categories:
  * Wallet: all of the private keys needed to create a blockchain transaction are under the exclusive control of the user

**Yes**
  
  * Pseudo-wallet: none of the private keys needed to create a blockchain transaction are under the exclusive control of the user

**No**
  
  * Hybrid wallet: some portion of the private keys needed to create a blockchain transaction are under the exclusive control of the user

**No**

2: Does your application provide any type of visual warning to the user when events which may reduce their privacy or safety occur, such as:
  * Receiving funds to an address which has previously received incoming transactions

**No, Could be implemented with ArmoryD**
  
  * Backups have been invalidated by new receiving or change address creation
  
**Not applicable because Armory wallets use deterministic address generation**  
  
  * If the wallet supports mixing, a proposed mixing transaction is easily reversible
  
**No, Could be implemented with ArmoryD**
  
  * An outgoing transaction sends funds to a previously-used address
  
**No, Could be implemented with ArmoryD**
  
  * An outgoing transaction links inputs from multiple addresses
  
**No, Could be implemented with ArmoryD**
  
  * Network connectivity to peers or dedicated balance servers is not routed through an anonymous channel
  
**No**
  
  * An outgoing transaction links inputs from multiple accounts/identities

**Not applicable**
  
3: Does your application’s backup process involve any activity which may be visible to an external network observer?

**Not necessarily, We have the ability "secure" print your backup from an offline computer. With secure print the user writes a code on the backup page. The written code would be necessary during restoration.**

4: Does your application take positive steps to make change outputs indistinguishable from spending outputs, such as:
  * Randomizing the number of change outputs
  * Randomizing the position of the change output(s)
  * Selecting sufficient input value such that the change output(s) closely resemble the size of the desired spend
  * Intentionally creating “decoy” change outputs that have a low number of significant digits

**None of those**  

5: If your application includes mixing functionality:

  * Is it possible for a malicious participant in the mix to steal funds?
  * Is it possible for any participant in the mix to retain information which correlates outputs to their corresponding inputs?

**Depends on how it's implemented with ArmoryD**

6: If your application obtains balance information from dedicated servers:
  * Is it possible to operate the dedicated servers in a manner which correlates:
    * A user’s receiving or change address to another receiving or change address in the same wallet
    * Any of the above with a public IP address
    * Any of the above with a registered account 
    * Any of the above with a persistent software or hardware fingerprint
    
**Not applicable**
    
7: If your application obtains balance information by uploading a filter to network peers:
  * Are filters ever updated in a manner that allows the peer to correlate the old and new filter with the same connection?
  
**Not applicable**

8: Does your application take positive steps to route outgoing transactions through different path to the network than the path via which it receives balance and incoming transaction information?

**No**

9: Does your application take positive steps to route outgoing transactions through different path to the network than the path via which it receives balance and incoming transaction information?
  * Does your application take positive steps to route outgoing transactions through different path to the network than the path via which it receives balance and incoming transaction information?
  
**No**

##Question Scores##

<dl>
    <dt>I A 1 a)</dt>
    <dd></dd>
    <dt>I A 2 a)</dt>
    <dd></dd>
    <dt>I A 2 b)</dt>
    <dd></dd>
    <dt>I B 1 a)</dt>
    <dd></dd>
    <dt>I B 2 a)</dt>
    <dd></dd>
    <dt>I B 3 a)</dt>
    <dd></dd>
    <dt>II A 1 a)</dt>
    <dd></dd>
    <dt>II A 2 b)</dt>
    <dd></dd>
    <dt>II A 2 c)</dt>
    <dd></dd>
    <dt>II A 3 a)</dt>
    <dd></dd>
    <dt>II A 3 b)</dt>
    <dd></dd>
    <dt>II B 1 a)</dt>
    <dd></dd>
    <dt>II B 2 a)</dt>
    <dd></dd>
    <dt>II B 3 a)</dt>
    <dd></dd>
    <dt>III A 1 a)</dt>
    <dd></dd>
    <dt>III A 2 a)</dt>
    <dd></dd>
    <dt>III A 2 b)</dt>
    <dd></dd>
    <dt>III A 2 c)</dt>
    <dd></dd>
    <dt>III A 3 a)</dt>
    <dd></dd>
    <dt>III B 1 a)</dt>
    <dd></dd>
    <dt>III C 1 a)</dt>
    <dd></dd>
    <dt>III C 2 a)</dt>
    <dd></dd>
    <dt>III D 1 a)</dt>
    <dd></dd>
    <dt>IV A 1 a)</dt>
    <dd></dd>
    <dt>IV B a a)</dt>
    <dd></dd>
    <dt>V A 1 a)</dt>
    <dd></dd>
    <dt>V A 2 a)</dt>
    <dd></dd>
    <dt>V A 3 a)</dt>
    <dd></dd>
    <dt>V B 1 a)</dt>
    <dd></dd>
    <dt>V b 2 a)</dt>
    <dd></dd>
    <dt>V B 3 a)</dt>
    <dd></dd>
    <dt>V C 1 a)</dt>
    <dd></dd>
    <dt>V C 1 b)</dt>
    <dd></dd>
    <dt>V C 2 a)</dt>
    <dd></dd>
    <dt>V C 2 b)</dt>
    <dd></dd>
    <dt>V C 3 a)</dt>
    <dd></dd>
    <dt>V D 1 a)</dt>
    <dd></dd>
</dl>

