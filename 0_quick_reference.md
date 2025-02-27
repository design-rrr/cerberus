---
layout: default
title: 0. Overview & Quick Reference
nav_order: 0
summary: A concise reference for key roles, procedures, and checklists for the Cerberus Protocol.
image: /assets/quick_reference.png
---

IMPORTANT: This protocol is under development and not yet ready for use.
{: .label .label-red }

# Cerberus Protocol - Overview & Quick Reference

![Quick Reference Guide](/assets/quick_reference.png)

Welcome to the Cerberus Protocol – a comprehensive security framework designed for organizations seeking institutional-grade cryptocurrency custody. This document serves as both an overview of the entire protocol and a quick reference guide for key procedures.

The Cerberus Protocol employs a 2-of-3 multisignature arrangement where transactions require approval from at least two of three designated signatories, eliminating single points of failure while maintaining operational flexibility. The protocol provides detailed procedures for setup, transaction handling, recovery, and emergency situations.

Begin by reviewing this overview, then proceed through each section sequentially, starting with the [Introduction](/1_introduction.md) and following the implementation path through [Preparation](/2_preparation.md) and [Setup Ceremony](/3_setup_ceremony.md).

## Key Roles and Responsibilities

### Signatory Roles

| Role | Primary Responsibility | Backup Responsibility |
|------|------------------------|----------------------|
| **Signatory 1** | Initiates all transactions | Maintains hardware wallet & seed phrase |
| **Signatory 2** | Verifies & approves transactions | Maintains hardware wallet & seed phrase |
| **Signatory 3** | Backup for either role | Maintains hardware wallet & seed phrase |

### Master of Ceremony (MC)

* **Initial Setup**: Guides the Setup Ceremony process
* **Equipment**: Responsible for acquiring necessary hardware and supplies
* **Coordination**: Schedules meetings and ensures all signatories complete tasks
* **Rotation**: Role should rotate to different signatories during key rotation events

## Essential Equipment Checklist

| Item | Quantity | Purpose |
|------|----------|---------|
| Trezor One hardware wallets | 3 | Secure key storage |
| Laptops with USB ports | 3 | Running Electrum software |
| Tamper-evident bags | 3+ | Secure seed phrase storage |
| Privacy boards | 3 | Visual security during setup |
| Sharpie markers | 3+ | Documenting seed phrases |
| Index cards | 12+ | Recording seed phrases |
| Safe deposit boxes | 3 | Offsite seed phrase storage |
| Home safes/secure storage | 3 | Hardware wallet storage |

## Critical Security Procedures

### Transaction Flow

1. **Initiation** (Signatory 1)
   * Create transaction in Electrum
   * Verify address character-by-character
   * Sign with hardware wallet
   * Save partially signed transaction file

2. **Verification** (Signatory 2)
   * Load partially signed transaction file
   * Independently verify destination address
   * Confirm amount and fee structure
   * Sign with hardware wallet
   * Broadcast transaction

3. **Confirmation**
   * Document transaction ID
   * Monitor for blockchain confirmation
   * Update transaction records

### Recovery Situations

