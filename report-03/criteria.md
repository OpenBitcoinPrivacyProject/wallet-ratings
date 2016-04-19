Bitcoin Wallet Privacy Ratings Criteria
=======================================

This document outlines the OBPP criteria for rating the privacy strength of Bitcoin wallets. Each item represents an objectively-measurable test of how well a rated wallet implements countermeasures for the attacks identified in the [threat model](threat model.wiki). The result of each test is converted into a numeric score via a method decribed below or in the [methodology](methodology.md).

Our metrics are based on feature completeness and user experience. To evaluate user experience, we utilize a "minimum number of clicks to perform action" metric. This metric is easily standardized between wallets, minimizes subjectivity, and can be measured by a single tester.

Each sub-category of privacy, such as "Receiving address management," is broken down into between one and three areas of consideration, including usability, quality, and user feedback.

## Criteria

<ol type="I">
	<li><strong>Protection from Blockchain Observers</strong>
		<ol type="A">
			<li><em>Receiving address management</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks required to deviate from the default receiving functionality and generate a new non-ECDH receiving address for an existing wallet. (4.049%)</li>
                            <li>Number of clicks required by user to generate a ECDH receiving address (BIP 63 or BIP 47), from the default window/authenticated home page. (2.024%)</li>
                        </ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Non-EDCH receiving addresses are hidden from the default view once they have been used? (3.543%)</li>
							<li>Preemptively indicates a loss of privacy when user elects to receive funds at a previously-used non-ECDH address, or prohibits this operation entirely? (1.771%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Change address management</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks required to deviate from the default change functionality and receive change at a newly generated address. (3.697%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Does the wallet produce P2SH change addresses when one or more of the spend outputs in a transaction is P2SH? (3.697%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Change addresses are hidden from the normal receiving workflow by default to discourage using them as receiving addresses? (1.972%)</li>
                            <li>Preemptively indicates a loss of privacy when user elects to reuse change addresses as receiving addresses, or prohibits this operation entirely? (0.986%)</li>
						</ol>
                    </li>
				</ol>
			</li>
            <li><em>Transaction construction</em>
                <ol type="1">
                    <li>Quality:
                        <ol type="a">
                            <li>When an outgoing transaction must merge inputs, and when mixing is not being used, is the transaction constructed in a way that plausibly resembles a mixing transaction? (1.893%)</li>
                            <li>Are inputs and outputs ordered in a deterministic manner based on criteria other than the status of outputs as spends or change (BIP 69)? (1.893%)</li>
                            <li>Does the wallet order inputs and outputs via a methodology common to multiple wallets? (0.473%)</li>
                            <li>When an input is selected which is part of a set of unspent outputs containing identical scripts (multiple deposits to a single address), is every output in the set added to the transaction? (0.946%)</li>
                            <li>Are all transactions created by the wallet compliant with BIP 62? (0.473%)</li>
                            <li>Can the wallet send to ECDH addresses (BIP 63 or BIP 47)? (0.946%)</li>
                        </ol>
                    </li>
                    <li>Feedback:
                        <ol type="a">
                            <li>Outside of a mixing transaction, preemptively indicates a loss of privacy when merging inputs from different addresses in the same transaction? (2.484%)</li>
                            <li>Warns user when sending to an address that the user has sent to before? (1.656%)</li>
                            <li>Warns user when sending to an address that has received deposits from any source? (1.656%)</li>
                        </ol>
                    </li>
                </ol>
            </li>
            <li><em>Mixing</em>
                <ol type="1">
                    <li>Usability:
                        <ol type="a">
                            <li>Number of clicks required by user for inputs/outputs to be mixed with one or more other users (2.958%)</li>
                        </ol>
                    </li>
                    <li>Quality:
                        <ol type="a">
                            <li>Average number of other users whose funds are mixed with yours when sending through a mixing process (1.479%)</li>
                            <li>Are mixing transactions constructed in a manner that makes them indistinguishable from non-mixing transactions? (1.479%)</li>
                        </ol>
                    </li>
                    <li>Feedback:
                        <ol type="a">
                            <li>Warns the user when a proposed mix is easy to reverse? (2.366%)</li>
                        </ol>
                    </li>
                </ol>
            </li>
            <li><em>Recurring transactions</em>
                <ol type="1">
                    <li>Usability:
                        <ol type="a">
                            <li>Number of clicks to opt out of creating recurring transactions, such as for donations to the wallet provider (0.518%)</li>
                        </ol>
                    </li>
                    <li>Quality:
                        <ol type="a">
                            <li>Does the wallet avoid creating recurring transactions with outputs of a known value or to a known address? (0.518%)</li>
                        </ol>
                    </li>
                </ol>
            </li>
		</ol>
	</li>
	<li><strong>Protection from Network Observers</strong>
		<ol type="A">
			<li><em>Balance information</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks required by user to to obtain balance information without leaking their machine identity over the network (2.677%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Is balance information obtained via one of the following methods? (2.008%)
                                <ul>
                                    <li>Without making queries to other network participants</li>
                                    <li>By making queries to other network participants that do not include multiple addresses in a specific connection context</li>
                                    <li>Via a method that matches a fraction of the blockchain beyond the addresses belonging to the wallet?</li>
                                </ul>
                            </li>
							<li>If balance information is obtained via querying more than one address in a given query, is a separate connection context used for each unique query? (0.669%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Client provides a visual indication if the balance information is not being obtained through an anonymizing network, including IP address information (2.142%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Outgoing transactions</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks required by user to route outgoing transactions through an anonymizing network (2.142%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Are outgoing transactions routed through a different entry point into the network than the source of balance information? (2.142%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Client provides a visual indication if outgoing transactions are not being routed through an anonymizing network, including IP address information (1.713%)</li>
						</ol>
					</li>
				</ol>
			</li>
            <li><em>Identity separation</em>
                <ol type="1">
                    <li>Quality:
                        <ol type="a">
                            <li>Avoids including addresses from multiple identity containers in the same balance query? (3.598%)</li>
                            <li>Avoids broadcasting outgoing transactions from different identity containers via the same connection context? (2.399%)</li>
                        </ol>
                    </li>
                </ol>
            </li>
            <li><em>Network behavior</em>
                <ol type="1">
                    <li>Quality:
                        <ol type="a">
                            <li>Does the backup process avoid leaking information about wallet addresses (e.g. each time a new change address is created on-demand, an email backup is triggered immediately)? (0.167%)</li>
                            <li>Wallet avoids leaking information about recipients via an external identity lookup? (0.666%)</li>
                            <li>Does the wallet avoid observably connecting to a known endpoint, such as a wallet provider’s domain? (0.333%)</li>
                            <li>User agent: (0.333%)
                                <ul>
                                    <li>Does the wallet connect to the network using an unremarkable user agent, OR</li>
                                    <li>Does the wallet connect to the network using a random user agent, from a set of unremarkable user agents, for each connection?</li>
                                </ul>
                            </li>
                        </ol>
                    </li>
                </ol>
            </li>
            <li><em>Operating system</em>
                <ol type="1">
                    <li>Usability:
                        <ol type="a">
                            <li>Compatible with latest version of Tails? (0.750%)
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
	<li><strong>Protection from Transaction Participants</strong>
		<ol type="A">
			<li><em>Identity management</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks to create a new identity container from the home screen of an existing identity container (1.165%)</li>
                            <li>Number of clicks to assign an imported private key into an identity container (0.388%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Avoids creating transactions which contain inputs from different identity containers, except optionally if the user has intentionally overridden this behavior? (1.553%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Visually indicates when inputs from different identity containers are merged before the transaction is broadcast, or prohibits this operation entirely? (1.242%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Mixing</em>
				<ol type="1">
					<li>Quality:
						<ol type="a">
							<li>Mixing is secure against correlation attacks by the facilitator (4.348%)</li>
                            <li>Mixing is secure against theft of funds (4.348%)</li>
						</ol>
					</li>
				</ol>
			</li>
		</ol>
	</li>
	<li><strong>Protection from Physical Adversaries</strong>
		<ol type="A">
			<li><em>GUI design</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks to configure the GUI to resemble a non-wallet application (0.543%)</li>
						</ol>
					</li>
                    <li>Quality:
                        <ol type="a">
                            <li>Does the wallet display addresses or transaction hashes in any form prior to the user explicitly requesting to see them? (0.543%)</li>
                        </ol>
                    </li>
				</ol>
			</li>
			<li><em>Data protection</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks to set an encryption password/PIN for wallet public keys (apart from that needed to encrypt private keys) (0.408%)</li>
                            <li>Number of clicks to set an encryption password/PIN for non-keypair wallet metadata (apart from that needed to encrypt private keys) (0.408%)</li>
                            <li>Number of clicks needed to permanently and completely erase the wallet from a device (0.408%)</li>
                            <li>Number of clicks needed to permanently and completely remove the wallet application from a device (0.408%)</li>
						</ol>
					</li>
                    <li>Quality:
                        <ol type="a">
                            <li>Can the wallet data be remotely deleted by the user in the event the device containing the wallet is lost or stolen? (0.326%)</li>
                            <li>Is the wallet application difficult to detect as being installed unless the user performs a series of actions unlikely to be duplicated by an unauthorized user? (0.326%)</li>
                            <li>Does the wallet application removal process eliminate all evidence that a wallet was previously installed? (0.326%)</li>
                            <li>Does the wallet deletion process eliminate all evidence that a wallet was previously installed? (0.326%)</li>
                            <li>Is persistent wallet metadata stored in a form not identifiable as belonging to a Bitcoin wallet? (0.326%)</li>
                        </ol>
                    </li>
				</ol>
			</li>
		</ol>
	</li>
	<li><strong>Protection from Wallet Providers</strong>
		<ol type="A">
			<li><em>Backups</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks to create the first wallet backup (0.376%)</li>
                            <li>Number of clicks needed to update an existing backup due to the creation of a new receiving or change address (0.753%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Backups can occur offline, or are encrypted client-side with data that only the user controls e.g. password? (1.129%)</li>
						</ol>
					</li>
					<li>Feedback:
						<ol type="a">
							<li>Indicates a reduction in wallet safety when backups are stale, or uses eternal backups? (0.903%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Personally identifying information</em>
				<ol type="1">
					<li>Quality:
						<ol type="a">
							<li>Does the wallet function without requiring the user to supply personally identifying information? (6.324%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Telemetry</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Number of clicks needed to disable sending telemetry data to the wallet provider (usage statistics, automatic crash reporting, etc) (0.949%)</li>
							<li>Number of clicks needed to ensure telemetry data is sent to the wallet provider in a manner that does not reveal the IP address of the user? (0.632%)</li>
						</ol>
					</li>
					<li>Quality:
						<ol type="a">
							<li>Does the wallet avoid transmitting telemetry data to the provider before the user has a chance to review the information being sent? (1.581%)</li>
						</ol>
					</li>
				</ol>
			</li>
			<li><em>Source code</em>
				<ol type="1">
					<li>Usability:
						<ol type="a">
							<li>Does the wallet provider supply simple instructions for building a usable binary from the source code? (2.372%)</li>
						</ol>
					</li>
                    <li>Quality:
                        <ol type="a">
                            <li>Is non-obfuscated source code for the wallet application available for immediate inspection? (1.186%)</li>
                            <li>Can a user produce a compiled version of the application from the public source code that exactly matches the version distributed by the wallet provider? (1.186%)</li>
                        </ol>
                    </li>
				</ol>
			</li>
		</ol>
	</li>
</ol>
