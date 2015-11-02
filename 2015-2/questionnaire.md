Bitcoin Wallet Privacy Questionnaire
====================================

This questionnaire was sent to the developers of each of the wallets included in the 2015-2 wallet rating exercise in order to more easily gather information about the behavior of the wallet that might otherwise be difficult to obtain.

##Questions##

### Transaction Formatting

1. Does your application take any steps to create ambiguity between transactions which unavoidably spend from multiple addresses at the same time and intentional mixing transactions?
2. What algorithms does your application use for ordering inputs and outputs in a transaction? In particular, how do you handle the change output and do you take into account common practices of other wallet applications when determining ordering?
3. Does your application minimise the harmful effects of address reuse by spending every spendable input (“sweeping”) from an address when a transaction is created?
4. Does your application fully implement BIP 62?
  
  ### Mixing
  
5. If your application supports mixing:
    a. What is the average number of participants a user can expect to interact with on a typical join transaction?
    b. Does your application attempt to construct join transactions in a way that avoids distinguishing them from non-join transactions?
    c. Does your application perform any kind of reversibility analysis on join transactions prior to presenting them to the user for confirmation?
    d. Is the mixing technique employed secure against correlation attacks by the facilitator, such as a CoinJoin server or off-chain mixing service?
    e. Is the mixing technique employed secure against theft of funds by the facilitator or its participants?
  
  ### Donations
  
6. If your application has a fee or donation to the developers feature:
    a. What steps do you take to make the donations indistinguishable from regular spend in terms of output sizes and destination addresses?
  
  ### Balance Queries and Tx Broadcasting
  
7. Please describe how your application obtains balance information in terms of how queries from the user’s device can reveal a connection between the addresses in their wallet.
    a. Does the application keep a complete copy of the blockchain locally (full node)?
    b. Does the user’s device provide a filter which matches some fraction of the blockchain while providing a false positive rate (bloom or prefix filters)?
        i. If so, approximately what fraction of the blockchain does the filter match in a default configuration (0% - 100%)?
    c. Does the user’s device query all of their addresses at the same time?
    d. Does the user’s device query addresses individually in a manner that does not allow the query responder to correlate queries for different addresses?
    e. Can users opt to obtain their balance information via Tor (or equivalent means)?
8. Does the applications route outgoing transactions independently from the manner in which it obtains balance information? Can users opt to have their transactions submitted to the Bitcoin network via Tor (or an equivalent means) independently of how they obtain their balance information?
9. If your application supports multiple identities/wallets, does each one connect to the network as if it were completely independent from the other?
    a. Does the application ever request balance information for addresses belonging to multiple identities in the same network query?
    b. Are outgoing transactions from multiple identities routed independently of each other to the Bitcoin network?
    c. When an identity/wallet is deleted, does the deletion process eliminate all evidence from the user's device that the wallet was previously installed?
  
  ### Network Privacy
  
10. When a user performs a backup operation for their wallet, does this generate any automatic network activity, such as a web query or email?
11. Does your application perform any lookup external to the user’s device related to identifying transaction senders or recipients?
12. Does you application connect to known endpoints which would be visible to an ISP, such as your domain?
13. If your application connects directly to nodes in the Bitcoin P2P network, does it either use an unremarkable user agent string (Bitcoin Core. BitcoinJ, etc), or randomize its user agent on each connection?
  
  ### Physical Access
  
14. Does the application uninstall process for your application eliminate all evidence from the user's device that the application was previously installed? Does it also eliminate wallet data?
15. Does your application use techniques such as steganography to store persistent wallet metadata in a form not identifiable as belong to a Bitcoin wallet application?
16. Please describe the degree to which users can use passwords/PINs to protect their data:
    a. Can the user set a password/PIN to protect their private keys?
    b. Can the user set a password/PIN to protect their public keys and balance information?
    c. Can the user set a password/PIN to encrypt other wallet metadata, such as address books and transaction notes?
    d. Does the application use a single password/PIN to cover all protected data, or does it allow the use of multiple passwords/PINs?
  
  ### Custodianship
  
17. Do you as a wallet provider ever have access to unencrypted copies of the user’s private keys, public keys, or any other wallet metadata which may be used to associate a user with their transactions or balances?
  
  ### Telemetry Data
  
18. If your application reports telemetry data, such as usage information or automatic crash reporting, does the user have the opportunity to review and approve all information transmitted before it is sent?
  
  ### Source Code and Building
  
19. Can a user of your application compile the application themselves in a manner that produces a binary version identical to the version you distribute (deterministic build system)?