| Scenario | First Response | Documentation |
|----------|----------------|--------------|
| Hardware wallet failure | Use seed phrase to restore to new device | [Recovery Procedures - Section 1](/5_recovery_procedures.html#1-hardware-wallet-recovery) |
| Forgotten PIN | Reset device and restore from seed | [Recovery Procedures - Section 2](/5_recovery_procedures.html#2-pin-recovery) |
| Lost/compromised seed phrase | Immediate key rotation | [Recovery Procedures - Section 3](/5_recovery_procedures.html#3-seed-phrase-recovery) |
| Signatory unavailability | Use alternate signatory | [Recovery Procedures - Section 4](/5_recovery_procedures.html#4-signatory-unavailability-recovery) |
| Security breach | Activate Emergency Response Team | [Emergency Protocols - Part 1](/6_emergency_protocols_part1.md) |

## Important Contact Information

| Role | Contact Information | Backup Contact |
|------|---------------------|----------------|
| Signatory 1 | [Complete during setup] | [Complete during setup] |
| Signatory 2 | [Complete during setup] | [Complete during setup] |
| Signatory 3 | [Complete during setup] | [Complete during setup] |
| Legal Counsel | [Complete during setup] | [Complete during setup] |
| Security Officer | [Complete during setup] | [Complete during setup] |
| Executive Approval Authority | [Complete during setup] | [Complete during setup] |

## Regular Maintenance Schedule

| Task | Frequency | Responsible Party | Documentation |
|------|-----------|-------------------|--------------|
| Test wallet access | Monthly | All signatories | [Security Best Practices - Section 7.1](/security_best_practices.html#71-regular-testing) |
| Verify seed phrase storage | Quarterly | All signatories | [Security Best Practices - Section 7.2](/security_best_practices.html#72-backup-verification) |
| Emergency response drill | Bi-annually | MC | [Emergency Protocols - Part 2](/emergency_protocols_part2.html#6-emergency-drills-and-preparedness) |
| Full key rotation | Annually | All signatories | [Key Rotation Procedures](/8_key_rotation_procedures.md) |
| Security review | Annually | All signatories + Security Officer | [Security Best Practices - Section 8.2](/security_best_practices.html#82-security-assessments) |

## Complete Protocol Map

The full Cerberus Protocol consists of these key sections:

1. [Introduction](/1_introduction.md) - Overview and principles
   * What is the Cerberus Protocol
   * Core security principles
   * Required resources

2. [Preparation](/2_preparation.md) - Team assembly and equipment setup
   * Assembling the signatory team
   * Setting up secure storage
   * Acquiring hardware and software
   * Scheduling the setup ceremony

3. [Setup Ceremony](/3_setup_ceremony.md) - Creating the multisig wallet
   * Security preparations
   * Hardware wallet initialization
   * Multisignature wallet creation
   * Secure backup procedures

4. [Transaction Procedures](/4_transaction_procedures.md) - Day-to-day operations
   * Transaction initiation (Signatory 1)
   * Transaction verification (Signatory 2)
   * Emergency transaction procedures

5. [Recovery Procedures](/5_recovery_procedures.md) - Handling access issues
   * Hardware wallet recovery
   * PIN recovery
   * Seed phrase recovery
   * Signatory unavailability

6. [Emergency Protocols - Part 1](/6_emergency_protocols_part1.md) - Response team and breaches
   * Emergency Response Team activation
   * Security breach handling
   * Emergency fund transfers

7. [Emergency Protocols - Part 2](/7_emergency_protocols_part2.md) - Specific emergency scenarios
   * Personnel events
   * Extortion response
   * Force majeure situations
   * System failures

8. [Key Rotation Procedures](/8_key_rotation_procedures.md) - Periodic security updates
   * Scheduled key rotation
   * Emergency key rotation
   * Signatory replacement

9. [Security Best Practices](/9_security_best_practices.md) - Ongoing security measures
   * Operational security
   * Physical security
   * Digital security
   * Human factors

10. [Troubleshooting Guide - Part 1](/11_troubleshooting_guide_part1.md) - Hardware & software issues
    * Hardware wallet troubleshooting
    * Electrum software issues
    * Installation problems

11. [Troubleshooting Guide - Part 2](/12_troubleshooting_guide_part2.md) - Multisig & transaction issues
    * Multisignature specific issues
    * Transaction problems
    * Recovery and coordination issues

12. [Glossary](/10_glossary.md) - Terminology definitions
    * Technical terms explained
    * Acronyms and abbreviations

13. [Appendix](/13_appendix.md) - Background and rationales
    * Multisignature technology explained
    * Hardware security details
    * Risk analysis

## Emergency Response Flowchart

```
Incident Detected
       │
       ▼
Is it a security breach?
       │
  ┌────┴────┐
  │         │
 Yes        No
  │         │
  ▼         ▼
Activate    Is it a personnel issue?
   ERT      │
  │     ┌───┴───┐
  │     │       │
  │    Yes      No
  │     │       │
  │     ▼       ▼
  │  Follow    Is it extortion?
  │ Personnel  │
  │ Procedures ┌┴──┐
  │            │   │
  │           Yes  No
  │            │   │
  │            ▼   ▼
  │         Contact  Is it force majeure?
  │           Law    │
  │        Enforcement┌┴──┐
  │            │     │   │
  │            │    Yes  No
  │            │     │   │
  │            │     ▼   ▼
  │            │  Evacuation System
  │            │  Procedure  Failure
  │            │     │       │
  └────────────┘     │       │
        │            │       │
        ▼            │       │
  Document           │       │
   Incident          │       │
        │            │       │
        ▼────────────┘       │
  Review & Improve            │
        ◄───────────────────┘
```

***

**Note:** This quick reference guide does not replace thorough understanding of the complete Cerberus Protocol. All signatories should be familiar with the detailed procedures in each section.

***
