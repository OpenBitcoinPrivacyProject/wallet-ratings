Bitcoin Wallet Privacy Rating - Spring 2015
============================================

<dl>
    <dt>Rank</dt>
    <dd></dd>
    <dt>Name</dt>
    <dd>Mycelium</dd>
    <dt>Type</dt>
    <dd>Wallet</dd>
    <dt>Tested Version</dt>
    <dd>2.2.0 (android)</dd>
    <dt>Supported Platforms</dt>
    <dd>Android, iOS</dd>
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

Many long-time Bitcoin users have regarded Mycelium Bitcoin Wallet as the leading Android wallet throughout 2014 and in to 2015. In terms of privacy features, Mycelium implements HD wallets based on BIP44, including multiple account support, and does not encourage address reuse by default. Mycelium is notable for including Local Trader, a built-in P2P system for finding traders to exchange between local currencies and Bitcoin.

Mycelium is the best performer of all mobile wallets in this round of rating by OBPP, but its score suffers from the method via which the wallet obtains balance information. Mycelium wallets obtain their balance information from dedicated Mycelium servers instead of connecting to Bitcoin network peers. While this does provide substantial benefits in terms of performance and battery life, this practice places Mycelium in a position to collect identifying information about their users. While Mycelium has very good support for Tor in their wallet, connecting to Mycelium servers via Tor only partially mitigates this privacy weakness.

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
    <dt>I A 1 a): Number of clicks required to deviate from the default receiving functionality and generate a new receiving address for an existing wallet.</dt>
    <dd></dd>
    <dt>I A 2 a): Receiving addresses are hidden from the default view once they have been used?</dt>
    <dd></dd>
    <dt>I A 2 b): Preemptively indicates a loss of privacy when user elects to receive funds at a previously-used addresses?</dt>
    <dd></dd>
    <dt>I B 1 a): Number of clicks to backup a newly-generated receiving address from an existing wallet (worst case), from the default window/authenticated home page.</dt>
    <dd></dd>
    <dt>I B 2 a): Does the backup process leak information about wallet addresses (e.g. each time a new change address is created on-demand, an email backup is triggered immediately)?</dt>
    <dd></dd>
    <dt>I B 3 a): Indicates a reduction in wallet safety when receiving address backups are stale, or uses eternal backups?</dt>
    <dd></dd>
    <dt>II A 1 a): Number of clicks required to deviate from the default change functionality and receive change at a newly generated address</dt>
    <dd></dd>
    <dt>II A 2 a): The position of the change output(s) in the transaction is random?</dt>
    <dd></dd>
    <dt>II A 2 b): One or more change outputs are created which are close to the value of the desired spend?</dt>
    <dd></dd>
    <dt>II A 2 c): Some change output values are intentionally set to “round numbers” (a.k.a low number of significant digits)?</dt>
    <dd></dd>
    <dt>II A 3 a): Change addresses are hidden from the normal receiving workflow by default to discourage using them as receiving addresses?</dt>
    <dd></dd>
    <dt>II A 3 b): Preemptively indicates a loss of privacy when user elects to reuse change addresses as receiving addresses?</dt>
    <dd></dd>
    <dt>II B 1 a): Number of clicks to backup a newly-generated change address from an existing wallet (worst case), apart from the sending workflow</dt>
    <dd></dd>
    <dt>II B 2 a): Backups can occur offline, or are encrypted client-side with data that only the user controls e.g. password?</dt>
    <dd></dd>
    <dt>II B 3 a): Indicates a reduction in wallet safety when change address backups are stale, or uses eternal backups?</dt>
    <dd></dd>
    <dt>III A 1 a): Number of clicks required by user for inputs/outputs to be mixed with one or more other users</dt>
    <dd></dd>
    <dt>III A 2 a): Average number of other users whose funds are mixed with yours when sending through a mixing process</dt>
    <dd></dd>
    <dt>III A 2 b): Mixing is secure against correlation attacks by the facilitator?</dt>
    <dd></dd>
    <dt>III A 2 c): Mixing is secure against theft of funds?</dt>
    <dd></dd>
    <dt>III A 3 a): Warns the user when a proposed mix is easy to reverse?</dt>
    <dd></dd>
    <dt>III B 1 a): Warns user when sending to an address that the user has sent to before?</dt>
    <dd></dd>
    <dt>III C 1 a): When an outgoing transaction must merge inputs, and when mixing is not being used, is the transaction constructed in a way that plausibly resembles a mixing transaction?</dt>
    <dd></dd>
    <dt>III C 2 a): Outside of a mixing transaction, preemptively indicates a loss of privacy when merging inputs from different addresses in the same transaction?</dt>
    <dd></dd>
    <dt>III D 1 a): Avoids creating transactions which contain inputs from different identity containers, except optionally if the user has intentionally overridden this behavior?</dt>
    <dd></dd>
    <dt>IV A 1 a): Number of clicks required by user to generate a ECDH receiving address, from the default window/authenticated home page.</dt>
    <dd></dd>
    <dt>IV B a a): Wallet avoids leaking information about recipients via an external identity lookup?</dt>
    <dd></dd>
    <dt>V A 1 a): Number of clicks required by user to connect to the source of balance information without leaking their identity over the network</dt>
    <dd></dd>
    <dt>V A 2 a): Is balance information obtained in a manner which avoids leaking the addresses in a wallet to network peers?</dt>
    <dd></dd>
    <dt>V A 3 a): Client provides a visual indication if the balance information is not being obtained through an anonymizing network, including IP address information?</dt>
    <dd></dd>
    <dt>V B 1 a): Number of clicks required by user to route outgoing transactions through an anonymizing network</dt>
    <dd></dd>
    <dt>V B 2 a): Are outgoing transactions routed through a different entry point into the network than the source of balance information?</dt>
    <dd></dd>
    <dt>V B 3 a): Client provides a visual indication if outgoing transactions are not being routed through an anonymizing network, including IP address information?</dt>
    <dd></dd>
    <dt>V C 1 a): Number of clicks to create a new identity container</dt>
    <dd></dd>
    <dt>V C 1 b): Number of clicks to assign an imported address to an identity container</dt>
    <dd></dd>
    <dt>V C 2 a): Avoids including addresses from multiple identity containers in the same address filter?</dt>
    <dd></dd>
    <dt>V C 2 b): Avoids broadcasting outgoing transactions from different identity containers via the same network access path?</dt>
    <dd></dd>
    <dt>V C 3 a): Visually indicates to user when inputs from different accounts/pockets are merged before the transaction is broadcast, or prohibits this operation entirely.</dt>
    <dd></dd>
    <dt>V D 1 a): Compatible with latest version of Tails?</dt>
    <dd></dd>
</dl>
