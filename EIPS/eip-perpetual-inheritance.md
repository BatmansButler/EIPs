eip: <to be assigned>
title: <EIP title>
author: Seth Goldfarb (@goldfarbas), Ken Hodler (@bgok), Morgan Sherwood (@morganstar), Aaron Anderson (@andersonmmi)
discussions-to: <URL>
status: Draft
type: Standards Track
category ERC
created: 2020-06-22
requires (*optional): <EIP number(s)>
replaces (*optional): <EIP number(s)>

## Simple Summary
Perpetual Inheritance is a minimalistic protocol for digital wallet recovery. It increases the likelihood a digital wallet holder will be able to recover their assets in the event they lose access to their primary wallet by forcing them to prove their ability to access their primary wallet at regular intervals.

<!--"If you can't explain it simply, you don't understand it well enough." Provide a simplified and layman-accessible explanation of the EIP.-->

## Abstract
Helping people safely maintain custody of their digital assets remains one of the largest hurdles to the adoption of decentralized technologies. This protocol provides the basic functionality needed to help and encourage people to store their cryptoassets in a safe manner.

<!--A short (~200 word) description of the technical issue being addressed.-->

## Motivation
The value of lost cryptocurrency (sent to non-existent addresses, lost keys, and ) exceeds that of stolen cryptocurrency by approximately 4x

<!--The motivation is critical for EIPs that want to change the Ethereum protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the EIP solves. EIP submissions without sufficient motivation may be rejected outright.-->

## Specification
1. Create two Ethereum wallets: a primary and a backup.

2. Set a timer.

3. If time expires prior to check-in (signing a transaction), the contents of the primary wallet transfer to the backup wallet.

4. Allow a different backup wallet to be assigned to the primary wallet in case the user loses access to their backup but not their primary wallet.

5. When the backup wallet is accessed, a timer must be set in order to access the wallet. Once the timer is set, a new wallet is created and the backup becomes the user’s new primary wallet.

<!--The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current Ethereum platforms (go-ethereum, parity, cpp-ethereum, ethereumj, ethereumjs, and [others](https://github.com/ethereum/wiki/wiki/Clients)).-->
The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current Ethereum platforms (go-ethereum, parity, cpp-ethereum, ethereumj, ethereumjs, and [others](https://github.com/ethereum/wiki/wiki/Clients)).

## Rationale
![Perpetual Inheritance diagram](https://github.com/BatmansButler/Perpetual-Inheritance/Recovery1.png)

<!--The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.-->

## Backwards Compatibility
Perpetual inheritance can be applied to wallets created without it by incorporating a backup wallet and timer.

<!--All EIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The EIP must explain how the author proposes to deal with these incompatibilities. EIP submissions without a sufficient backwards compatibility treatise may be rejected outright.-->

## Test Cases
[](https://github.com/BatmansButler/Perpetual-Inheritance)

<!--Test cases for an implementation are mandatory for EIPs that are affecting consensus changes. Other EIPs can choose to include links to test cases if applicable.-->

## Implementation
Possible applications include:

* Preventing the loss of digital assets due to loss of control over a particular set of private keys.

* Facilitating digital asset transfer in the event of death or incapacitation.

<!--The implementations must be completed before any EIP is given status "Final", but it need not be completed before the EIP is accepted. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of "rough consensus and running code" is still useful when it comes to resolving many discussions of API details.-->

## Security Considerations
This protocol __does not__ provide a remedy for the theft of private keys or loss of access to both the primary and backup wallets.

<!--All EIPs must contain a section that discusses the security implications/considerations relevant to the proposed change. Include information that might be important for security discussions, surfaces risks and can be used throughout the life cycle of the proposal. E.g. include security-relevant design decisions, concerns, important discussions, implementation-specific guidance and pitfalls, an outline of threats and risks and how they are being addressed. EIP submissions missing the "Security Considerations" section will be rejected. An EIP cannot proceed to status "Final" without a Security Considerations discussion deemed sufficient by the reviewers.-->

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
