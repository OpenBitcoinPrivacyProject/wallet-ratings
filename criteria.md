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

<ol type="I">
	<li><strong>Receiving Addresses</strong>
		<ol type="A" style="list-style-type:upper-alpha">
			<li><em>Generation</em>
				<ol>
					<li>Usability:
						<ol type="a">
							<li>Number of clicks required to deviate from the default receiving functionality and generate a new receiving address for an existing wallet.</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Receiving addresses are hidden from the default view once they have been used?</li>
							<li>Preemptively indicates a loss of privacy when user elects to receive funds at a previously-used addresses?</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Backup</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks to backup a newly-generated receiving address from an existing wallet (worst case), from the default window/authenticated home page.</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Does the backup process leak information about wallet addresses (e.g. each time a new change address is created on-demand, an email backup is triggered immediately)?</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Indicates a reduction in wallet safety when receiving address backups are stale?</li>
						</ol>
					</li>
				</ol>
			</li>
		</ol>
	</li>
	<li><strong>Change Addresses</strong>
		<ol type="A">
			<li><em>Generation</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks required to deviate from the default change functionality and receive change at a newly generated address.</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>The position of the change output(s) in the transaction is random?</li>
							<li>The size and number of change outputs is chosen to make the change outputs resemble the desired spend?</li>
							<li>Some change output values are intentionally set to “round numbers” (a.k.a low number of significant digits)?</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Change addresses are hidden from the normal receiving workflow by default to discourage using them as receiving addresses?</li>
							<li>Preemptively indicates a loss of privacy when user elects to reuse change addresses as receiving addresses?</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Backup</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks to backup a newly-generated change address from an existing wallet (worst case), apart from the sending workflow.</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Backups can occur offline, or are encrypted client-side with data that only the user controls e.g. password?</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Indicates a reduction in wallet safety when change address backups are stale?</li>
						</ol>
					</li>
				</ol>
			</li>
		</ol>
	</li>
	<li><strong>Sender Privacy vs Blockchain Observers</strong>
		<ol type="A">
			<li><em>Mixing</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks required by user for inputs/outputs to be mixed with one or more other users</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Average number of other users whose funds are mixed with yours when sending through a mixing process</li>
							<li>Mixing is secure against correlation attacks by the facilitator</li>
							<li>Mixing is secure against theft of funds</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Warns the user when a proposed mix is easy to reverse?</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Address Reuse</em>
				<ol type="1">
					<li>Feedback:
						<ol type="a">
							<li>Warns user when sending to an address that the user has sent to before?</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Input Merging</em>
				<ol type="1">
					<li>Feedback:
						<ol type="a">
							<li>Outside of a mixing transaction, preemptively indicates a loss of privacy when merging inputs from different addresses in the same transaction?</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Identity Separation</em>
				<ol type="1">
					<li>Quality:
						<ol type="a">
							<li>Avoids creating transactions which contain inputs from different identity containers, except optionally if the user has intentionally overridden this behavior?</li>
						</ol>
					</li>
				</ol>
			</li>
		</ol>
	</li>
	<li><strong>Receiver Privacy</strong>
		<ol type="A">
			<li><em>ECDH Address Support</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks required by user to generate a ECDH receiving address, from the default window/authenticated home page.</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Receiver Identity</em>
				<ol type="1">
					<li>Quality:
						<ol type="a">
							<li>Wallet avoids leaking information about recipients via an external identity lookup?</li>
						</ol>
					</li>
				</ol>
			</li>
		</ol>
	</li>
	<li><strong>Sender Privacy vs Network Observers</strong>
		<ol type="A">
			<li><em>Balance Information</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks required by user to connect to the source of balance information through an anonymizing network</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Is balance information obtained in a manner which avoids leaking the addresses in a wallet to network peers?
								<ul>
									<li>100: Full node - the wallet is part of, or works with, a full node under the user’s exclusive control</li>
									<li>75: Private SPV - address filters are used, but filters are never updated and when a new one is require it is registered with a brand new peer</li>
									<li>50: Non-private SPV - address filters are used, and they are updated or reuse peers.</li>
									<li>0: Non-private - Balance is obtained from a peer which can easily connect wallet addresses to a specific connection/wallet</li>
								</ul>
							</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Client provides a visual indication if the balance information is not being obtained through an anonymizing network, including IP address information</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Outgoing Transactions</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks required by user to route outgoing transactions through an anonymizing network</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Are outgoing transactions routed through a different entry point into the network than the source of balance information?</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Client provides a visual indication if outgoing transactions are not being routed through an anonymizing network, including IP address information</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Identity Separation</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks to import a seed or wallet file into the client.</li>
							<li>Number of clicks to assign an imported address to an identity container</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Avoids including addresses from multiple identity containers in the same address filter?</li>
							<li>Avoids broadcasting outgoing transactions from different identity containers via the same network access path?</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Visually indicates to user when inputs from different accounts/pockets are merged before the transaction is broadcast.</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Operating System Support </em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Compatible with latest version of Tails?
								<ul>
									<li>100: Actually included in the Tails live cd</li>
									<li>75: Program and any dependencies are packaged into a single file which can be easily installed</li>
									<li>50: Installation is possible, but requires multiple complex steps</li>
									<li>0: WIll not run on Tails</li>
								</ul>
							</li>
						</ol>
					</li>
				</ol>
			</li>
		</ol>
	</li>
</ol>
