Bitcoin Wallet Privacy Rating - Spring 2015
============================================

<dl>
    <dt>Rank</dt>
    <dd></dd>
    <dt>Name</dt>
    <dd>Coinbase</dd>
    <dt>Type</dt>
    <dd>Pseudo-wallet</dd>
    <dt>Tested Version</dt>
    <dd>March 2015 production website</dd>
    <dt>Supported Platforms</dt>
    <dd>Android, Web</dd>
    <dt>Score</dt>
    <dd>
        <dl>
            <dt>Overall</dt>
            <dd>10</dd>
            <dt>Quality</dt>
            <dd>10</dd>
            <dt>Usability</dt>
            <dd>8</dd>
            <dt>Feedback</dt>
            <dd>7</dd>
        </dl>
    </dd>
</dl>

##Description##

Coinbase is a prominent company in the Bitcoin space that provides Bitcoin exchange, payment processor, and wallet services on the web. Their wallet can be subdivided into two components: a classic version, and Coinbase Vault. Both versions of their wallet functionality are pseudo-wallets in that Coinbase acts as a custodian of private keys, with the exception that Coinbase Vault allows users to retain some of the signing keys required for a transaction. For this assessment of Coinbase, we focused on the class version of the wallet functionality.

Because of the custodial nature of Coinbase’s wallet, users are afforded low privacy. Private keys are generated and held server-side, and the service retains detailed information about incoming and outgoing transactions. Customers must undergo a stringent identification process in order to use the service. The wallet generates new Bitcoin addresses for change, but employs few other basic controls to protect privacy on the blockchain. By design, Coinbase’s servers have the capability to completely track all incoming and outgoing funds, and any metadata stored in the wallet software about those transactions. There are a number of basic improvements that can be made to the classic Coinbase wallet to protect customer privacy without violating Know-Your-Customer guidelines, including discouraging address reuse and randomizing output indexes on the blockchain. In the future, Coinbase can also provide better feedback to users about actions that will degrade their privacy, such as merging inputs when sending bitcoins from their Coinbase wallet.

##Questionnaire Response ##

Coinbase's responses are listed in bold.

1: Please classify your application as one of the three categories:
  * Wallet: all of the private keys needed to create a blockchain transaction are under the exclusive control of the user
  * Pseudo-wallet: none of the private keys needed to create a blockchain transaction are under the exclusive control of the user
  * Hybrid wallet: some portion of the private keys needed to create a blockchain transaction are under the exclusive control of the user

2: Does your application provide any type of visual warning to the user when events which may reduce their privacy or safety occur, such as:
  * Receiving funds to an address which has previously received incoming transactions
  * Backups have been invalidated by new receiving or change address creation
  * If the wallet supports mixing, a proposed mixing transaction is easily reversible
  * An outgoing transaction sends funds to a previously-used address
  * An outgoing transaction links inputs from multiple addresses
  * Network connectivity to peers or dedicated balance servers is not routed through an anonymous channel
  * An outgoing transaction links inputs from multiple accounts/identities

3: Does your application’s backup process involve any activity which may be visible to an external network observer?

4: Does your application take positive steps to make change outputs indistinguishable from spending outputs, such as:
  * Randomizing the number of change outputs
  * Randomizing the position of the change output(s)
  * Selecting sufficient input value such that the change output(s) closely resemble the size of the desired spend
  * Intentionally creating “decoy” change outputs that have a low number of significant digits

5: If your application includes mixing functionality:
  * Is it possible for a malicious participant in the mix to steal funds?
  * Is it possible for any participant in the mix to retain information which correlates outputs to their corresponding inputs?

6: If your application obtains balance information from dedicated servers:
  * Is it possible to operate the dedicated servers in a manner which correlates:
    * A user’s receiving or change address to another receiving or change address in the same wallet
    * Any of the above with a public IP address
    * Any of the above with a registered account 
    * Any of the above with a persistent software or hardware fingerprint

7: If your application obtains balance information by uploading a filter to network peers:
  * Are filters ever updated in a manner that allows the peer to correlate the old and new filter with the same connection?

8: Does your application take positive steps to route outgoing transactions through different path to the network than the path via which it receives balance and incoming transaction information?

9: If your application supports multiple accounts/identities:
  * Does your application take positive steps to route balance, incoming and outgoing transaction information through different network paths for each account/identity?

**Thank you for contacting Coinbase support. We are not accepting survey questions at this time, and kindly decline your offer to be involved with your survey.  Thanks for your interest in Coinbase, best of luck.**

##Question Scores##

