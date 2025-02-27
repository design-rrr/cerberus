---
layout: default
title: 9. Troubleshooting Guide - Hardware & Software
nav_order: 11
summary: Solutions for common hardware and software issues encountered with the Cerberus Protocol system.
image: /assets/troubleshooting1.png
---

IMPORTANT: This protocol is under development and not yet ready for use.
{: .label .label-red }

Troubleshooting Guide - Part 1
=============================

![Troubleshooting - Hardware & Software](/assets/troubleshooting1.png)

This chapter provides solutions to common hardware and software issues that may arise when using the Cerberus Protocol multisig wallet system. For multisignature specific and transaction issues, see [Troubleshooting Guide - Part 2](/12_troubleshooting_guide_part2.md).

## 1. Hardware Wallet Issues

### 1.1. Hardware wallet not recognized by computer

**Symptoms:**
* Hardware wallet does not appear in Electrum when connected
* No device notification on computer
* Device may or may not power on (LED indicator)

**Troubleshooting steps:**
1. Verify the hardware wallet is powered on
2. Try a different USB cable
3. Try a different USB port
4. Try connecting to a different computer
5. Check if device drivers are installed correctly

**Solution:**
* If the device powers on but isn't recognized: Update device drivers or reinstall Electrum
* If the device doesn't power on: Attempt charging for 15 minutes, then try again
* If still unresponsive: Prepare for device recovery using your seed phrase

**Prevention:**
* Regularly test device connectivity
* Keep device firmware updated
* Store in a dry, temperature-controlled environment

### 1.2. Forgotten PIN

**Symptoms:**
* Unable to access hardware wallet due to forgotten PIN
* Risk of device wipe after multiple incorrect attempts

**Troubleshooting steps:**
1. Do not guess repeatedly as most devices will wipe after 3 incorrect attempts
2. Check if PIN was documented in secure storage
3. If PIN cannot be recovered, prepare for device reset

**Solution:**
* Retrieve your seed phrase from secure storage
* Follow the Recovery Procedures to reset the device using the seed phrase
* Create a new PIN and document it securely

**Prevention:**
* Document PIN in secure storage
* Consider creating a PIN that follows a memorable pattern
* Test PIN entry regularly to maintain muscle memory

### 1.3. Device firmware issues

**Symptoms:**
* Device displays firmware error
* Request to update firmware when connected
* Unusual behavior or error messages

**Troubleshooting steps:**
1. Verify the legitimacy of any firmware update request
2. Check the manufacturer's website for current firmware version
3. Never update firmware without verifying authenticity

**Solution:**
* If a legitimate update is available, follow manufacturer instructions carefully
* Have your seed phrase accessible in case the update fails
* Verify wallet access after update completion

**Prevention:**
* Regularly check for official firmware updates
* Never update firmware immediately before critical transactions
* Always verify firmware signatures before installation

***

## 2. Electrum Software Issues

### 2.1. Electrum won't connect to servers

**Symptoms:**
* Status indicator shows disconnected
* Unable to view updated balance
* Cannot broadcast transactions

**Troubleshooting steps:**
1. Check internet connectivity
2. Verify Electrum server settings
3. Check if your firewall is blocking Electrum
4. Try restarting Electrum

**Solution:**
* Select "Auto-connect" in network settings
* Manually add trusted Electrum servers
* Temporarily disable firewall to test connectivity
* Update to the latest version of Electrum

**Prevention:**
* Maintain a list of reliable Electrum servers
* Consider running your own Electrum server for critical operations
* Keep Electrum updated to the latest version

### 2.2. Electrum displays incorrect balance

**Symptoms:**
* Balance shown does not match expected amount
* Transactions missing from history
* Unconfirmed transactions not appearing

**Troubleshooting steps:**
1. Verify wallet address on a blockchain explorer
2. Check if Electrum is fully synchronized
3. Verify you're on the correct blockchain (main chain vs. fork)

**Solution:**
* Try switching Electrum servers
* Restart Electrum with the "--reset" flag to rebuild history
* Verify transactions on multiple block explorers

**Prevention:**
* Keep transaction logs outside of Electrum
* Regularly verify balance across multiple tools
* Use trusted Electrum servers

### 2.3. Unable to create or sign transactions

**Symptoms:**
* Error messages when attempting to create transactions
* Hardware wallet not prompting to sign
* "Transaction not complete" errors

**Troubleshooting steps:**
1. Verify hardware wallet is properly connected
2. Check if the wallet is locked or requires PIN entry
3. Verify sufficient funds including transaction fees
4. Check if inputs are confirmed (not pending)

