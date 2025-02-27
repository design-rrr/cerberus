---
layout: default
title: 3. Setup Ceremony
nav_order: 3
summary: Step-by-step execution of the multisignature wallet setup ceremony.
image: /assets/setup_ceremony.png
---

IMPORTANT: This protocol is under development and not yet ready for use.
{: .label .label-red }

Setup Ceremony
=============

![Setup Ceremony](/assets/setup_ceremony.png)

This chapter provides detailed instructions for the execution of the Cerberus Protocol's Setup Ceremony, during which the multisignature (multisig) wallet will be established. The ceremony should be conducted with all three signatories present in the same secure location as arranged by the Master of Ceremony (MC).

## Before Beginning

* Confirm that all steps in the [Preparation](/2_preparation.md) section have been completed
* Ensure all required equipment is present and unopened
* The MC should have all signatories' laptops verified for Electrum installation
* The venue should be secured with no unauthorized personnel present
* All mobile phones should be powered off completely (not just on silent)

## 1. Setup Preparations

* [ ] **1.1. Secure the room**

* Place a "Meeting in Progress - Do Not Disturb" sign on the outside of the door
* Lock the door from the inside if possible
* Draw any blinds or curtains to prevent outside visibility
* Verify no security cameras are active in the room

* [ ] **1.2. Set up the workspace**

* MC unpacks and distributes one privacy board to each signatory
* MC unpacks and places one Sharpie at each station
* MC unpacks the tamper-evident bags and places them in the center of the table
* Each signatory sets up their laptop and connects to power (not to internet)

* [ ] **1.3. Record attendees**

* MC records the full names of each signatory and their assigned numbers (1, 2, or 3)
* Each signatory verbally confirms their understanding of their assigned role

***

## 2. Hardware Wallet Setup

* [ ] **2.1. Distribute hardware wallets**

* MC unpacks each Trezor device, examines the security seal, and confirms it is intact
* MC documents each device's serial number and assigns it to a specific signatory
* Each signatory receives their designated hardware wallet

* [ ] **2.2. Connect and initialize devices**

Each signatory should:

* Connect the Trezor device to their laptop via USB
* When prompted, follow the on-screen instructions to set up a new device
* Select "Create new wallet"
* Write down the 24-word recovery seed phrase on the provided index card
  * Write clearly in capital letters with the Sharpie
  * Include the word number before each word (e.g., "1. APPLE")
* Verify the seed phrase when prompted by the device
* Set a strong device PIN (at least 6 digits, preferably 8+)
  * Do not use birth dates, addresses, or other easily guessable sequences
  * Document the PIN on the same index card as the seed phrase

| WARNING |
| - |
| Keep your seed phrase and PIN hidden under your privacy board at all times. Do not share this information with the other signatories. |

* [ ] **2.3. Verify individual wallets**

Each signatory should:

* Open Electrum on their laptop
* Select "Create new wallet" and name it "[YourName] Cerberus"
* Select "Standard wallet"
* Select "Use a hardware device"
* Select your Trezor device when it appears
* Follow the prompts to complete the setup
* Verify that a receive address is generated
* Record this address on a separate piece of paper for later verification

***

## 3. Creating the Multisignature Wallet

* [ ] **3.1. Obtain public keys**

Each signatory should:

* In Electrum, go to Wallet > Information
* Locate your "Master Public Key" (xpub)
* Copy this key to a piece of paper (or small index card)
* Label it with your signatory number (1, 2, or 3)
* Do not show this key to others yet

* [ ] **3.2. Create the multisig wallet (Signatory 1)**

Signatory 1 should:

* Close the current wallet in Electrum
* Select "Create new wallet" and name it "Cerberus Multisig"
* Select "Multi-signature wallet"
* Select "2 of 3 signatures"
* For the first cosigner, select "Use a hardware device" and select your own Trezor
* For the second cosigner, select "Enter cosigner key" and enter Signatory 2's public key
* For the third cosigner, select "Enter cosigner key" and enter Signatory 3's public key
* Complete the setup process

* [ ] **3.3. Verify the multisig setup**

* Signatory 1 should create a receive address in the new multisig wallet
* All signatories should record this address on paper
* Signatory 2 and 3 should now create their own multisig wallets following the same procedure as 3.2
* All three signatories should verify they have the exact same receive address
* If any discrepancy exists, the process must be restarted

***

## 4. Testing the Multisig Wallet

* [ ] **4.1. Send a test transaction**

* MC should prepare a safe way to send a minimal test amount (e.g., 0.001 BTC) to the multisig address
* After confirmation, verify that all signatories can see the incoming transaction
* Test a withdrawal by creating a transaction to return funds to the source address

* [ ] **4.2. Create and sign transaction (Signatory 1)**

* Signatory 1 creates a transaction sending the test amount minus fees back to source
* Signs the transaction with their hardware wallet
* Saves the partially signed transaction to a USB drive

* [ ] **4.3. Complete and broadcast transaction (Signatory 2)**

* Signatory 2 loads the partially signed transaction
* Signs the transaction with their hardware wallet
* Broadcasts the fully signed transaction to the network
* All signatories verify the transaction appears in the blockchain

***

## 5. Securing Recovery Information

* [ ] **5.1. Package seed phrases for secure storage**

Each signatory should:

* Review their seed phrase and PIN for legibility
* Place the index card with the seed phrase and PIN into a tamper-evident bag
* Seal the bag and write the following on the outside:
  * "CERBERUS PROTOCOL - SIGNATORY [NUMBER]"
  * Current date
  * Your signature across the seal

* [ ] **5.2. Verify wallet backup procedure**

MC leads a step-by-step review:

* Each signatory confirms they have:
  * A functional hardware wallet with PIN access
  * Their seed phrase securely sealed in a tamper-evident bag
  * A clear understanding of their role in the multisig arrangement

* [ ] **5.3. Conduct a recovery rehearsal (optional)**

If time permits:

* One signatory (volunteer) performs a simulated recovery using their seed phrase
* Verify the same public key is generated
* Verify access to the multisig wallet is maintained

***

## 6. Final Steps

* [ ] **6.1. Documentation**

* MC completes all ceremony documentation, including:
  * Signatory names and assigned numbers
  * Hardware wallet serial numbers
  * Multisig wallet address
  * Date and time of ceremony completion

* [ ] **6.2. Final security briefing**

MC reminds all signatories:

* Store hardware wallets in secure home storage
* Deposit seed phrases in safe deposit boxes within 48 hours
* Never store the seed phrase and hardware wallet together
* Report any suspected compromise immediately
* Review the Transaction Procedures section before initiating any real transactions

* [ ] **6.3. Clean up**

* Securely destroy any scratch paper or temporary notes
* Ensure all signatories take their designated equipment
* Leave the room in its original condition

***

**Congratulations! You have successfully completed the Cerberus Protocol Setup Ceremony. Your organization now has a secure multisignature wallet for cryptocurrency custody. Proceed to review the Transaction Procedures section before conducting any operations with the new wallet.**

***
