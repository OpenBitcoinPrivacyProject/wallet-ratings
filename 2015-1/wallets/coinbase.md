Bitcoin Wallet Privacy Rating - Spring 2015
============================================

<dl>
    <dt>Rank</dt>
    <dd></dd>
    <dt>Name</dt>
    <dd>Coinbase</dd>
    <dt>Type</dt>
    <dd>Pseudo-wallet</dd>
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

