# Template

 - [ ] Build Arch

 - [ ] Build MacOS Sonoma

 - [ ] Build Ubuntu 22.04

 - [ ] Build Win 10

## Setup 1 => from zero (signet, p2wsh, fulcrum) arch

- [ ] Jade (A)
  - <mnemonic>
  - <Xpub>

- [ ] ColdCard(B)
  - 
  - 

- [ ] Specter (C)
  - 
  - 

- [ ] Nano S+ (D)
  - 
  - 

  
- [x] Generate new wallet or(thresh(4,A,B,C,D,E), and(thresh(2,A,B,C,D,E,F), timelock))
  - <descriptor>

- [ ] Register on Jade (Installer)
- [ ] Register on Coldcard (Installer)
- [ ] Register on Specter (Installer)
- [ ] Register on Ledger (Installer)

- [ ] remove the wallet
- [ ] change timelock to 1000 & remove checksum
- [ ] import the modified wallet <descriptor>

- [ ] Register on Jade (Installer)
- [ ] Register on Coldcard (Installer)
- [ ] Register on Specter (Installer)
- [ ] Register on Ledger (Installer)

- [ ] Verify recption address w/ specter (QR Code)
- [ ] Verify recption address w/ ColdCard => Display bug
- [ ] Verify recption address w/ Ledger
- [ ] Verify recption address w/ Jade

- [ ] Receive regtest wallet


- [ ] Register on Jade (Settings)
- [ ] Register on Coldcard (Settings)
- [ ] Register on Specter (Settings)
- [ ] Register on Ledger (Settings)

- [ ] rotate coin
  - [ ] Check signing flow w/ Coldcard
    - [ ] appear as slf transfert
  - [ ] Check signing flow w/ Jade
    - [ ] appear as slf transfert
  - [ ] Check signing flow w/ Ledger
    - [ ] appear as slf transfert
  - [ ] Check signing flow w/ Specter
    - [ ] appear as slf transfert

- [ ] recovery sweep at 1 sats/vb
  - [ ] Check signing flow w/ Specter
  - [ ] Check signing flow w/ Coldcard
  - [ ] broadcast

- [ ] recovery sweep at 10 sats/vb
  - [ ] Check signing flow w/ Nano S+
  - [ ] Check signing flow w/ Jade
  - [ ] broadcast
    - [ ] warning about tx replaced
    - [ ] tx replaced in mempool & mined

## Setup 2 Participate mode (regtest + fulcrum + taproot)

### Machine 1 (macOS) handle Jade and Ledger using 'participate' mode

  - [ ] Ledger (A)
  - [ ] Share xpub to machine 2

### Machine 2 (Win10) handle C using 'create' mode

  - [ ] Coldcard (B)
  - [ ] Register B on machine 2

- [ ] Generate wallet or(A, and(B, timelock))
  -  

- [ ] Register descriptor B (from settings)
- [ ] Receive coins
- [ ] go to expiration - 1 block
- [ ] renew the coin

- [ ] go to expiration + 1 block
- [ ] prepare tx and send to machine 1 (PSBT)
- [ ] share descriptor w/ machine 1

### Back to machine 1
- [ ] Import descriptor
- [ ] Register descriptor A (from settings)

- [ ] craft recovery tx

- [ ] Broadcast

### Labels

- [ ] add label from Home > Last payments for a received payment
  - [ ] label appear in coins
  - [ ] label appear in transactions
  - [ ] close and reopen liana, label still there

- [ ] edit the label from coins
  - [ ] label appear in home -> last payments
  - [ ] label appear in transactions
  - [ ] close and reopen liana, label still there

- [ ] edit the label from transactions
  - [ ] label appear in home -> last payments
  - [ ] label appear in coins 
  - [ ] close and reopen liana, label still there

- [ ] add a label on an address
- [ ] receive a coin to this address
  - [ ] adress label appear in Home -> last payments
  - [ ] coins -> select the coins -> address label appear
  - [ ] transactions -> select transaction -> click payment -> address label appear
  - [ ] close and reopen liana, label still there

