test made on top of v8rc1

# Template

 - [ ] Build Arch

## Setup 1 => maxi wallet (local unmanaged bitcoind regtest)

- [x] ColdCard(A)
  - fc898399

- [x] BitBox02(B)
  - e2e975b7

- [x] Jade (C)
  - 0e266cd1

- [x] Nano S+ (D)
  - d4ab66f1

  
- [x] Generate new wallet 
  - wsh(or_i(and_v(v:thresh(1,pkh([fc898399/48'/1'/0'/2']tpubDEEZZ8c3g9DJ55sp2aWHcZT8syRA5d26VZEdjBbVDaPAVJwKnf3cKY53dfnwecTXoLhocpGKzJkRJo1G271JnUnXRoE28Qo2b2pGUFhN1UV/<6;7>/*),a:pkh([e2e975b7/48'/1'/0'/2']tpubDFkztzafRmw9sd9V2jwgiv5eafAAZmfQX5huqBLzbfFcNUzkCCWN2kpYHkjhzWvwrQuckyxmruVka7DWtzNRPy4Bpgty4vr9Sx6U5QmhGrw/<6;7>/*),a:pkh([d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<4;5>/*),a:pkh([0e266cd1/48'/1'/0'/2']tpubDEFZePEvLmrRCsQu1M1H8RTTrLFBsmvSorPv5n9ybuvc8HcB4LrspavJDbfu5vtZWYfVj356KKFZ77RK6xLPuRTDc1Vv1tYubLAr5qAxozY/<4;5>/*)),older(3)),or_i(and_v(v:thresh(2,pkh([fc898399/48'/1'/0'/2']tpubDEEZZ8c3g9DJ55sp2aWHcZT8syRA5d26VZEdjBbVDaPAVJwKnf3cKY53dfnwecTXoLhocpGKzJkRJo1G271JnUnXRoE28Qo2b2pGUFhN1UV/<4;5>/*),a:pkh([e2e975b7/48'/1'/0'/2']tpubDFkztzafRmw9sd9V2jwgiv5eafAAZmfQX5huqBLzbfFcNUzkCCWN2kpYHkjhzWvwrQuckyxmruVka7DWtzNRPy4Bpgty4vr9Sx6U5QmhGrw/<4;5>/*),a:pkh([d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<2;3>/*),a:pkh([0e266cd1/48'/1'/0'/2']tpubDEFZePEvLmrRCsQu1M1H8RTTrLFBsmvSorPv5n9ybuvc8HcB4LrspavJDbfu5vtZWYfVj356KKFZ77RK6xLPuRTDc1Vv1tYubLAr5qAxozY/<2;3>/*)),older(2)),or_d(multi(2,[fc898399/48'/1'/0'/2']tpubDEEZZ8c3g9DJ55sp2aWHcZT8syRA5d26VZEdjBbVDaPAVJwKnf3cKY53dfnwecTXoLhocpGKzJkRJo1G271JnUnXRoE28Qo2b2pGUFhN1UV/<0;1>/*,[e2e975b7/48'/1'/0'/2']tpubDFkztzafRmw9sd9V2jwgiv5eafAAZmfQX5huqBLzbfFcNUzkCCWN2kpYHkjhzWvwrQuckyxmruVka7DWtzNRPy4Bpgty4vr9Sx6U5QmhGrw/<0;1>/*),and_v(v:thresh(3,pkh([fc898399/48'/1'/0'/2']tpubDEEZZ8c3g9DJ55sp2aWHcZT8syRA5d26VZEdjBbVDaPAVJwKnf3cKY53dfnwecTXoLhocpGKzJkRJo1G271JnUnXRoE28Qo2b2pGUFhN1UV/<2;3>/*),a:pkh([e2e975b7/48'/1'/0'/2']tpubDFkztzafRmw9sd9V2jwgiv5eafAAZmfQX5huqBLzbfFcNUzkCCWN2kpYHkjhzWvwrQuckyxmruVka7DWtzNRPy4Bpgty4vr9Sx6U5QmhGrw/<2;3>/*),a:pkh([d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<0;1>/*),a:pkh([0e266cd1/48'/1'/0'/2']tpubDEFZePEvLmrRCsQu1M1H8RTTrLFBsmvSorPv5n9ybuvc8HcB4LrspavJDbfu5vtZWYfVj356KKFZ77RK6xLPuRTDc1Vv1tYubLAr5qAxozY/<0;1>/*)),older(1))))))#20uzjjwh

- [x] remove the wallet
- [x] import the modified wallet ....

- [x] Register on Coldcard (Installer)
- [x] Register on Bitbox (Installer)
- [x] Register on Jade (Installer)
- [x] Register on Ledger (Installer)

- [x] Verify recption address w/ Bitbox02
- [x] Verify recption address w/ ColdCard
- [x] Verify recption address w/ Ledger
- [x] Verify recption address w/ Jade

- [x] Receive regtest wallet

- [x] Register on Jade (Settings)
- [x] Register on Coldcard (Settings)
- [no menu on the device to remove already registered descriptor] Register on Bitbox02
- [x] Register on Ledger (Settings)

- [x] rotate coin
  - [x] Check signing flow w/ Coldcard
    - [x] appear as slf transfert
  - [x] Check signing flow w/ Bitbox
    - [x] appear as slf transfert

- [x] recovery sweep at 1 sats/vb
  - [x] Check signing flow w/ Coldcard
  - [x] Check signing flow w/ BitBox02
  - [x] broadcast

- [x] recovery sweep at 10 sats/vb
  - [x] Check signing flow w/ Nano S+
  - [x] Check signing flow w/ Jade
  - [x] broadcast
    - [x] warning about tx replaced
    - [x] tx replaced in mempool & mined

## Setup 2 Inheritance regtest external electrs
- [x] ColdCard(A)
  - fc898399

- [x] BitBox02(B)
  - e2e975b7

- [x] Generate new wallet 
  - tr([fc898399/48'/1'/0'/2']tpubDEEZZ8c3g9DJ55sp2aWHcZT8syRA5d26VZEdjBbVDaPAVJwKnf3cKY53dfnwecTXoLhocpGKzJkRJo1G271JnUnXRoE28Qo2b2pGUFhN1UV/<0;1>/*,and_v(v:pk([e2e975b7/48'/1'/0'/2']tpubDFkztzafRmw9sd9V2jwgiv5eafAAZmfQX5huqBLzbfFcNUzkCCWN2kpYHkjhzWvwrQuckyxmruVka7DWtzNRPy4Bpgty4vr9Sx6U5QmhGrw/<0;1>/*),older(65535)))#usrcheph

- [x] Register on Coldcard (Installer)
- [x] Register on Bitbox (Installer)

- [x] Receive regtest wallet

- [x] spend coin
  - [x] Check signing flow w/ Coldcard

- [x] recovery sweep at 1 sats/vb
  - [x] Check signing flow w/ BitBox02
  - [x] broadcast

## Setup 3 Multisig template WS backend signet taproot
- [x] ColdCard(A)
  - fc898399

- [x] BitBox02(B)
  - e2e975b7

- [x] Nano S+ (C)
  - d4ab66f1

- [x] Generate new wallet 
  - tr(tpubD6NzVbkrYhZ4XCoeWzLy2H9dv5sbUsEjitjzgcmHWYBHnBHnbCnFRPLLhw7yreXFg8qmd2pGpnbkxYSPxLszWLc1p1sQwYUu3nVmWejzMrS/<0;1>/*,{and_v(v:multi_a(2,[fc898399/48'/1'/0'/2']tpubDEEZZ8c3g9DJ55sp2aWHcZT8syRA5d26VZEdjBbVDaPAVJwKnf3cKY53dfnwecTXoLhocpGKzJkRJo1G271JnUnXRoE28Qo2b2pGUFhN1UV/<2;3>/*,[e2e975b7/48'/1'/0'/2']tpubDFkztzafRmw9sd9V2jwgiv5eafAAZmfQX5huqBLzbfFcNUzkCCWN2kpYHkjhzWvwrQuckyxmruVka7DWtzNRPy4Bpgty4vr9Sx6U5QmhGrw/<2;3>/*,[d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<0;1>/*),older(1)),multi_a(2,[fc898399/48'/1'/0'/2']tpubDEEZZ8c3g9DJ55sp2aWHcZT8syRA5d26VZEdjBbVDaPAVJwKnf3cKY53dfnwecTXoLhocpGKzJkRJo1G271JnUnXRoE28Qo2b2pGUFhN1UV/<0;1>/*,[e2e975b7/48'/1'/0'/2']tpubDFkztzafRmw9sd9V2jwgiv5eafAAZmfQX5huqBLzbfFcNUzkCCWN2kpYHkjhzWvwrQuckyxmruVka7DWtzNRPy4Bpgty4vr9Sx6U5QmhGrw/<0;1>/*)})#yrh3g7v0

- [x] Register on Coldcard (Installer)
- [x] Register on Bitbox (Installer)
- [x] Register on Ledger (Installer)

- [x] Receive regtest wallet

- [x] spend coin
  - [x] Check signing flow w/ Coldcard
  - [x] Check signing flow w/ BitBox

- [x] recovery sweep at 1 sats/vb
  - [x] Check signing flow w/ BitBox02
  - [x] Check signing flow w/ Ledger
  - [x] broadcast

## PRs

 - [ ] #1359 fix history events and txs pagination
 - [ ] #1358 hw: check if app is open before sending old version error message
 - [ ] #1381 Change primary and secondary button for consistency
 - [ ] #1370 [GUI] Indicate wallet is syncing after completing installer
 - [ ] #1390 doc: fix broken link to Edouard PGP key
 - [ ] #1387 [GUI] Don't treat wallets using bitcoind as syncing
 - [ ] #1395 Fix lianalite resend token
 - [ ] #1394 electrum: use debug log level for sync messages
 - [ ] #1376 Get timestamp of last completed poll of the blockchain
 - [ ] #1377 [GUI] Consider wallet to be syncing until first poll completes after opening
 - [ ] #1386 [GUI] Skip loading screen for existing wallets
 - [ ] #1366 Add templates to installer descriptor editor
 - [ ] #1399 Template multisig security
 - [ ] #1396 gui: upgrade managed bitcoind version to 28.0
 - [ ] #1403 Disable edit of defined key in multisig template recovery path
 - [ ] #1417 gui(installer): re-add next button when starting managed bitcoind
 - [ ] #1413 bump gui msrv to 1.71.1
 - [ ] #1419 gui(edit key modal): increase size of the closing icon
 - [ ] #1400 gui: add support for tapminiscript on bitbox02
 - [ ] #1421 Refresh cache more often in GUI while wallet or blockchain is syncing
 - [ ] #1415 gui(installer): add space at bottom of pages
 - [ ] #1430 gui(installer): better warn. if a signer is not compatible w/ tapminiscript
 - [ ] #1412 gui(installer): make edit key modal scrollable
 - [ ] #1422 gui(installer): apply wording changes to installer templates
 - [ ] #1428 gui(installer): align title & descrpition in path cards
 - [ ] #1404 Refac pagination: sort list in async command
 - [ ] #1431 gui(installer): display warning & selected icons
 - [ ] #1350 Add compression algo flag to dpkg command for arch build
 - [ ] #1441 gui(installer): fix word plurality when adding keys
 - [ ] #1442 gui(installer): use fixed keys ordering
 - [ ] #1446 gui(installer): list wallets using secondary buttons


### Successfully checked


## Comments

### Related w/ closed issues


### New opened issues/PRs

