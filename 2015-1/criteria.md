Bitcoin Wallet Privacy Ratings Criteria
=======================================

This document outlines the OBPP criteria for rating the privacy strength of Bitcoin wallets. Each item represents an objectively-measurable test of how well a rated wallet implements countermeasures for the attacks identified in the [threat model](threat model.wiki). The result of each test is converted into a numeric score via a method decribed below or in the [methodology](methodology.md).

Our metrics are based on feature completeness and user experience. To evaluate user experience, we utilize a "minimum number of clicks to perform action" metric. This metric is easily standardized between wallets, minimizes subjectivity, and can be measured by a single tester.

Each sub-category of privacy, such as "Change Address Generation," is broken down into between one and three areas of consideration, including usability, quality, and user feedback.

## Criteria

<ol type="I">
	<li><strong>Receiving Addresses</strong>
		<ol type="A">
			<li><em>Generation</em>
				<ol>
					<li>Usability:
						<ol type="a">
							<li>Number of clicks required to deviate from the default receiving functionality and generate a new receiving address for an existing wallet (8.89%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Receiving addresses are hidden from the default view once they have been used? (3.11%)</li>
							<li>Preemptively indicates a loss of privacy when user elects to receive funds at a previously-used addresses? (4.67%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Backup</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks to backup a newly-generated receiving address from an existing wallet (worst case), from the default window/authenticated home page (1.39%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Does the backup process leak information about wallet addresses (e.g. each time a new change address is created on-demand, an email backup is triggered immediately)? (1.39%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Indicates a reduction in wallet safety when receiving address backups are stale, or uses eternal backups? (1.11%)</li>
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
							<li>Number of clicks required to deviate from the default change functionality and receive change at a newly generated address (5.95%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>The position of the change output(s) in the transaction is random? (2,98%)</li>
							<li>One or more change outputs are created which are close to the value of the desired spend? (1.98%)</li>
							<li>Some change output values are intentionally set to “round numbers” (a.k.a low number of significant digits)? (0.99%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Change addresses are hidden from the normal receiving workflow by default to discourage using them as receiving addresses? (1.90%)</li>
							<li>Preemptively indicates a loss of privacy when user elects to reuse change addresses as receiving addresses? (2.86%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Backup</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks to backup a newly-generated change address from an existing wallet (worst case), apart from the sending workflow (1.39%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Backups can occur offline, or are encrypted client-side with data that only the user controls e.g. password? (1.39%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Indicates a reduction in wallet safety when change address backups are stale, or uses eternal backups? (1.11%)</li>
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
							<li>Number of clicks required by user for inputs/outputs to be mixed with one or more other users (2.38%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Average number of other users whose funds are mixed with yours when sending through a mixing process (0.79%)</li>
							<li>Mixing is secure against correlation attacks by the facilitator? (0.79%)</li>
							<li>Mixing is secure against theft of funds? (0.79%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Warns the user when a proposed mix is easy to reverse? (1.90%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Address Reuse</em>
				<ol type="1">
					<li>Feedback:
						<ol type="a">
							<li>Warns user when sending to an address that the user has sent to before? (3.89%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Input Merging</em>
				<ol type="1">
					<li>Quality:
						<ol type="a">
							<li>When an outgoing transaction must merge inputs, and when mixing is not being used, is the transaction constructed in a way that plausibly resembles a mixing transaction? (3.33%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Outside of a mixing transaction, preemptively indicates a loss of privacy when merging inputs from different addresses in the same transaction? (2.22%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Identity Separation</em>
				<ol type="1">
					<li>Quality:
						<ol type="a">
							<li>Avoids creating transactions which contain inputs from different identity containers, except optionally if the user has intentionally overridden this behavior? (6.67%)</li>
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
							<li>Number of clicks required by user to generate a ECDH receiving address, from the default window/authenticated home page. (5.56%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Receiver Identity</em>
				<ol type="1">
					<li>Quality:
						<ol type="a">
							<li>Wallet avoids leaking information about recipients via an external identity lookup? (5.56%)</li>
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
							<li>Number of clicks required by user to connect to the source of balance information without leaking their identity over the network (3.97%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Is balance information obtained in a manner which avoids leaking the addresses in a wallet to network peers? (3.97%)
								<ul>
									<li>100: Full node - the wallet is part of, or works with, a full node under the user’s exclusive control</li>
									<li>75: Carefully filtered - address filters are used, but filters are never updated and when a new one is require it is registered with a brand new peer</li>
									<li>50: Unsafely filtered - address filters are used, and they are updated or reuse peers.</li>
									<li>0: Unfiltered - Balance is obtained from a peer which can easily connect wallet addresses to a specific connection/wallet</li>
								</ul>
							</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Client provides a visual indication if the balance information is not being obtained through an anonymizing network, including IP address information? (3.17%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Outgoing Transactions</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks required by user to route outgoing transactions through an anonymizing network (1.98%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Are outgoing transactions routed through a different entry point into the network than the source of balance information? (1.98%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Client provides a visual indication if outgoing transactions are not being routed through an anonymizing network, including IP address information? (1.59%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Identity Separation</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks to create a new identity container ( 1.32%)</li>
							<li>Number of clicks to assign an imported address to an identity container (0.66%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Avoids including addresses from multiple identity containers in the same address filter? (0.99%)</li>
							<li>Avoids broadcasting outgoing transactions from different identity containers via the same network access path? (0.99%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Visually indicates to user when inputs from different accounts/pockets are merged before the transaction is broadcast, or prohibits this operation entirely?(1.59%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Operating System Support </em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Compatible with latest version of Tails? (2.78%)
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

