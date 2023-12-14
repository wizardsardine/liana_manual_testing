# Template

- [ ] Install Win10
- [ ] Install Debian12
- [ ] Install Ubuntu 22.04/22.10/23.04/23.10
- [ ] Install Arch
- [ ] IBD testnet <platform>
- [ ] IBD Mainnet <platform>
- [ ] Build <platform> commit <commit> 

## Upgrade

- [ ] Upgrade from V2
- [ ] Upgrade from V3

## Setup 1 => from zero (Signet Managed by Liana)

- [ ] Generate 1 hot seed (A)
  - <xpub>
  - <mnemonics>
- [ ] Import seed #1 on <signer> (B)
  - <mnemonics>
  - <descriptor>
- [ ] Import seed #2 on <signer> (C)
  - <mnemonics>
  - <descriptor>
- [ ] Generate new wallet multi(3, A, B, C) | multi(2, A, B, C) & 10 blocs | multi(1, A, B, C) & 20 Blocs
- [ ] Register on B
- [ ] Register on C
- [ ] Let Liana handle bitcoind
- [ ] Receive from <type> faucet (<?> coin, <?> change)
- [ ] send back to <type> faucet (<?> coins, <?> change) primary path


## Simulate Lost machine 1 => restore wallet + recovery

- [ ] Import A on machine 3
- [ ] Import descriptor on machine 3
- [ ] Use signer B on machine 3
- [ ] Register B on machine 3
- [ ] Rescan
- [ ] Recovery with path2 (A + B) on <type> faucet

## 'Participate' Setup using standalone bitcoind

### Machine 1 handle A and B using 'participate' mode
  
  - [ ] Generate 1 hot seed (A)
    - <xpub>
    - <mnemonics>
  - [ ] Register B on machine 1
  - [ ] Share xpubs A & B to machine 2

### Machine 2 handle C using 'create' mode

- [ ] Import A & B xpubs
- [ ] Connect signer C
- [ ] Generate wallet
- [ ] Register descriptor on signer C
- [ ] receive coins from faucet wallet
- [ ] prepare tx and send to machine 1 (PSBT)
- [ ] share descriptor w/ machine 1

### Back to machine 1
- [ ] Import descriptor
- [ ] Register descriptor on signer B
- [ ] import and sign with A & B tx generated on machine 2 
- [ ] send back PSBT to machine 2

### Back to machine 2
- [ ] Import PSBT
- [ ] Sign w/ signer C
- [ ] Broadcast

## Notes


