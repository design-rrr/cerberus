---
layout: default
title: 9a. Troubleshooting Guide - Multisig & Transactions
nav_order: 12
summary: Solutions for multisignature-specific and transaction issues encountered with the Cerberus Protocol system.
image: /assets/troubleshooting2.png
---

IMPORTANT: This protocol is under development and not yet ready for use.
{: .label .label-red }

Troubleshooting Guide - Part 2
=============================

![Troubleshooting - Multisig & Transactions](/assets/troubleshooting2.png)

This chapter provides solutions to multisignature-specific and transaction issues that may arise when using the Cerberus Protocol system. For hardware and software issues, see [Troubleshooting Guide - Part 1](/11_troubleshooting_guide_part1.md).

## 1. Multisignature Specific Issues

### 1.1. Co-signers see different transaction details

**Symptoms:**
* Signatories report different transaction amounts or destinations
* Unable to complete signing process
* Transaction ID differences

**Troubleshooting steps:**
1. Compare transaction details character by character
2. Verify all signatories are using the same wallet file
3. Check if all are on the same Electrum version

**Solution:**
* Recreate the transaction from scratch
* Ensure all signatories have the identical multisig wallet setup
* Share the transaction file via a secure, verified channel

**Prevention:**
* Use a standardized procedure for transaction creation
* Verify transaction details through multiple channels
* Maintain identical Electrum versions across all signatories

### 1.2. Partially signed transaction files corrupted

**Symptoms:**
* Error when attempting to load transaction file
* "Invalid partial transaction" messages
* File appears empty or corrupted

**Troubleshooting steps:**
1. Verify the file was transferred completely
2. Check file extension and format
3. Try an alternative transfer method

**Solution:**
* Have the first signatory create and sign a new transaction
* Use encrypted channels for file transfer
* Consider using QR codes for small transactions instead of files

**Prevention:**
* Use file checksums to verify successful transfers
* Have backup methods for transaction file sharing
* Test file transfer process regularly

### 1.3. Unable to locate multisig wallet

**Symptoms:**
* Multisig wallet not appearing in Electrum
* "File not found" errors when trying to load wallet
* Different wallet appearing than expected

**Troubleshooting steps:**
1. Check the wallet file location in Electrum settings
2. Verify the file exists in the expected directory
3. Search for .wallet files on the computer

**Solution:**
* Use "File" > "Open" in Electrum to browse for the wallet file
* Recreate the multisig wallet using the original public keys
* Restore from backups if available

**Prevention:**
* Maintain backups of the multisig wallet file
* Document the exact storage location
* Regularly verify wallet accessibility

***

## 2. Transaction Issues

### 2.1. Transaction stuck with low fees

**Symptoms:**
* Transaction remains unconfirmed for extended periods
* No option to cancel transaction
* Funds appear locked

**Troubleshooting steps:**
1. Check current network fee conditions
2. Verify transaction status on multiple block explorers
3. Determine if the transaction is replaceable (RBF enabled)

**Solution:**
* If RBF is enabled, create a replacement transaction with higher fees
* Wait for the network to clear lower fee transactions
* For critical situations, consider fee bumping services

**Prevention:**
* Always enable Replace-By-Fee when creating transactions
* Check network congestion before sending important transactions
* Maintain a small reserve for potential fee bumping

### 2.2. Receiving address not showing funds

**Symptoms:**
* Funds sent to multisig address not appearing in wallet
* Explorer shows funds arrived but wallet shows zero balance
* Address may appear unfamiliar

**Troubleshooting steps:**
1. Verify the exact receiving address on a blockchain explorer
2. Confirm the transaction has sufficient confirmations
3. Verify all signatories have the identical multisig setup

**Solution:**
* Try refreshing the wallet (Tools > Network > Refresh)
* Verify the wallet derivation path matches the receiving address
* Recreate the multisig wallet if necessary using original public keys

**Prevention:**
* Verify receiving addresses across all signatory wallets before use
* Document all addresses used for significant transactions
* Test receiving with small amounts before large transfers

### 2.3. Transaction broadcast failures

**Symptoms:**
* "Network error" when broadcasting transaction
* Transaction disappears after attempted broadcast
* No transaction ID generated

**Troubleshooting steps:**
1. Check internet connectivity
2. Verify Electrum is connected to servers
3. Check if transaction size is unusually large

**Solution:**
* Try broadcasting through an alternative Electrum server
* Save the signed transaction file and try broadcasting later
* Consider using a blockchain explorer's "push transaction" feature

**Prevention:**
* Test network connectivity before initiating important transactions
* Have backup broadcasting methods prepared
* Avoid creating extremely large transactions with many inputs

***

## 3. Coordination and Human Issues

### 3.1. Signatory availability problems

**Symptoms:**
* Unable to reach required signatories
* Delayed response from signatories
* Scheduling conflicts for transaction signing

**Troubleshooting steps:**
1. Attempt contact through alternative channels
2. Check if backup signatory (Signatory 3) is available
3. Determine urgency of the transaction

**Solution:**
* For non-urgent transactions, reschedule when primary signatories are available
* For urgent transactions, activate Signatory 3 as per the protocol
* For emergencies, follow Emergency Protocols

**Prevention:**
* Maintain updated contact information for all signatories
* Establish clear response time expectations
* Have pre-scheduled transaction windows for predictable transactions

### 3.2. Process confusion or disagreement

