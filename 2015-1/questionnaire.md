Bitcoin Wallet Privacy Questionnaire
====================================

This questionnaire was sent to the developers of each of the wallets included in the 2015-1 wallet rating exercise in order to more easily gather information about the behavior of the wallet that might otherwise be difficult to obtain.

##Questions##

1. Please classify your application as one of the three categories:
  * **Wallet**: all of the private keys needed to create a blockchain transaction are under the exclusive control of the user
  * **Pseudo-wallet**: none of the private keys needed to create a blockchain transaction are under the exclusive control of the user
  * **Hybrid wallet**: some portion of the private keys needed to create a blockchain transaction are under the exclusive control of the user
2. Does your application provide any type of visual warning to the user when events which may reduce their privacy or safety occur, such as:
  * Receiving funds to an address which has previously received incoming transactions
  * Backups have been invalidated by new receiving or change address creation
  * If the wallet supports mixing, a proposed mixing transaction is easily reversible
  * An outgoing transaction sends funds to a previously-used address
  * An outgoing transaction links inputs from multiple addresses
  * Network connectivity to peers or dedicated balance servers is not routed through an anonymous channel
  * An outgoing transaction links inputs from multiple accounts/identities
3. Does your application’s backup process involve any activity which may be visible to an external network observer?
4. Does your application take positive steps to make change outputs indistinguishable from spending outputs, such as:
  * Randomizing the number of change outputs
  * Randomizing the position of the change output(s)
  * Selecting sufficient input value such that the change output(s) closely resemble the size of the desired spend
  * Intentionally creating “decoy” change outputs that have a low number of significant digits
5. If your application includes mixing functionality:
  * Is it possible for a malicious participant in the mix to steal funds?
  * Is it possible for any participant in the mix to retain information which correlates outputs to their corresponding inputs?
6. If your application obtains balance information from dedicated servers:
  * Is it possible to operate the dedicated servers in a manner which correlates:
    * A user’s receiving or change address to another receiving or change address in the same wallet
    * Any of the above with a public IP address
    * Any of the above with a registered account 
    * Any of the above with a persistent software or hardware fingerprint
7. If your application obtains balance information by uploading a filter to network peers:
  * Are filters ever updated in a manner that allows the peer to correlate the old and new filter with the same connection?
8. Does your application take positive steps to route outgoing transactions through different path to the network than the path via which it receives balance and incoming transaction information?
9. Does your application take positive steps to route outgoing transactions through different path to the network than the path via which it receives balance and incoming transaction information?
  * Does your application take positive steps to route outgoing transactions through different path to the network than the path via which it receives balance and incoming transaction information?



