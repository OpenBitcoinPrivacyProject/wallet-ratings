Bitcoin Wallet Privacy Rating - Spring 2015
============================================

<dl>
    <dt>Rank</dt>
    <dd></dd>
    <dt>Name</dt>
    <dd>Airbitz</dd>
    <dt>Type</dt>
    <dd>Wallet</dd>
    <dt>Version</dt>
    <dd><1.4.6 (android)/dd>
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

The AirBitz Bitcoin Wallet, first released in early 2014, is a light client available for Android and iOS mobile devices. The mobile app features sending and receiving functionality, as well as a Bitcoin merchant directory that allows users to search for nearby Bitcoin-accepting businesses, and which integrates into the sending functionality. Much of the Bitcoin-specific code is based on the Libbitcoin library.

AirBitz was one of the first mobile wallets to use an HD architecture, which permits it to easily protect user privacy by automatically generating new addresses for receipt of funds and change. The HD architecture also allows AirBitz more advanced support for multiple accounts than many of its competitors. Additional controls are needed for AirBitz to thoroughly protect blockchain privacy, including randomizing output indexes and mixing funds. Balance information and transaction broadcasting are conducted through one or more trusted Obelisk servers, which can lead to a degradation in privacy. Since access to privacy networks such as Tor are limited on mobile devices, AirBitz users have limited capacity to take advantage of network-based protections, and the wallet does not integrate support for such proxies.

##Questionnaire Response ##

Airbitz's responses are listed in bold.

1: Please classify your application as one of the three categories:
  * Wallet: all of the private keys needed to create a blockchain transaction are under the exclusive control of the user
  * Pseudo-wallet: none of the private keys needed to create a blockchain transaction are under the exclusive control of the user
  * Hybrid wallet: some portion of the private keys needed to create a blockchain transaction are under the exclusive control of the user

**a** (wallet)

2: Does your application provide any type of visual warning to the user when events which may reduce their privacy or safety occur, such as:
  * Receiving funds to an address which has previously received incoming transactions
  * Backups have been invalidated by new receiving or change address creation
  * If the wallet supports mixing, a proposed mixing transaction is easily reversible
  * An outgoing transaction sends funds to a previously-used address
  * An outgoing transaction links inputs from multiple addresses
  * Network connectivity to peers or dedicated balance servers is not routed through an anonymous channel
  * An outgoing transaction links inputs from multiple accounts/identities

**(None of above)**

3: Does your application’s backup process involve any activity which may be visible to an external network observer?

**Not sure what is meant by this. Network observer can see transmission of fully encrypted data**

4: Does your application take positive steps to make change outputs indistinguishable from spending outputs, such as:
  * Randomizing the number of change outputs

**No, but in pipeline**

  * Randomizing the position of the change output(s)

**No, but in pipeline**

  * Selecting sufficient input value such that the change output(s) closely resemble the size of the desired spend

**No, but in pipeline**

  * Intentionally creating “decoy” change outputs that have a low number of significant digits

**No**

5: If your application includes mixing functionality:

**No**

  * Is it possible for a malicious participant in the mix to steal funds?
  * Is it possible for any participant in the mix to retain information which correlates outputs to their corresponding inputs?
 
6: If your application obtains balance information from dedicated servers:

**No. Some Airbitz and some non-airbitz servers. All peer-to-peer open source servers**

  * Is it possible to operate the dedicated servers in a manner which correlates:
    * A user’s receiving or change address to another receiving or change address in the same wallet

**No**

    * Any of the above with a public IP address

**Yes**

    * Any of the above with a registered account 

**No**

    * Any of the above with a persistent software or hardware fingerprint

**No**

7: If your application obtains balance information by uploading a filter to network peers:

**It does not. in pipeline via prefix queries**

  * Are filters ever updated in a manner that allows the peer to correlate the old and new filter with the same connection?

8: Does your application take positive steps to route outgoing transactions through different path to the network than the path via which it receives balance and incoming transaction information?

**Yes, sends and receives have different paths**

9: If your application supports multiple accounts/identities:
  * Does your application take positive steps to route balance, incoming and outgoing transaction information through different network paths for each account/identity?

**Accounts have no links at all to balance and incoming/outgoing transactions.**

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