<dl>
    <dt>I A 1 a): Number of clicks required to deviate from the default receiving functionality and generate a new receiving address for an existing wallet.</dt>
    <dd>2.22</dd>
    <dt>I A 2 a): Receiving addresses are hidden from the default view once they have been used?</dt>
    <dd>0</dd>
    <dt>I A 2 b): Preemptively indicates a loss of privacy when user elects to receive funds at a previously-used addresses?</dt>
    <dd>0</dd>
    <dt>I B 1 a): Number of clicks to backup a newly-generated receiving address from an existing wallet (worst case), from the default window/authenticated home page.</dt>
    <dd>0</dd>
    <dt>I B 2 a): Does the backup process leak information about wallet addresses (e.g. each time a new change address is created on-demand, an email backup is triggered immediately)?</dt>
    <dd>0</dd>
    <dt>I B 3 a): Indicates a reduction in wallet safety when receiving address backups are stale, or uses eternal backups?</dt>
    <dd>0</dd>
    <dt>II A 1 a): Number of clicks required to deviate from the default change functionality and receive change at a newly generated address</dt>
    <dd>5.95</dd>
    <dt>II A 2 a): The position of the change output(s) in the transaction is random?</dt>
    <dd>0</dd>
    <dt>II A 2 b): One or more change outputs are created which are close to the value of the desired spend?</dt>
    <dd>0</dd>
    <dt>II A 2 c): Some change output values are intentionally set to “round numbers” (a.k.a low number of significant digits)?</dt>
    <dd>0</dd>
    <dt>II A 3 a): Change addresses are hidden from the normal receiving workflow by default to discourage using them as receiving addresses?</dt>
    <dd>0</dd>
    <dt>II A 3 b): Preemptively indicates a loss of privacy when user elects to reuse change addresses as receiving addresses?</dt>
    <dd>2.86</dd>
    <dt>II B 1 a): Number of clicks to backup a newly-generated change address from an existing wallet (worst case), apart from the sending workflow</dt>
    <dd>0</dd>
    <dt>II B 2 a): Backups can occur offline, or are encrypted client-side with data that only the user controls e.g. password?</dt>
    <dd>0</dd>
    <dt>II B 3 a): Indicates a reduction in wallet safety when change address backups are stale, or uses eternal backups?</dt>
    <dd>0</dd>
    <dt>III A 1 a): Number of clicks required by user for inputs/outputs to be mixed with one or more other users</dt>
    <dd>0</dd>
    <dt>III A 2 a): Average number of other users whose funds are mixed with yours when sending through a mixing process</dt>
    <dd>0</dd>
    <dt>III A 2 b): Mixing is secure against correlation attacks by the facilitator?</dt>
    <dd>0</dd>
    <dt>III A 2 c): Mixing is secure against theft of funds?</dt>
    <dd>0</dd>
    <dt>III A 3 a): Warns the user when a proposed mix is easy to reverse?</dt>
    <dd>0</dd>
    <dt>III B 1 a): Warns user when sending to an address that the user has sent to before?</dt>
    <dd>0</dd>
    <dt>III C 1 a): When an outgoing transaction must merge inputs, and when mixing is not being used, is the transaction constructed in a way that plausibly resembles a mixing transaction?</dt>
    <dd>0</dd>
    <dt>III C 2 a): Outside of a mixing transaction, preemptively indicates a loss of privacy when merging inputs from different addresses in the same transaction?</dt>
    <dd>0</dd>
    <dt>III D 1 a): Avoids creating transactions which contain inputs from different identity containers, except optionally if the user has intentionally overridden this behavior?</dt>
    <dd>0</dd>
    <dt>IV A 1 a): Number of clicks required by user to generate a ECDH receiving address, from the default window/authenticated home page.</dt>
    <dd>0</dd>
    <dt>IV B a a): Wallet avoids leaking information about recipients via an external identity lookup?</dt>
    <dd>0</dd>
    <dt>V A 1 a): Number of clicks required by user to connect to the source of balance information without leaking their identity over the network</dt>
    <dd>0</dd>
    <dt>V A 2 a): Is balance information obtained in a manner which avoids leaking the addresses in a wallet to network peers?</dt>
    <dd>0</dd>
    <dt>V A 3 a): Client provides a visual indication if the balance information is not being obtained through an anonymizing network, including IP address information?</dt>
    <dd>0</dd>
    <dt>V B 1 a): Number of clicks required by user to route outgoing transactions through an anonymizing network</dt>
    <dd>0</dd>
    <dt>V B 2 a): Are outgoing transactions routed through a different entry point into the network than the source of balance information?</dt>
    <dd>0</dd>
    <dt>V B 3 a): Client provides a visual indication if outgoing transactions are not being routed through an anonymizing network, including IP address information?</dt>
    <dd>0</dd>
    <dt>V C 1 a): Number of clicks to create a new identity container</dt>
    <dd>0</dd>
    <dt>V C 1 b): Number of clicks to assign an imported address to an identity container</dt>
    <dd>0</dd>
    <dt>V C 2 a): Avoids including addresses from multiple identity containers in the same address filter?</dt>
    <dd>0</dd>
    <dt>V C 2 b): Avoids broadcasting outgoing transactions from different identity containers via the same network access path?</dt>
    <dd>0</dd>
    <dt>V C 3 a): Visually indicates to user when inputs from different accounts/pockets are merged before the transaction is broadcast, or prohibits this operation entirely.</dt>
    <dd>0</dd>
    <dt>V D 1 a): Compatible with latest version of Tails?</dt>
    <dd>0</dd>
</dl>

