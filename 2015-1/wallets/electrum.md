Bitcoin Wallet Privacy Rating - Spring 2015
============================================

<dl>
    <dt>Rank</dt>
    <dd></dd>
    <dt>Name</dt>
    <dd>Electrum</dd>
    <dt>Type</dt>
    <dd>Wallet</dd>
    <dt>Tested Version</dt>
    <dd>2.0.3 (linux)</dd>
    <dt>Supported Platforms</dt>
    <dd>Android, Linux, OSX, Windows</dd>
    <dt>Score</dt>
    <dd>
        <dl>
            <dt>Overall</dt>
            <dd>4</dd>
            <dt>Quality</dt>
            <dd>5</dd>
            <dt>Usability</dt>
            <dd>3</dd>
            <dt>Feedback</dt>
            <dd>3</dd>
        </dl>
    </dd>
</dl>

##Description##

Electrum is a cross-platform lightweight desktop wallet that has been under active development since November 2011. This wallet uses a deterministic seed to generate all keys, backed up by a 12-word string. Electrum 2.0 now implements BIP32 for this. Instead of downloading the entire blockchain, it connects to federated Electrum servers for transaction and balance data. These connections can easily be made through Tor; Electrum is the only Bitcoin wallet to be included by default with the privacy-focused Linux distro Tails. Electrum can also do two-factor authentication, and provides compatibility with hardware wallets such as Trezor.

Because the Electrum client connects to servers for data, users sacrifice privacy and must rely on trust in the blockchain information received. Because of the networking model, Electrum servers can identify relationships between addresses through observing requests for balance information and transaction broadcasts. Electrum could be improved through the implementation of features also lacking in many other wallets, including ECDH address and mixing support, and by providing more detailed warnings to users before privacy violations take place.

##Questionnaire Response ##

The developers of Electrum did not respond to the OBPP questionnaire.

##Question Scores##

<dl>
    <dt>I A 1 a): Number of clicks required to deviate from the default receiving functionality and generate a new receiving address for an existing wallet.</dt>
    <dd>8.89</dd>
    <dt>I A 2 a): Receiving addresses are hidden from the default view once they have been used?</dt>
    <dd>3.11</dd>
    <dt>I A 2 b): Preemptively indicates a loss of privacy when user elects to receive funds at a previously-used addresses?</dt>
    <dd>0</dd>
    <dt>I B 1 a): Number of clicks to backup a newly-generated receiving address from an existing wallet (worst case), from the default window/authenticated home page.</dt>
    <dd>1.39</dd>
    <dt>I B 2 a): Does the backup process leak information about wallet addresses (e.g. each time a new change address is created on-demand, an email backup is triggered immediately)?</dt>
    <dd>1.39</dd>
    <dt>I B 3 a): Indicates a reduction in wallet safety when receiving address backups are stale, or uses eternal backups?</dt>
    <dd>1.11</dd>
    <dt>II A 1 a): Number of clicks required to deviate from the default change functionality and receive change at a newly generated address</dt>
    <dd>5.95</dd>
    <dt>II A 2 a): The position of the change output(s) in the transaction is random?</dt>
    <dd>2.98</dd>
    <dt>II A 2 b): One or more change outputs are created which are close to the value of the desired spend?</dt>
    <dd>0</dd>
    <dt>II A 2 c): Some change output values are intentionally set to “round numbers” (a.k.a low number of significant digits)?</dt>
    <dd>0</dd>
    <dt>II A 3 a): Change addresses are hidden from the normal receiving workflow by default to discourage using them as receiving addresses?</dt>
    <dd>1.9</dd>
    <dt>II A 3 b): Preemptively indicates a loss of privacy when user elects to reuse change addresses as receiving addresses?</dt>
    <dd>2.86</dd>
    <dt>II B 1 a): Number of clicks to backup a newly-generated change address from an existing wallet (worst case), apart from the sending workflow</dt>
    <dd>1.39</dd>
    <dt>II B 2 a): Backups can occur offline, or are encrypted client-side with data that only the user controls e.g. password?</dt>
    <dd>1.39</dd>
    <dt>II B 3 a): Indicates a reduction in wallet safety when change address backups are stale, or uses eternal backups?</dt>
    <dd>1.11</dd>
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
    <dd>5.56</dd>
    <dt>V A 1 a): Number of clicks required by user to connect to the source of balance information without leaking their identity over the network</dt>
    <dd>0.99</dd>
    <dt>V A 2 a): Is balance information obtained in a manner which avoids leaking the addresses in a wallet to network peers?</dt>
    <dd>0</dd>
    <dt>V A 3 a): Client provides a visual indication if the balance information is not being obtained through an anonymizing network, including IP address information?</dt>
    <dd>0</dd>
    <dt>V B 1 a): Number of clicks required by user to route outgoing transactions through an anonymizing network</dt>
    <dd>0.5</dd>
    <dt>V B 2 a): Are outgoing transactions routed through a different entry point into the network than the source of balance information?</dt>
    <dd>0</dd>
    <dt>V B 3 a): Client provides a visual indication if outgoing transactions are not being routed through an anonymizing network, including IP address information?</dt>
    <dd>0</dd>
    <dt>V C 1 a): Number of clicks to create a new identity container</dt>
    <dd>0.13</dd>
    <dt>V C 1 b): Number of clicks to assign an imported address to an identity container</dt>
    <dd>0.66</dd>
    <dt>V C 2 a): Avoids including addresses from multiple identity containers in the same address filter?</dt>
    <dd>0</dd>
    <dt>V C 2 b): Avoids broadcasting outgoing transactions from different identity containers via the same network access path?</dt>
    <dd>0</dd>
    <dt>V C 3 a): Visually indicates to user when inputs from different accounts/pockets are merged before the transaction is broadcast, or prohibits this operation entirely.</dt>
    <dd>1.59</dd>
    <dt>V D 1 a): Compatible with latest version of Tails?</dt>
    <dd>2.78</dd>
</dl>