**Solution:**
* Reconnect hardware wallet and restart Electrum
* Ensure correct wallet is open in Electrum
* Try creating the transaction with a different fee rate
* Check for any pending transactions that may be blocking new ones

**Prevention:**
* Regularly test transaction creation process
* Keep inputs confirmed before attempting new transactions
* Maintain awareness of network fee conditions

***

## 3. Installation and Setup Issues

### 3.1. Electrum verification failures

**Symptoms:**
* Unable to verify GPG signature
* Signature verification shows "bad signature"
* Key import errors

**Troubleshooting steps:**
1. Verify you downloaded from the official Electrum website
2. Check your GPG installation is working correctly
3. Ensure you have the correct public key

**Solution:**
* Re-download both the Electrum installer and signature files
* Try an alternative verification method if available
* On Windows, try using Kleopatra instead of command line
* On Mac, ensure GPG tools are correctly installed

**Prevention:**
* Bookmark the official Electrum website
* Keep GPG or verification tools updated
* Maintain a copy of trusted public keys

### 3.2. Operating system compatibility issues

**Symptoms:**
* Installation fails or crashes
* Electrum won't start after installation
* Hardware wallet not detected by operating system

**Troubleshooting steps:**
1. Verify your operating system meets minimum requirements
2. Check for operating system updates
3. Look for known compatibility issues on Electrum website

**Solution:**
* Update your operating system to the latest version
* Install any required dependencies
* Try an alternative version of Electrum compatible with your OS
* Consider using a different computer for critical operations

**Prevention:**
* Keep operating systems updated
* Maintain a dedicated computer for cryptocurrency operations
* Test new Electrum versions in a non-critical environment first

### 3.3. Hardware wallet driver problems

**Symptoms:**
* Device connected but not recognized
* "Unknown device" errors
* Intermittent connection issues

**Troubleshooting steps:**
1. Check device manager for unknown devices
2. Verify if drivers are properly installed
3. Look for interference from other USB devices

**Solution:**
* Install the latest drivers from the manufacturer's website
* Try different USB ports, preferably directly on the motherboard
* Disable other USB devices that might cause interference
* On Windows, try running Electrum as administrator

**Prevention:**
* Keep hardware wallet firmware updated
* Install manufacturer tools for device management
* Avoid USB hubs for critical devices

***

## 4. Security and Recovery Tool Issues

### 4.1. Password manager integration problems

**Symptoms:**
* Unable to save or retrieve passwords
* Password manager not recognizing Electrum
* Autofill not working properly

**Troubleshooting steps:**
1. Verify password manager is up to date
2. Check if the password manager has browser integration enabled
3. Confirm permissions are correctly set

**Solution:**
* Update password manager to latest version
* Manually add entries if auto-detection fails
* Consider using the password manager's standalone application
* Use copy/paste for sensitive information rather than autofill

**Prevention:**
* Regularly update security software
* Test password manager functionality with non-critical accounts
* Maintain offline backups of critical passwords

### 4.2. Backup and recovery media failures

**Symptoms:**
* Unable to read written seed phrases
* Storage media degradation
* Physical damage to backup materials

**Troubleshooting steps:**
1. Inspect backup media for physical damage
2. Test readability under good lighting conditions
3. Check if water or heat damage has occurred

**Solution:**
* If seed phrase is partially readable, attempt recovery with partial seed tools
* If backup is compromised but wallet is still accessible, create new backups immediately
* Consider upgrading to metal backup solutions for long-term storage

**Prevention:**
* Use archival quality paper or metal backup solutions
* Store backups in waterproof, fireproof containers
* Create multiple backups stored in different physical locations
* Periodically verify the condition of backup materials

### 4.3. Security software interference

**Symptoms:**
* Antivirus quarantining Electrum files
* Firewall blocking network connectivity
* Security software preventing hardware wallet access

**Troubleshooting steps:**
1. Check security software logs for blocked actions
2. Verify if Electrum executable has been quarantined
3. Look for USB device blocking by security software

**Solution:**
* Add Electrum to your security software's exception list
* Temporarily disable security software to test if it's the cause
* Whitelist Electrum's network connections in your firewall
* Configure device access permissions in security software

**Prevention:**
* Properly configure security software before using Electrum
* Use application whitelisting rather than only blacklisting
* Keep security definitions updated
* Verify software authenticity before whitelisting

***

See [Troubleshooting Guide - Part 2](/12_troubleshooting_guide_part2.md) for solutions to multisignature and transaction-specific issues.

***
