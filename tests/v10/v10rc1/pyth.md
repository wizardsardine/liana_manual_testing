test made on top of v9rc1

 - [x] Build Arch

## get binary

- [x] download from github liana-10.0rc1-x86_64-linux-gnu.tar.gz
- [x] check signature
- [x] check binary version w/ `liana-gui --version ` => 10.0.0-rc1
- [x] check version in launcher => 10.0.0-rc1
- [x] check version in installer title bar => 10.0.0-rc1
- [x] check version in gui title bar => 10.0.0-rc1

## Setup 1 => maxi wallet (local unmanaged bitcoind regtest) 

- [x] ColdCard(A)
  - c658b283

- [x] Nano S+ (B) 
  - d4ab66f1

- [x] BitBox02(C) (Safety net)
  - e2e975b7

- [x] Generate new wallet tr( A || B & 1 year || C & max )
  - wsh(or_i(and_v(v:pkh([e2e975b7/48'/1'/0'/2']tpubDFkztzafRmw9sd9V2jwgiv5eafAAZmfQX5huqBLzbfFcNUzkCCWN2kpYHkjhzWvwrQuckyxmruVka7DWtzNRPy4Bpgty4vr9Sx6U5QmhGrw/<0;1>/*),older(65535)),or_d(pk([c658b283/48'/1'/0'/2']tpubDFL5wzgPBYK5pZ2Kh1T8qrxnp43kjE5CXfguZHHBrZSWpkfASy5rVfj7prh11XdqkC1P3kRwUPBeX7AHN8XBNx8UwiprnFnEm5jyswiRD4p/<0;1>/*),and_v(v:pkh([d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<0;1>/*),older(100)))))#e8xsu3au

- [x] [backup file](./assets/liana-backup-2025-03-26T06-31-48.json)

- [x] close liana here
- [x] import the backup file

- [x] Register on Coldcard (Installer)
- [x] Register on Ledger (Installer)

- [x] Verify reception address w/ ColdCard
  - [x] display address
  - [x] display index
- [x] Verify reception address w/ Ledger
  - [!] display address
  - [!] display index

- [x] Label address
- [x] Receive regtest wallet
- [x] Label coin
- [x] Make another [backup](./assets/liana-backup-2025-03-26T12-47-22.json)

- [x] remove wallet
- [x] stp & restart bitcoind

- [x] import wallet

- [x] rescan
- [x] address label is present
- [x] coin label is present
- [x] aliases are present

- [x] Register on Bitbox02 (Settings)
- [x] Register on Ledger (Settings)

- [x] rotate coin
  - [x] click refresh button in home panel
  - [x] Check signing flow w/ Coldcard

- [x] recovery sweep at 1 sats/vb
  - [x] Check signing flow w/ Coldcard
  - [x] Check signing flow w/ BitBox02
  - [x] broadcast

- [ ] recovery sweep at 10 sats/vb
  - [ ] broadcast
    - [ ] warning about tx replaced
    - [ ] tx replaced in mempool & mined

## Setup 2 Inheritance regtest external electrs

- [x] ColdCard(A)
  - c658b283

- [x] BitBox02(B)
  - e2e975b7

- [x] Generate new wallet 
  - wsh(or_d(pk([c658b283/48'/1'/0'/2']tpubDFL5wzgPBYK5pZ2Kh1T8qrxnp43kjE5CXfguZHHBrZSWpkfASy5rVfj7prh11XdqkC1P3kRwUPBeX7AHN8XBNx8UwiprnFnEm5jyswiRD4p/<0;1>/*),and_v(v:pkh([e2e975b7/48'/1'/0'/2']tpubDFkztzafRmw9sd9V2jwgiv5eafAAZmfQX5huqBLzbfFcNUzkCCWN2kpYHkjhzWvwrQuckyxmruVka7DWtzNRPy4Bpgty4vr9Sx6U5QmhGrw/<0;1>/*),older(200))))#0c8rrk2d
  - [x] [backup](./assets/setup_2.json)

- [x] Register on Coldcard (Installer)
- [x] Register on Bitbox (Installer)

- [x] Receive regtest wallet

- [x] spend coin w/ change
  - [x] Check signing flow w/ Coldcard
  - [x] broadcast

- [x] bump fee 10 sats/vb
  - [x] broadcast
  - [x] warning about tx replaced
  - [x] tx replaced in mempool & mined

- [x] cancel tx
  - [x] broadcast
  - [x] warning about tx replaced
  - [x] generate block
  - [x] tx replaced in mempool & mined

- [x] spend coin w/o change
  - [x] Check signing flow w/ Coldcard
  - [x] broadcast

- [fail] bump fee 10 sats/vb
  - [ ] broadcast
  - [ ] warning about tx replaced
  - [ ] tx replaced in mempool & mined

- [x] cancel tx
  - [x] broadcast
  - [x] warning about tx replaced
  - [x] generate block
  - [x] tx replaced in mempool & mined

- [x] recovery sweep at 1 sats/vb
  - [x] Check signing flow w/ BitBox02
  - [x] broadcast

- [x] export [transactions](./assets/liana-txs-setup_2.csv)
- [x] export [labels](./assets/liana-labels-setup2.jsonl)
- [x] export [descriptor](./assets/liana-0c8rrk2d.descriptor)
- [x] export [backup](./assets/liana-backup-setup2.json)

## miner user

- [x] create wallet
- [x] send 450 coins w/ nano s+ => 27 minutes

## coldcard airgap flow

- [x] export descriptor to sd-card
- [x] register descriptor on mk4
- [x] export psbt
- [x] sign
- [x] import PSBT
- [x] broadcast

## Setup 3 Multisig template WS backend signet on 2 machines

- [x] ColdCard(A) Machine 1
  - c658b283

- [x] Jade (B) Machine 2
  - 0e266cd1

- [x] Bitbox (C) Machine 1
  - e2e975b7

- [x] Generate new wallet tr(A & B | thresh(2,A,B,C) & 1 block)
  - wsh(or_i(and_v(v:thresh(2,pkh([c658b283/48'/1'/0'/2']tpubDFL5wzgPBYK5pZ2Kh1T8qrxnp43kjE5CXfguZHHBrZSWpkfASy5rVfj7prh11XdqkC1P3kRwUPBeX7AHN8XBNx8UwiprnFnEm5jyswiRD4p/<2;3>/*),a:pkh([0e266cd1/48'/1'/0'/2']tpubDEFZePEvLmrRCsQu1M1H8RTTrLFBsmvSorPv5n9ybuvc8HcB4LrspavJDbfu5vtZWYfVj356KKFZ77RK6xLPuRTDc1Vv1tYubLAr5qAxozY/<2;3>/*),a:pkh([e2e975b7/48'/1'/0'/2']tpubDFkztzafRmw9sd9V2jwgiv5eafAAZmfQX5huqBLzbfFcNUzkCCWN2kpYHkjhzWvwrQuckyxmruVka7DWtzNRPy4Bpgty4vr9Sx6U5QmhGrw/<0;1>/*)),older(1)),and_v(v:pk([c658b283/48'/1'/0'/2']tpubDFL5wzgPBYK5pZ2Kh1T8qrxnp43kjE5CXfguZHHBrZSWpkfASy5rVfj7prh11XdqkC1P3kRwUPBeX7AHN8XBNx8UwiprnFnEm5jyswiRD4p/<0;1>/*),pk([0e266cd1/48'/1'/0'/2']tpubDEFZePEvLmrRCsQu1M1H8RTTrLFBsmvSorPv5n9ybuvc8HcB4LrspavJDbfu5vtZWYfVj356KKFZ77RK6xLPuRTDc1Vv1tYubLAr5qAxozY/<0;1>/*))))#xwjre4ae
  - [x] [backup](./assets/liana-backup-setup3-installer.json)

- [x] Register on Coldcard (Installer)
- [x] Register on Bitbox (Installer)

- [x] Use liana connect

- [x] Receive wallet

- [x] spend coin to self
  - [x] Check signing flow w/ Coldcard Machine A
  - [x] Check signing flow w/ Ledger B

- [x] recovery sweep at 1 sats/vb Machine A + Machine B
  - [x] Check signing flow w/ BitBox02
  - [x] Check signing flow w/ Ledger


### New opened issues/PRs

