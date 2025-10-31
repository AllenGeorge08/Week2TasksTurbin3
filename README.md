# EscrowAI

## Project Name  
**EscrowAI**

---

## Value Proposition

EscrowAI is a decentralized platform that verifies and rewards authentic AI training data. It uses blockchain-based escrows and oracles to ensure that contributors are fairly compensated for providing verified datasets, and that AI developers receive reliable, transparent, and traceable data.

---

## Product Market Fit

EscrowAI serves two growing needs:

1. **Data Contributors** who want fair rewards and ownership proof for their data contributions.  
2. **AI Developers and Companies** who require high-quality, verifiable datasets for model training to ensure reliability and compliance.

By combining blockchain transparency with oracle-based validation, EscrowAI bridges the trust gap between data providers and data consumers in the AI ecosystem.

---

## Target User Profiles

### Primary User Persona

**Name:** Allen  
**Role:** Independent Data Labeler  
**Goal:** To upload and verify data contributions securely, prove ownership, and earn tokens for providing high-quality datasets.  
**Pain Points:** Unfair compensation, no way to prove authorship, and lack of transparency about how data is used.  

### Secondary User Persona

**Name:** Rajesh Patel  
**Role:** AI Startup Founder  
**Goal:** To purchase verified and high-quality data for AI training without worrying about legal or ethical risks.  
**Frustrations:** Difficult to verify the authenticity of datasets, risk of using stolen or synthetic data, and lack of quality control.

---

## Acceptance Criteria

### Functionality
- Users can upload dataset metadata (e.g., hash or IPFS link) through the dApp interface.  
- Dataset hash is stored in a vault smart contract as proof of authorship.  
- Verification oracles assess data authenticity and quality.  
- Once verified, an escrow contract automatically releases $EAI tokens to the contributor.  
- AI developers can browse verified datasets and pay with $EAI tokens to access them.

---

### User Interaction
- Contributors connect their wallet to the platform.  
- Contributors can view the verification status of their submitted datasets.  
- Upon verification, contributors receive a transaction confirmation and reward summary.  
- Developers can view dataset governance and verification logs before purchasing.  
- If verification fails, the user is notified, and tokens remain locked in escrow.

---

### Security
- Vaults ensure only the dataset owner can claim ownership.  
- Escrow smart contracts release rewards only after successful oracle verification.  
- All transactions are immutable and recorded on-chain for transparency.

---

### Priority
High - for establishing user trust and ensuring transparent data validation.

---

## Technical Notes for Developers

- Use Solana smart contracts for vault and escrow functionality.  
- Integrate with external oracles for data validation.  
- Store dataset metadata using decentralized storage (e.g., IPFS or Arweave).  
- Implement a token contract ($EAI) for rewarding verified data contributions.  
- Include a reputation mechanism for contributors and verifiers.

---

## Dependencies

- Requires Solana devnet or mainnet availability.  
- Requires oracle integration for off-chain verification.  
- Requires a frontend for wallet connection and data submission.

---

## User Story ID: EAI-001

**Persona:** Allen, Data Contributor  

**User Story:**  
As a data contributor, when I upload a dataset and its metadata to EscrowAI, I want it to be verified through a transparent process and receive tokens when the data is confirmed to be valid, so that I am rewarded fairly and can prove my ownership.  

**Acceptance Criteria:**  
- User connects wallet and uploads dataset metadata (hash + description).  
- Vault smart contract stores ownership details.  
- Oracle verifies data authenticity and reports the result on-chain.  
- Upon approval, escrow smart contract releases $EAI tokens to the contributor’s wallet.  
- If verification fails, user receives a notification with the reason for rejection.  
- Ownership and verification details are publicly viewable on-chain.

---

## User Story ID: EAI-002

**Persona:** Rajesh Patel, AI Developer  

**User Story:**  
As an AI developer, when I browse available datasets, I want to see verified data with on-chain proof of authenticity, so that I can safely use it for model training without legal or ethical risks.  

**Acceptance Criteria:**  
- User connects wallet and accesses the dataset marketplace.  
- User can view verification status, contributor information, and dataset hash.  
- Payment in $EAI tokens is processed through the escrow contract.  
- Dataset access is granted after successful payment.  
- Provenance and verification details are available for compliance and audit.

![EscrowAI Architecture Diagram](./Untitled%20Diagram.drawio%20(1).png)