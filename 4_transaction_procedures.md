---
layout: default
title: 4. Transaction Procedures
nav_order: 4
summary: Detailed procedures for safely initiating, verifying, and executing transactions with the Cerberus multisignature wallet.
image: /assets/transaction.png
---

IMPORTANT: This protocol is under development and not yet ready for use.
{: .label .label-red }

Transaction Procedures
=====================

![Transaction Procedures](/assets/transaction.png)

This chapter outlines the step-by-step procedures for conducting secure transactions using your Cerberus Protocol multisig wallet. These procedures maintain the segregation of duties established during the Setup Ceremony and ensure that no single signatory can unilaterally move funds.

## Transaction Roles and Responsibilities

As established during the Preparation phase, each signatory has a specific role:

| **Signatory 1** | Initiates all outbound transactions |
| **Signatory 2** | Verifies and approves all outbound transactions |
| **Signatory 3** | Backup signatory who can substitute for either Signatory 1 or 2 if they are unavailable |

Every transaction requires the participation of at least two signatories, maintaining the 2-of-3 multisignature security model.

## 1. Transaction Request Process

* [ ] **1.1. Business approval**

* All transactions must first receive appropriate business approval according to your organization's standard financial controls
* Documentation of this approval should be retained according to normal business procedures
* An official Transaction Request form should be completed with the following information:
  * Destination address
  * Amount to be sent
  * Purpose of transaction
  * Business approver name and signature
  * Date of request

* [ ] **1.2. Transaction scheduling**

* Signatory 1 schedules a transaction verification session with Signatory 2
* If either is unavailable, Signatory 3 should be scheduled as a replacement
* Both participating signatories should receive copies of the Transaction Request form in advance

***

## 2. Transaction Initiation (Signatory 1)

* [ ] **2.1. Preparation**

Signatory 1 should:

* Retrieve their hardware wallet from secure storage
* Ensure their laptop has the latest version of Electrum installed
* Connect the hardware wallet to their laptop
* Open Electrum and load the "Cerberus Multisig" wallet
* Enter PIN when prompted by the hardware wallet
* Verify the wallet balance before proceeding

* [ ] **2.2. Create transaction**

* Select "Send" tab in Electrum
* Enter the destination address from the Transaction Request form
* Double-check the address character by character against the form
* Enter the amount to be sent
* Set an appropriate fee based on current network conditions
* Create a reference note in the description field with the Transaction Request ID

* [ ] **2.3. First signature**

* Review all transaction details one final time
* Click "Send" to initiate the signing process
* Follow the prompts on the hardware wallet to verify and sign the transaction
* After signing, do NOT broadcast the transaction
* Select "Save" to export the partially signed transaction to a file
* Name the file with format: "Cerberus_TX_[DATE]_[AMOUNT]_partial.psbt"

***

## 3. Transaction Verification (Signatory 2)

* [ ] **3.1. Preparation**

Signatory 2 should:

* Retrieve their hardware wallet from secure storage
* Ensure their laptop has the latest version of Electrum installed
* Connect the hardware wallet to their laptop
* Open Electrum and load the "Cerberus Multisig" wallet
* Enter PIN when prompted by the hardware wallet
* Verify the wallet balance matches Signatory 1's reported balance

* [ ] **3.2. Independent address verification**

* Independently verify the destination address from the Transaction Request form
* If possible, verify through a secondary channel (e.g., signed email, official documentation)
* Document this verification on the Transaction Request form

* [ ] **3.3. Load and verify partial transaction**

* Select "Tools" > "Load transaction" > "From file"
* Load the partially signed transaction file provided by Signatory 1
* Review the details displayed in Electrum:
  * Destination address (match to Transaction Request form)
  * Amount (match to Transaction Request form)
  * Fee amount (reasonable for current network conditions)

* [ ] **3.4. Second signature and broadcast**

* Once verification is complete, click "Sign"
* Follow the prompts on the hardware wallet to verify and sign the transaction
* After signing, the transaction should show as "Fully Signed"
* Only after confirming full signing, click "Broadcast"
* Record the transaction ID on the Transaction Request form
* Both signatories should monitor for confirmation on the blockchain

***

## 4. Transaction Documentation

* [ ] **4.1. Record keeping**

* The completed Transaction Request form with blockchain transaction ID should be archived
* Both participating signatories should sign the form indicating their participation
* All transaction details should be recorded in the organization's financial records according to standard procedures

* [ ] **4.2. Secure storage**

* Both signatories return their hardware wallets to secure storage
* Any digital copies of the transaction file should be securely deleted
* The completed Transaction Request form should be filed according to company record retention policies

***

## 5. Emergency Transaction Procedures

In the event that standard procedures cannot be followed due to unavailability of personnel or time constraints, the following emergency procedures may be used.

* [ ] **5.1. Signatory unavailability**

If Signatory 1 is unavailable:
* Signatory 3 assumes the role of transaction initiator
* All other procedures remain the same

If Signatory 2 is unavailable:
* Signatory 3 assumes the role of transaction verifier
* All other procedures remain the same

If two signatories are unavailable:
* The transaction must be delayed until at least one becomes available
* Alternative emergency procedures may be initiated according to the Emergency Protocols section

* [ ] **5.2. Urgent transaction verification**

For time-sensitive transactions:
* The business approval process may be expedited according to your organization's emergency financial controls
* Transaction verification may occur remotely via secure channels
* All verification steps must still be completed, but may be conducted via secure video conference
* Full documentation must still be completed, but may be assembled after the transaction has been broadcast

***

## 6. Receiving Funds

* [ ] **6.1. Generate receive address**

Any signatory can:
* Open Electrum and load the "Cerberus Multisig" wallet
* Go to the "Receive" tab
* Generate a new address for each incoming transaction
* Provide this address to the sender along with any required payment instructions

* [ ] **6.2. Verify incoming transactions**

* Monitor wallet for incoming transactions
* Once confirmed, record transaction details according to normal financial procedures
* If the transaction is related to a specific business activity, ensure the appropriate team is notified

***

**Note:** The security of your organization's cryptocurrency holdings depends on strict adherence to these procedures. Do not take shortcuts or bypass steps, even in urgent situations. If a procedure cannot be followed as written, consult the Emergency Protocols section.

***
