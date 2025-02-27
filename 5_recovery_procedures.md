---
layout: default
title: 5. Recovery Procedures
nav_order: 5
summary: Guidelines for safely recovering access to the multisignature wallet in various scenarios.
image: /assets/recovery.png
---

IMPORTANT: This protocol is under development and not yet ready for use.
{: .label .label-red }

Recovery Procedures
==================

![Recovery Procedures](/assets/recovery.png)

This chapter outlines the procedures for recovering from various access issues that may affect your Cerberus multisignature wallet. The 2-of-3 multisignature arrangement provides built-in redundancy, allowing the system to remain operational even if one key is compromised or unavailable.

## Overview of Recovery Scenarios

The Cerberus Protocol is designed to accommodate recovery from the following scenarios:

1. **Hardware wallet failure or loss**
2. **PIN forgotten**
3. **Seed phrase loss or compromise**
4. **Signatory unavailability (temporary or permanent)**

Each scenario has a specific recovery procedure that maintains the security of the multisignature arrangement while restoring full functionality.

## 1. Hardware Wallet Recovery

* [ ] **1.1. Identify hardware wallet issues**

Common hardware wallet issues include:
* Device not powering on
* Device not recognized by computer
* Physical damage to the device
* Device stolen or misplaced

* [ ] **1.2. Recovery procedure**

The affected signatory should:

* Purchase a new Trezor One hardware wallet
* Retrieve their seed phrase from their secure deposit box
* Set up the new device using the existing seed phrase
* Verify access to the multisig wallet using Electrum
* Test signing a small transaction with another signatory
* Return the seed phrase to secure storage
* Document the recovery in the Cerberus activity log

| WARNING |
| - |
| During this process, the seed phrase will temporarily be exposed. Perform this procedure in a secure location with no surveillance cameras and no unauthorized personnel. |

***

## 2. PIN Recovery

* [ ] **2.1. Identify PIN issues**

If a signatory has forgotten their PIN but still has their hardware wallet and access to their seed phrase, follow this procedure.

* [ ] **2.2. Recovery procedure**

The affected signatory should:

* Retrieve their seed phrase from their secure deposit box
* Intentionally enter the wrong PIN three times on the hardware wallet to reset it
* Follow the on-screen reset procedure
* Restore the wallet using the seed phrase
* Create a new PIN
* Document the new PIN on the same index card as the seed phrase
* Verify access to the multisig wallet using Electrum
* Return the seed phrase to secure storage
* Document the recovery in the Cerberus activity log

***

## 3. Seed Phrase Recovery

* [ ] **3.1. Identify seed phrase issues**

In the event that a signatory's seed phrase is:
* Lost or destroyed
* Potentially compromised
* Tamper-evident bag shows signs of tampering

A full key rotation for that signatory is required.

* [ ] **3.2. Recovery procedure**

The affected signatory should:

* Maintain possession of their existing hardware wallet if available
* Schedule a supervised recovery session with at least one other signatory
* During the session:
  * Create a new wallet on the hardware device (or on a new device if the original is unavailable)
  * Document the new seed phrase and PIN on an index card
  * Place in a new tamper-evident bag
  * Transfer the new seed phrase to a safe deposit box
* Once the new key is secure, proceed to key rotation (Step 3.3)

* [ ] **3.3. Key rotation procedure**

To replace a compromised key in the multisig arrangement:

* Create a new multisig wallet using:
  * The affected signatory's new public key
  * The unaffected signatories' existing public keys
  * The same 2-of-3 configuration
* Transfer all funds from the old multisig wallet to the new multisig wallet
  * This requires signatures from any two of the three signatories
  * At least one must be from an unaffected signatory with a trusted key
* Verify the funds have been received in the new multisig wallet
* Document the new wallet address and update all records
* Decommission the old multisig wallet

***

## 4. Signatory Unavailability Recovery

* [ ] **4.1. Temporary unavailability**

If a signatory is temporarily unavailable (vacation, illness, etc.):

* Use the two available signatories to sign transactions
* Document the use of alternate signatories in the transaction records
* No special recovery procedure is needed

* [ ] **4.2. Permanent unavailability**

If a signatory becomes permanently unavailable (employment termination, incapacitation, etc.):

* The organization must designate a new signatory
* The new signatory must complete all preparation steps
* Schedule a key rotation ceremony with the remaining original signatories
* Create a new hardware wallet and seed phrase for the new signatory
* Create a new multisig wallet with:
  * The new signatory's public key
  * The remaining original signatories' public keys
  * The same 2-of-3 configuration
* Transfer all funds from the old multisig wallet to the new multisig wallet
* Update all documentation with the new signatory information

| WARNING |
| - |
| When replacing a signatory due to termination of employment or other potentially adversarial situations, the key rotation should be performed immediately before the individual is notified of their termination. |

***

## 5. Full System Recovery

In the catastrophic event that multiple recovery scenarios occur simultaneously, a full system recovery may be necessary.

* [ ] **5.1. Assessing the situation**

Determine which components of the system remain intact:
* Which signatories still have access to their keys?
* Which seed phrases remain secure?
* Are any hardware wallets still operational?

* [ ] **5.2. Recovery requirements**

For full system recovery:
* At least 2 of the 3 seed phrases must still be accessible
* If only 1 seed phrase remains accessible, emergency procedures must be initiated

* [ ] **5.3. Recovery procedure**

* Assemble all available signatories
* For each compromised component:
  * Follow the appropriate recovery procedure above
  * Restore hardware wallets where possible
  * Replace signatories if necessary
* Once at least two keys are operational:
  * Create a new multisig wallet
  * Transfer funds from the old wallet
* Rebuild the system to full 2-of-3 redundancy
* Document all changes

***

## 6. Recovery Documentation

* [ ] **6.1. Recovery log**

After any recovery procedure:
* Document the issue that required recovery
* List all steps taken during recovery
* Record any changes to hardware, seed phrases, or personnel
* Have all participating signatories sign the log

* [ ] **6.2. System verification**

After any recovery procedure:
* Conduct a test transaction to verify system functionality
* Verify all signatories can access the wallet
* Confirm the correct balance is displayed
* Update any documentation that may have changed

***

**Note:** While these recovery procedures are designed to address a wide range of scenarios, unexpected situations may arise. If confronted with a scenario not covered in this document, prioritize the security of remaining keys and consult with a cryptocurrency security professional before proceeding.

***
