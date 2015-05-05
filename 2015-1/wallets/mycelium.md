Bitcoin Wallet Privacy Rating - Spring 2015
============================================

<dl>
    <dt>Rank</dt>
    <dd></dd>
    <dt>Name</dt>
    <dd>Mycelium</dd>
    <dt>Type</dt>
    <dd>Wallet</dd>
    <dt>Version</dt>
    <dd>2.2.0 (android)</dd>
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

Mycelium Bitcoin Wallet is generally considered the leading Android wallet throughout 2014 and in to 2015. In terms of privacy features, Mycelium implements HD wallets based on BIP44, including multiple account support, and encourages good behavior by not encouraging address reuse by default. Mycelium is notable for including Local Trader, a built-in P2P system for finding traders to exchange between local currencies and Bitcoin.

Mycelium is the best performer of all mobile wallets in this round of rating, but its score suffers from the method via which the wallet obtains balance information. Mycelium wallet obtain their balance information from dedicated Mycelium servers instead of connecting to network peers. While this does provide substantial benefits in terms of performance and battery life, it means Mycelium is in a position collect identifying information about their users. While Mycelium has very good support for Tor in their wallet, connecting to Mycelium servers via Tor only partially mitigates this privacy weakness.

##Questionnaire Response ##

Mycelium's responses are listed in bold.

1: Please classify your application as one of the three categories:
  * Wallet: all of the private keys needed to create a blockchain transaction are under the exclusive control of the user
  * Pseudo-wallet: none of the private keys needed to create a blockchain transaction are under the exclusive control of the user
  * Hybrid wallet: some portion of the private keys needed to create a blockchain transaction are under the exclusive control of the user

**Wallet: all of the private keys needed to create a blockchain transaction are under the exclusive control of the user**

2: Does your application provide any type of visual warning to the user when events which may reduce their privacy or safety occur, such as:
  * Receiving funds to an address which has previously received incoming transactions

**No**

  * Backups have been invalidated by new receiving or change address creation

**No (we use HD wallets, so this isn't an issue, but we warn if single address accounts have not been backed up)**

  * If the wallet supports mixing, a proposed mixing transaction is easily reversible

**Wallet does not support mixing yet**

  * An outgoing transaction sends funds to a previously-used address

**No, but previous addresses are not displayed, or available to send to from within the wallet. A new address is always used.**

  * An outgoing transaction links inputs from multiple addresses

**No**

  * Network connectivity to peers or dedicated balance servers is not routed through an anonymous channel

**Yes. If Tor is selected as a connection method, the connection either goes through to our .onion address, or fails completely.**

  * An outgoing transaction links inputs from multiple accounts/identities

**Our wallet can't send from multiple accounts. Only one account at a time.**

3: Does your application’s backup process involve any activity which may be visible to an external network observer?

**No. Backup is done by displaying a 12 word seed, on a protected (can't screenshot) display, one word at a time.**

4: Does your application take positive steps to make change outputs indistinguishable from spending outputs, such as:
  * Randomizing the number of change outputs

**We have only one change output, but always to a new address**

  * Randomizing the position of the change output(s)

**If you mean randomizing the position of the two addresses, change and sent, then yes**

  * Selecting sufficient input value such that the change output(s) closely resemble the size of the desired spend

**No**

  * Intentionally creating “decoy” change outputs that have a low number of significant digits

**No**

5: If your application includes mixing functionality:
  * Is it possible for a malicious participant in the mix to steal funds?
  * Is it possible for any participant in the mix to retain information which correlates outputs to their corresponding inputs?

**(N/A but CoinShuffle will be implemented, so use that for reference when done)**

6: If your application obtains balance information from dedicated servers:

**(It does...)**

  * Is it possible to operate the dedicated servers in a manner which correlates:
    * A user’s receiving or change address to another receiving or change address in the same wallet

**Not for spending, since all signing is done on the wallet, and address information is not tracked. We can only correlate addresses where more than one is used for inputs, same as anyone else can by looking at transactions on the blockchain. However, for balance lookups yes, since we don't have a good way to anonymize that yet (bloom filters aren't a good solution either), but we don't keep logs of balance lookups**

    * Any of the above with a public IP address

**If connecting through clearweb, it's possible, but we don't log IP addresses either. And since we also added full support for Tor, users can completely hide their IP addresses if they want to.**

    * Any of the above with a registered account 

**There are no registered accounts in our app, or any identifiable information besides addresses**

    * Any of the above with a persistent software or hardware fingerprint

**No**

7: If your application obtains balance information by uploading a filter to network peers:
  * Are filters ever updated in a manner that allows the peer to correlate the old and new filter with the same connection?

**(N/A)**

8: Does your application take positive steps to route outgoing transactions through different path to the network than the path via which it receives balance and incoming transaction information?

**No, all incoming and outgoing transaction information is broadcast through our servers, though that limits such tracking to just knowing that the user is a Mycelium user.**

9: If your application supports multiple accounts/identities:
  * Does your application take positive steps to route balance, incoming and outgoing transaction information through different network paths for each account/identity?

**No, all balance information and signed transactions go through our server**

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
