---
layout: default
title: 6. Emergency Protocols - Response Team & Breach Handling
nav_order: 6
summary: Emergency procedures for establishing a response team and handling security breaches.
image: /assets/emergency.png
---

IMPORTANT: This protocol is under development and not yet ready for use.
{: .label .label-red }

Emergency Protocols - Part 1
===========================

![Emergency Protocols](/assets/emergency.png)

This chapter outlines the procedures to follow in emergency situations that may threaten the security of your organization's cryptocurrency holdings. These protocols should only be activated in genuine emergency scenarios and require appropriate authorization from organization leadership.

## Emergency Situations Overview

The following situations qualify as emergencies requiring activation of these protocols:

1. **Security breaches** - Confirmed or strongly suspected compromise of keys, seed phrases, or hardware wallets
2. **Critical personnel events** - Unexpected loss of multiple signatories
3. **Extortion attempts** - Threats against signatories or the organization demanding cryptocurrency transfers
4. **Force majeure events** - Natural disasters, civil unrest, or other events threatening physical security
5. **System-wide failure** - Inability to access funds through normal procedures due to technical failures

For detailed responses to specific scenarios (items 2-5), see [Emergency Protocols - Part 2](/7_emergency_protocols_part2.md).

## 1. Emergency Response Team

* [ ] **1.1. Composition**

The Emergency Response Team (ERT) should consist of:
* At least one available signatory
* A member of the organization's executive leadership
* The organization's security officer or IT security representative
* Legal counsel (internal or external)

* [ ] **1.2. Activation**

The ERT can be activated by:
* Any signatory identifying a potential emergency
* Executive leadership of the organization
* Security officer identifying a credible threat

* [ ] **1.3. Communication**

Upon activation:
* Use the secure communication channel established during the Preparation phase
* If the primary channel is potentially compromised, use the backup channel
* Do not discuss specifics of the emergency over regular communication channels
* Establish an in-person meeting location if possible

***

## 2. Security Breach Response

* [ ] **2.1. Immediate containment**

If a security breach is suspected:

* The identifying signatory should immediately notify the other signatories
* Do not discuss details of the breach over potentially compromised channels
* All signatories should secure their hardware wallets and avoid connection to any computing device
* The ERT should be activated

* [ ] **2.2. Assessment**

The ERT should quickly assess:
* Which components may be compromised
* The severity and extent of the breach
* Whether funds are at immediate risk

* [ ] **2.3. Asset protection**

If funds are at immediate risk:
* Initiate an emergency fund transfer to a pre-designated "crisis wallet" address
* This requires any two available signatories
* Use offline transaction signing if possible
* Prioritize moving funds to safety over perfect procedure

* [ ] **2.4. Evidence preservation**

* Document all indicators of compromise
* Do not turn off or reset potentially compromised devices
* Preserve network logs and access records
* Take photographs of any physical evidence of tampering

***

## 3. Emergency Fund Transfer

* [ ] **3.1. Authorization**

An emergency fund transfer requires:
* Documented approval from executive leadership
* Participation of at least two signatories
* Documentation of the emergency circumstances

* [ ] **3.2. Destination wallet**

Funds should be transferred to:
* The organization's pre-established crisis wallet (recommended)
* A newly created multisig wallet (if crisis wallet is potentially compromised)
* In extreme circumstances, a trusted exchange's corporate account

* [ ] **3.3. Execution procedure**

To execute the emergency transfer:
1. Assemble available signatories in a secure location
2. Create the transaction using air-gapped devices if possible
3. Verify the destination address through multiple channels
4. Complete the 2-of-3 signing procedure
5. Broadcast the transaction
6. Monitor for confirmation
7. Document all actions taken

***

## 4. Post-Emergency Procedures

* [ ] **4.1. Documentation**

After resolving the emergency:
* Prepare a detailed incident report including:
  * Nature of the emergency
  * Actions taken
  * Timeline of events
  * Components affected
  * Funds moved and current status

* [ ] **4.2. System rebuild**

If the system was compromised:
* Replace all affected hardware
* Generate new seed phrases
* Create new multisig wallet
* Transfer funds from emergency destination
* Update documentation with new details

* [ ] **4.3. Process improvement**

* Conduct a post-incident review
* Identify process weaknesses or vulnerabilities
* Implement additional safeguards as needed
* Update emergency protocols based on lessons learned

***

**Important:** These emergency protocols should be reviewed and practiced regularly through simulated emergency drills. All signatories should be familiar with these procedures before an actual emergency occurs.

See [Emergency Protocols - Part 2](/7_emergency_protocols_part2.md) for specific scenario responses.

***
