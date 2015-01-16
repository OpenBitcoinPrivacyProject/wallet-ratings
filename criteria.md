Bitcoin Wallet Privacy Ratings Criteria
=======================================

## Authors

Open Bitcoin Privacy Project (OBPP) 2015
Kristov Atlas, Justus Ranvier, Chris Pacia, Samuel Patterson

## Contact

* w: http://www.openbitcoinprivacyproject.org/connect/
* e: contact [at] openbitcoinprivacyproject [dot] org
* t: [@obpp_org](https://twitter.com/obpp_org)

## Description

Version 0.1 (Request for Public Comment)

This document outlines the OBPP criteria for rating the privacy strength of Bitcoin wallets. A separate document will describe the relative importance of each criterion and how per-wallet scores are calculated. 

Our metrics are based on feature completeness and user experience. To evaluate user experience, we utilize a "minimum number of clicks to perform action" metric. This metric is easily standardized between wallets, minimizes subjectivity, and can be measured by a single tester.

Each sub-category of privacy, such as "Change Address Generation," is broken down into between one and three areas of consideration, including usability, quality, and user feedback.

## Criteria

I. Receiving Addresses
  A. Generation
    1. Usability:
      a) Number of clicks required to deviate from the default receiving functionality and generate a new receiving address for an existing wallet.
    2. Feedback:
      a) Receiving addresses are hidden from the default view once they have been used?
	  b) Preemptively indicates a loss of privacy when user elects to receive funds at a previously-used addresses?
  B. Backup
    1. Usability:
      a) Number of clicks to backup a newly-generated receiving address from an existing wallet (worst case), from the default window/authenticated home page.
    2. Quality:
      a) Does the backup process leak information about wallet addresses (e.g. each time a new change address is created on-demand, an email backup is triggered immediately)?
    3. Feedback:
      a) Indicates a reduction in wallet safety when receiving address backups are stale?
II. Change Addresses
  A. Generation
    1. Usability:
      a) Number of clicks required to deviate from the default change functionality and receive change at a newly generated address.
    2. Quality:
      a) The position of the change output(s) in the transaction is random?
      b) The size and number of change outputs is chosen to make the change outputs resemble the desired spend?
      c) Some change output values are intentionally set to “round numbers” (a.k.a low number of significant digits)?
    3. Feedback:
      a) Change addresses are hidden from the normal receiving workflow by default to discourage using them as receiving addresses?
      b) Preemptively indicates a loss of privacy when user elects to reuse change addresses as receiving addresses?
  B. Backup
    1. Usability:
	  a) Number of clicks to backup a newly-generated change address from an existing wallet (worst case), apart from the sending workflow.
    2. Quality:
      a) Backups can occur offline, or are encrypted client-side with data that only the user controls e.g. password?
    3. Feedback:
      a) Indicates a reduction in wallet safety when change address backups are stale?
III. Sender Privacy vs Blockchain Observers
  A. Mixing
    1. Usability:
      a) Number of clicks required by user for inputs/outputs to be mixed with one or more other users
    2. Quality:
      a) Average number of other users whose funds are mixed with yours when sending through a mixing process
      b) Mixing is secure against correlation attacks by the facilitator
      c) Mixing is secure against theft of funds
    3. Feedback:
	  a) Warns the user when a proposed mix is easy to reverse?
  B. Address Reuse 
    1. Feedback:
	  a) Warns user when sending to an address that the user has sent to before?
  C. Input Merging 
    1. Feedback:
	  a) Outside of a mixing transaction, preemptively indicates a loss of privacy when merging inputs from different addresses in the same transaction?
  D. Identity Separation
    1. Quality:
      a) Avoids creating transactions which contain inputs from different identity containers, except optionally if the user has intentionally overridden this behavior?
IV. Receiver Privacy
  A. ECDH Address Support
    1. Usability:
	  a) Number of clicks required by user to generate a ECDH receiving address, from the default window/authenticated home page.
  B. Receiver Identity 
    1. Quality:
	  a) Wallet avoids leaking information about recipients via an external identity lookup?
V. Sender Privacy vs Network Observers
  A. Balance Information 
    1. Usability:
      a) Number of clicks required by user to connect to the source of balance information through an anonymizing network
    2. Quality:
	  a) Is balance information obtained in a manner which avoids leaking the addresses in a wallet to network peers?
        (1) 100: Full node - the wallet is part of, or works with, a full node under the user’s exclusive control
        (2) 75: Private SPV - address filters are used, but filters are never updated and when a new one is require it is registered with a brand new peer
        (3) 50: Non-private SPV - address filters are used, and they are updated or reuse peers.
        (4) 0: Non-private - Balance is obtained from a peer which can easily connect wallet addresses to a specific connection/wallet
    3. Feedback:
      a) Client provides a visual indication if the balance information is not being obtained through an anonymizing network, including IP address information
  B. Outgoing Transactions 
    1. Usability:
      a) Number of clicks required by user to route outgoing transactions through an anonymizing network
    2. Quality:
      a) Are outgoing transactions routed through a different entry point into the network than the source of balance information?
    3. Feedback:
      a) Client provides a visual indication if outgoing transactions are not being routed through an anonymizing network, including IP address information
  C. Identity Separation 
    1. Usability:
      a) Number of clicks to import a seed or wallet file into the client.
      b) Number of clicks to assign an imported address to an identity container
    2. Quality:
      a) Avoids including addresses from multiple identity containers in the same address filter?
      b) Avoids broadcasting outgoing transactions from different identity containers via the same network access path?
    3. Feedback:
      a) Visually indicates to user when inputs from different accounts/pockets are merged before the transaction is broadcast.
  D. Operating System Support 
    1. Usability:
      a) Compatible with latest version of Tails?
        (1) 100: Actually included in the Tails live cd
        (2) 75: Program and any dependencies are packaged into a single file which can be easily installed
        (3) 50: Installation is possible, but requires multiple complex steps
        (4) 0: WIll not run on Tails