### PSBT
- [ ] create a spend -> go to sign process -> do NOT sign
- [ ] click save
- [ ] go to settings
- [ ] go to psbts
- [ ] the previous saved spend appear

- [ ] create a new spend that spend the same coin
- [ ] sign it
- [ ] go to home
- [ ] go to psbt
- [ ] the signed psbt is there
- [ ] click on it 
- [ ] broadcast it
- [ ] go to psbt
  - [ ] broadcasted psbt is labeled 'Unconfirmed'
  - [ ] wait 1 confirmation
  - [ ] psbt now labeled 'Spent'
  - [ ] previous psbt is labeled 'Deprecated'
  - [ ] click on this psbt and delete it

- [ ] create a recovery send
  - [ ] sign it
  - [ ] go to home
  - [ ] go to psbts
  - [ ] it appear w/ 'Recovery' badge

### Test coin selection

- [ ] MAX => should select both confirmed/unconfirmed coins
- [ ] unconfirmed coins are not auto selected
- [ ] unconfirmed coins can be manually selected

### RBF/CPFP

- [ ] RBF
  - [ ] send a coin a 1sat/vb
  - [ ] tx is unconfirmed
  - [ ] go to transactions -> click on unconfirmed tx -> bump fee
  - [ ] craft tx + sign + broadcast
  - [ ] warning appear at broadcast
  - [ ] go to PSBTS -> new tx is 'Unconfirmed', previous one 'Deprecated'
  - [ ] mine one block
  - [ ] the tx is now not 'Unconfirmed' but 'Spent'

- [ ] Cancel
  - [ ] send a coin to an external address at 1 sat/vb
  - [ ] tx is unconfirmed
  - [ ] go to transactions -> click on unconfirmed tx -> cancel
  - [ ] craft tx + sign + broadcast
  - [ ] warning appear at broadcast
  - [ ] go to PSBTs
    -[ ] new tx is unconfirmed
    - [ ] canceled tx is deprecated
    - [ ] cancceled tx is deprecated after replacement tx is mined

- [ ] CPFP
  - [ ] send 1 coin to Liana at 1 sat/vb
  - [ ] the payment is unconfirmed
  - [ ] use this coin for a send to self at 10 sat/vb
  - [ ] fees of CPFP tx should include fee for bump ancestor tx

### Reorg (bitcoind)

- [ ] reorg on unconfirmed coin
  - [ ] send a coin to the wallet
  - [ ] spend to self
  - [ ] wait for send to self unconfirmed coin appear in liana
  - [ ] invalidate 2 blocks
  - [ ] wait for liana block height to be updated
  - [ ] the unconfirmed coin should disapear

- [ ] reorg on confirmed coin
  - [ ] send a coin to the wallet
  - [ ] mine one block
  - [ ] coin appear confirmed
  - [ ] invalidate 2 blocks
  - [ ] coin should disapear

### Misc

- [ ] change key fingerprint alias
- [ ] address index increment
- [ ] fee rate at 0 should fail
- [ ] fee rate > 1000
- [ ] dust output
- [ ] adress validation in spend panel
- [ ] descriptor validation in import (installer)
  - [ ] wrong network fail
  - [ ] no checksum succeed
  - [ ] hardened multipath fail
  - [ ] no multipath fail
  - [ ] cannot import non liana descriptor

### Electrum
- [ ] electrs
- [ ] esplora
- [ ] electrumx
- [ ] fulcrum
- [ ] ssl (ssl://pythcoiner.dev:50002)

### WS Backend

- [ ] create custom wallet on desktop
- [ ] create a liana lite account + wallet & import in desktop
- [ ] join a wallet by invitation
- [ ] recovery from desktop

### DB upgrade

## Issues

### Successfully checked

## Comments

### Related w/ closed issues

### New opened issues/PRs