**Symptoms:**
* Signatories following different procedures
* Disagreement about correct protocol steps
* Inconsistent application of security measures

**Troubleshooting steps:**
1. Reference the written Cerberus Protocol documentation
2. Identify the specific point of confusion or disagreement
3. Consult with all signatories

**Solution:**
* Always defer to the written protocol in cases of disagreement
* Hold a clarification meeting with all signatories
* Document any process clarifications for future reference

**Prevention:**
* Conduct regular protocol review sessions
* Maintain a single authoritative version of the protocol
* Document common points of confusion and their resolution

### 3.3. Training and knowledge gaps

**Symptoms:**
* Signatory unsure how to perform required actions
* Frequent procedural questions
* Errors in basic wallet operations

**Troubleshooting steps:**
1. Identify specific knowledge gaps
2. Determine if the issue is isolated to one signatory or systemic
3. Assess impact on operational security

**Solution:**
* Provide targeted training for identified knowledge gaps
* Create simplified checklists for common procedures
* Pair less experienced signatories with more experienced ones

**Prevention:**
* Conduct regular training and refresher sessions
* Test operational knowledge through simulations
* Maintain detailed documentation with examples

***

## 4. Recovery and Restoration Issues

### 4.1. Wallet recovery from backup issues

**Symptoms:**
* Unable to reconstruct wallet from public keys
* Different wallet address generated after recovery
* Missing transaction history

**Troubleshooting steps:**
1. Verify the exact public keys being used
2. Check that the multisig configuration is identical (m-of-n)
3. Ensure the correct derivation path is used

**Solution:**
* Carefully record all original public keys during setup
* Recreate the wallet with exact same parameters and key order
* Use wallet file backups rather than recreating when possible

**Prevention:**
* Store complete wallet creation details, not just seed phrases
* Back up wallet files in multiple secure locations
* Test recovery procedures periodically

### 4.2. Key rotation complications

**Symptoms:**
* New wallet doesn't match expected configuration
* Funds not visible after key rotation
* Error during fund transfer to new wallet

**Troubleshooting steps:**
1. Verify that all new keys were properly generated
2. Confirm the multisig wallet was correctly created with new keys
3. Check that the fund transfer transaction was properly signed and broadcast

**Solution:**
* If the new wallet is incorrect, recreate it with careful verification
* If funds transfer failed, verify transaction details and retry
* Document each step of the key rotation process

**Prevention:**
* Follow key rotation procedures exactly
* Verify each step before proceeding to the next
* Maintain access to old wallet until new wallet is fully verified

### 4.3. Emergency access issues

**Symptoms:**
* Unable to execute emergency procedures
* Critical documentation missing
* Confusion about emergency protocols

**Troubleshooting steps:**
1. Identify which emergency procedure is applicable
2. Verify availability of required signatories
3. Locate emergency documentation

**Solution:**
* Contact all available signatories immediately
* For critical situations, prioritize fund security over perfect procedure
* Document all emergency actions taken for later review

**Prevention:**
* Conduct regular emergency drills
* Keep emergency procedure documentation in multiple secure locations
* Ensure all signatories understand their emergency responsibilities

***

## 5. External Service Issues

### 5.1. Blockchain congestion and fee spikes

**Symptoms:**
* Extremely high fee estimates in Electrum
* Transactions remaining unconfirmed for long periods
* Unable to make time-sensitive transactions

**Troubleshooting steps:**
1. Check current mempool status on blockchain explorers
2. Verify fee requirements across multiple sources
3. Assess urgency of the transaction

**Solution:**
* For non-urgent transfers, delay until network congestion subsides
* For urgent transfers, use RBF with appropriate priority fees
* Consider using "Child Pays For Parent" for stuck transactions

**Prevention:**
* Monitor network conditions before initiating transactions
* Maintain awareness of events that might cause congestion
* Keep a reserve for emergency high-fee transactions

### 5.2. Exchange deposit/withdrawal issues

**Symptoms:**
* Exchange not recognizing multisig format
* Verification requests for wallet ownership
* Delayed processing of transfers

**Troubleshooting steps:**
1. Check the exchange's policies regarding multisig wallets
2. Verify address format compatibility
3. Document all transaction details and communications

**Solution:**
* Contact exchange support with detailed information
* Provide requested verification within security protocols
* Consider using a single-sig intermediate wallet if necessary

**Prevention:**
* Research exchange policies before initiating transfers
* Test small amounts first
* Maintain relationships with multiple exchanges

### 5.3. Compatibility with updated protocols

**Symptoms:**
* Warnings about address format incompatibility
* New transaction types not supported
* Upgrade messages in software

**Troubleshooting steps:**
1. Research the protocol changes and their impact
2. Check compatibility of current hardware and software
3. Determine if updates are critical for security

**Solution:**
* Keep software updated to support newer protocol features
* Consider hardware upgrades when necessary for security
* Follow a controlled update process with thorough testing

**Prevention:**
* Stay informed about upcoming protocol changes
* Test new features in controlled environments
* Maintain compatibility with both legacy and newer systems

***

**Note:** If you encounter an issue not covered in this guide, contact your organization's designated cryptocurrency security expert before attempting untested solutions. Document any new issues and their resolutions to improve this guide over time.

See [Troubleshooting Guide - Part 1](/11_troubleshooting_guide_part1.md) for hardware and software specific issues.

***
