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

Multibit is an open-source, light client Bitcoin wallet written in Java for execution on desktop and laptop computers. The Java architecture of the code allows for it to be easily ported to Windows, OS X, and Linux. The Classic edition of the wallet was first announced as a project in late 2011. Multibit Classic has been a popular desktop client that competes with Electrum as light client alternatives to the reference full node Bitcoin Core wallet, sparing users from downloading the entire Bitcoin blockchain.

Balance information is obtained from peers on the Bitcoin network through an SPV extension to the Bitcoin protocol using Bloom filters. In recent years, development focus has shifted from Multibit Classic to an HD reboot of the software that is currently in beta testing. The Classic edition of the application lacks basic controls to protect user privacy on the blockchain. Private keys are generated and held in a key pool, making backups more complicated and incentivizing address reuse. Multibit relies on weak privacy guarantees when obtaining balance information and broadcasting transactions. The software provides primitive support for maintaining multiple financial identities by allowing the user to load multiple wallet files simultaneously and quickly switch between them.

##Questionnaire Response ##

Multibit's responses are listed in bold.

**https://github.com/jim618/multibit/issues/671**

1: Please classify your application as one of the three categories:
  * Wallet: all of the private keys needed to create a blockchain transaction are under the exclusive control of the user
  * Pseudo-wallet: none of the private keys needed to create a blockchain transaction are under the exclusive control of the user
  * Hybrid wallet: some portion of the private keys needed to create a blockchain transaction are under the exclusive control of the user

**a. All private keys are under exclusive control of the user.**

2: Does your application provide any type of visual warning to the user when events which may reduce their privacy or safety occur, such as:
  * Receiving funds to an address which has previously received incoming transactions
  * Backups have been invalidated by new receiving or change address creation
  * If the wallet supports mixing, a proposed mixing transaction is easily reversible
  * An outgoing transaction sends funds to a previously-used address
  * An outgoing transaction links inputs from multiple addresses
  * Network connectivity to peers or dedicated balance servers is not routed through an anonymous channel
  * An outgoing transaction links inputs from multiple accounts/identities

**No**

3: Does your application’s backup process involve any activity which may be visible to an external network observer?

**No - backups are performed by the user.**

4: Does your application take positive steps to make change outputs indistinguishable from spending outputs, such as:
  * Randomizing the number of change outputs
  * Randomizing the position of the change output(s)
  * Selecting sufficient input value such that the change output(s) closely resemble the size of the desired spend
  * Intentionally creating “decoy” change outputs that have a low number of significant digits

**No**

5: If your application includes mixing functionality:
  * Is it possible for a malicious participant in the mix to steal funds?
  * Is it possible for any participant in the mix to retain information which correlates outputs to their corresponding inputs?

**There is no mixing in MultiBit Classic**

6: If your application obtains balance information from dedicated servers:
  * Is it possible to operate the dedicated servers in a manner which correlates:
    * A user’s receiving or change address to another receiving or change address in the same wallet
    * Any of the above with a public IP address
    * Any of the above with a registered account 
    * Any of the above with a persistent software or hardware fingerprint
    
**MultiBit Classic does not obtain balance info from other servers. It gets (bloom-filtered) tx information from Bitcoin Core nodes.**
    
7: If your application obtains balance information by uploading a filter to network peers:
  * Are filters ever updated in a manner that allows the peer to correlate the old and new filter with the same connection?

**The bloom filters used by MultiBit (and other bitcoinj based wallets) are susceptible to reverse engineering if an attacker can monitor all the user's network traffic unfortunately.**

8: Does your application take positive steps to route outgoing transactions through different path to the network than the path via which it receives balance and incoming transaction information?

**It broadcasts on one Bitcoin Core node and listens on others yes.**

9: Does your application take positive steps to route outgoing transactions through different path to the network than the path via which it receives balance and incoming transaction information?
  * Does your application take positive steps to route outgoing transactions through different path to the network than the path via which it receives balance and incoming transaction information?
  
**MultiBit Classic does not support multiple identities.**

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
