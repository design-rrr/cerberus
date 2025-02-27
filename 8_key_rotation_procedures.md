---
layout: default
title: 7. Key Rotation Procedures
nav_order: 8
summary: Procedures for periodically updating the multisignature wallet configuration to maintain long-term security.
image: /assets/key_rotation.png
---

IMPORTANT: This protocol is under development and not yet ready for use.
{: .label .label-red }

Key Rotation Procedures
=====================

![Key Rotation](/assets/key_rotation.png)

This chapter outlines the procedures for periodically rotating keys in your Cerberus multisignature wallet. Regular key rotation is a critical security practice that limits the impact of undetected compromises and ensures the long-term integrity of your cryptocurrency holdings.

## Key Rotation Overview

Key rotation involves:
1. Creating new seed phrases and hardware wallet configurations
2. Establishing a new multisignature wallet
3. Transferring funds from the old wallet to the new wallet
4. Decommissioning the old wallet

This process should be performed:
* On a regular schedule (recommended annually)
* After any potential security compromise
* When replacing a signatory
* When upgrading hardware or software components

## 1. Preparation for Key Rotation

* [ ] **1.1. Scheduling**

* Schedule the key rotation ceremony at least two weeks in advance
* Ensure all three signatories can be present
* Book a secure room meeting all the requirements from the original Setup Ceremony
* The Master of Ceremony (MC) role should rotate to a different signatory with each key rotation (this promotes shared knowledge and prevents dependency on a single individual)

* [ ] **1.2. Equipment preparation**

The new MC should:
* Procure new hardware wallets (one for each signatory)
* Obtain new tamper-evident bags
* Verify all signatories have access to their safe deposit boxes
* Ensure all necessary software is up to date

* [ ] **1.3. Pre-rotation verification**

Prior to the ceremony:
* Verify full access to the current multisig wallet
* Confirm the current balance
* Prepare a list of any pending transactions
* Complete all pending transactions before proceeding

***

## 2. Key Rotation Ceremony

* [ ] **2.1. Opening the ceremony**

The MC should:
* Review the purpose and process of key rotation
* Distribute privacy boards and materials
* Confirm no recording devices are present
* Establish a clear timeline for the ceremony

* [ ] **2.2. Create new wallets**

Each signatory should:
* Unbox their new hardware wallet and verify tamper-evident seals
* Initialize the new device according to manufacturer instructions
* Generate and record a new 24-word seed phrase on an index card
* Set a new PIN (different from previous PIN)
* Keep the seed phrase and PIN hidden under their privacy board

* [ ] **2.3. Setup in Electrum**

Each signatory should:
* Connect their new hardware wallet to their laptop
* Create a new standard wallet in Electrum connected to the hardware device
* Name it "[YourName] Cerberus [YEAR]"
* Obtain their new extended public key (xpub) from wallet information
* Write this public key on a card labeled with their signatory number

* [ ] **2.4. Create new multisig wallet**

Starting with Signatory 1:
* Create a new multisig wallet in Electrum
* Configure it as 2-of-3
* Enter all three new public keys
* Verify the creation of a receive address
* Document this address

All signatories should:
* Repeat the multisig creation process with their own hardware wallets
* Verify they all generate the identical wallet address

***

## 3. Fund Transfer

* [ ] **3.1. Verification of new wallet**

Before transferring funds:
* All signatories should verify the same multisig address is displayed
* The MC should verify the configuration is correct (2-of-3)
* Conduct a small test transaction to the new wallet if time permits
* Verify receipt of the test transaction

* [ ] **3.2. Main fund transfer**

Using the old hardware wallets:
* Signatory 1 creates a transaction sending all funds minus the test amount to the new multisig address
* Include appropriate network fees
* Signatory 1 signs the transaction
* Signatory 2 reviews and signs the transaction
* Broadcast the transaction to the network
* Monitor for confirmation (this may take some time depending on network conditions)

* [ ] **3.3. Confirmation**

After the transaction is confirmed:
* Verify the full balance appears in the new multisig wallet
* All signatories should independently confirm the balance
* Document the transaction ID and final balance

***

## 4. Secure Storage

* [ ] **4.1. Seed phrase security**

Each signatory should:
* Place their new seed phrase and PIN in a tamper-evident bag
* Seal and sign across the seal
* Label with "CERBERUS PROTOCOL - SIGNATORY [NUMBER] - [DATE]"
* Commit to storing this in their safe deposit box within 48 hours

* [ ] **4.2. Hardware wallet security**

Each signatory should:
* Securely store their new hardware wallet
* Use their existing secure home storage location
* Keep the hardware wallet separate from the seed phrase at all times

***

## 5. Decommissioning Old Components

* [ ] **5.1. Secure erasure of old hardware wallets**

Each signatory should:
* Reset their old hardware wallet according to manufacturer instructions
* This typically involves entering incorrect PINs until a factory reset is triggered
* Verify the device has been fully reset

* [ ] **5.2. Handling old seed phrases**

Each signatory has two options:
* **Preferred:** Destroy the old seed phrase by shredding or burning
* **Alternative:** Mark it clearly as "DECOMMISSIONED - [DATE]" and store separately from active seed phrases

* [ ] **5.3. Software cleanup**

Each signatory should:
* Remove the old wallet from Electrum
* Clear any cache or temporary files
* Verify the old wallet no longer appears in their wallet list

***

## 6. Documentation and Verification

* [ ] **6.1. Update documentation**

The MC should prepare:
* A key rotation certificate documenting:
  * Date of rotation
  * Signatories present
  * New wallet address
  * Hardware wallet serial numbers
  * Transaction ID of the fund transfer
* Each signatory should sign this certificate

* [ ] **6.2. Verification process**

Within one week of the ceremony:
* Each signatory should verify they can still access the new wallet
* Conduct a small test transaction between signatories
* Document successful access and transaction ability

* [ ] **6.3. Secure the documentation**

* The key rotation certificate should be stored according to organization document policies
* Digital copies should be encrypted and access-restricted
* Physical copies should be stored in secure storage

***

## 7. Special Rotation Scenarios

* [ ] **7.1. Partial rotation (single signatory)**

When replacing only one signatory:
* Only the affected signatory creates a new seed phrase and hardware wallet
* The new multisig wallet uses:
  * The new signatory's public key
  * The unaffected signatories' existing public keys
* All other procedures remain the same

* [ ] **7.2. Emergency rotation**

In the event of a suspected compromise:
* Follow the Emergency Protocols first to secure funds
* Once funds are secured, conduct a full key rotation as soon as possible
* Consider generating keys in a more secure environment (e.g., air-gapped computer)

* [ ] **7.3. Upgrade-driven rotation**

When upgrading to new hardware or software:
* Follow the standard rotation procedure
* Ensure all new components are compatible
* Document the specific changes in technology

***

**Note:** Key rotation is a critical security practice. Never postpone scheduled rotations, and always maintain the same level of security during rotation as during the initial setup. While it may seem cumbersome, regular key rotation significantly reduces the risk of undetected compromises affecting your cryptocurrency holdings.

***
