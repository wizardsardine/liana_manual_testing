test made on top of afe5f6c0

 - [x] Build Arch

## Setup 1 => maxi wallet (local unmanaged bitcoind regtest) 

- [x] ColdCard(A)
  - c658b283

- [x] Nano S+ (B)
  - d4ab66f1

- [x] BitBox02(C)
  - e2e975b7

- [x] Generate new wallet tr( A || B & 50 blocks|| C & 100 blocks )
  - tr([c658b283/48'/1'/9'/2']tpubDFTvVpnXpYXFQv3TrjVSbivSYpVHnBomcHG5qxoaabZ8MjHi5iQ9q7xgJEaM1pwEe9QxmobXLae8t2HtxjYBUkZdoTMXPhL87N2iqRXcp7G/<0;1>/*,{and_v(v:pk([d4ab66f1/48'/1'/8'/2']tpubDEcnoakGw926LWF47MinynMNnqouVSW6qpgreHnesKEtL53Zs426EEdnJsCSQEvqCR1KB5E8JqUuyP35Wki3sc21b15KQZNn53ih6PEppZZ/<0;1>/*),older(50)),and_v(v:pk([e2e975b7/48'/1'/5'/2']tpubDFfQvtn4fio8kzJCPsZUiyrv93BAEwPWCSayKHABoT5ajRFMT18WoJCWS8NA6vywYuvUFwGv1RSakFJ5LzFjToSXRFesRwxPJadsF4S1pQD/<0;1>/*),older(100))})#8pyhv26y

- [x] [backup file](./assets/maxi_wallet.json)

- [x] close liana here
- [x] import the backup file

- [x] Register on Coldcard (Installer)
- [x] Register on Ledger (Installer)

- [x] Register on Bitbox (Settings)

- [x] Verify reception address w/ ColdCard
- [x] Verify reception address w/ Ledger
- [x] Verify reception address w/ Bitbox

- [x] Label address
- [x] Receive regtest wallet
- [x] Label coin
- [x] Make another [backup](./assets/maxi_wallet2.json)

- [x] remove wallet
- [x] stp & restart bitcoind

- [x] import wallet

- [x] rescan
- [x] address label is present
- [x] coin label is present
- [x] aliases are present

- [x] Register on Ledger (Settings)

- [x] rotate coin
  - [x] click refresh button in home panel
  - [x] Check signing flow w/ Coldcard

- [x] recovery sweep at 1 sats/vb
  - [x] Check signing flow w/ ledger
  - [x] broadcast

## Setup 2 Inheritance regtest external electrs

- [x] ColdCard(A)
  - c658b283

- [x] BitBox02(B)
  - e2e975b7

- [x] Generate new wallet 
  - wsh(or_d(pk([c658b283/48'/1'/4'/2']tpubDF34zRSZtCt3ZM9xEkJVunMZjB9wmUv6mP6McUzZkv3dbzMc9C6LnHtAHDxTAHddDSCgChkxsbvHwsMD1FW51ewHSrVezAoFRo1AHP8uSbr/<0;1>/*),and_v(v:pkh([e2e975b7/48'/1'/2'/2']tpubDFmD8DWkSX2KEd5TuSDE5sXTubFjQT4rb17zZ3xe3wwo9JaNZJvTZi4G23g4NJ5nXTXnR4mvcnewKGNeeRmQE583y6ANusDgpUudv6P9XjW/<0;1>/*),older(10))))#674jk4tt
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
  - [x] tx replaced in mempool

- [x] cancel tx
  - [x] broadcast
  - [x] warning about tx replaced
  - [x] tx replaced in mempool
  - [x] generate block
  - [x] tx mined

- [x] spend coin w/o change
  - [x] Check signing flow w/ Coldcard
  - [x] broadcast

- [x] bump fee 10 sats/vb
  - [x] broadcast
  - [x] warning about tx replaced
  - [x] tx replaced in mempool

- [x] cancel tx
  - [x] broadcast
  - [x] warning about tx replaced
  - [x] tx replaced in mempool
  - [x] generate block
  - [x] tx mined

- [x] recovery sweep at 1 sats/vb
  - [x] Check signing flow w/ BitBox02
  - [x] broadcast

- [x] export [transactions](./assets/setup2_tx.csv)
- [x] export [labels](./assets/setup2_labels.jsonl)
- [x] export [descriptor](./assets/setup2_descriptor.txt)
- [x] export [backup](./assets/setup_2_end.json)

## coldcard airgap flow

- [x] export descriptor to sd-card
- [x] register descriptor on mk4
- [x] export psbt
- [x] sign
- [x] import PSBT
- [x] broadcast

## krux airgap flow

- [x] export descriptor to sd-card
- [x] register descriptor on mk4
- [x] export psbt
- [x] sign
- [x] import PSBT
- [x] broadcast

## Setup 3 Multisig template WS backend signet

- [x] Use liana connect

- [x] ColdCard(A)
  - c658b283

- [x] Jade (B)
  - 0e266cd1

- [x] Ledger (C)
  - e2e975b7

- [x] Generate new wallet wsh(A & B | thresh(2,A,B,C) & 10 block)
  - wsh(or_i(and_v(v:thresh(2,pkh([c658b283/48'/1'/1'/2']tpubDFm2m2rpqo9gfnXqxwTVDwDfdgpovAgt1BQw5bMrbHLeMsQZAZ7gd8wRKDoCBSxwycwa4g261YBwK7eMxXemWzFmAuKwqR82QiDpH73nqgG/<2;3>/*),a:pkh([0e266cd1/48'/1'/2'/2']tpubDEVPRs1SJrUmEWxaFExcNYXGJ2zwXR1Xv8jR1gDREuh7EB96iJ6nbmYMGs72xTRznqo7snRSVbtxZwnZ5N4KRjCtu6t1aXbFZX3sE7wZmUt/<2;3>/*),a:pkh([d4ab66f1/48'/1'/3'/2']tpubDELZQQSUMrTKnp2Wim3WVxMqbkpCYME6qHffwhdJ86Aatgn3xPHQE9JDvs7nerW1zmHPutMwpPt1kDdDHcwBB8vTSHbwqT31t6ztuzZ3CsV/<0;1>/*)),older(10)),and_v(v:pk([c658b283/48'/1'/1'/2']tpubDFm2m2rpqo9gfnXqxwTVDwDfdgpovAgt1BQw5bMrbHLeMsQZAZ7gd8wRKDoCBSxwycwa4g261YBwK7eMxXemWzFmAuKwqR82QiDpH73nqgG/<0;1>/*),pk([0e266cd1/48'/1'/2'/2']tpubDEVPRs1SJrUmEWxaFExcNYXGJ2zwXR1Xv8jR1gDREuh7EB96iJ6nbmYMGs72xTRznqo7snRSVbtxZwnZ5N4KRjCtu6t1aXbFZX3sE7wZmUt/<0;1>/*))))#hqfx9k8v
  - [x] [backup](./assets/setup3.json)

- [x] Register on Coldcard (Installer)
- [x] Register on Coldcard (Installer)
- [x] Register on Ledger (Installer)


- [x] Receive wallet

- [x] spend coin to self
  - [x] Check signing flow w/ Coldcard
  - [x] Check signing flow w/ Jade

- [x] recovery sweep at 1 sats/vb 
  - [x] Check signing flow w/ Ledger
  - [x] Check signing flow w/ Jade


