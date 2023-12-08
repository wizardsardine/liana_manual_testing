## Signet Faucet

Coins should be availables in a bunch of wallets used as faucet.

There is 4 wallets using same mnemonics:

 - P2PKH
 - P2SH-P2WPSH
 - P2WPKH
 - P2TR

 Relevants informations (mnemonics/desciptors) about this wallets can be found in `faucet` folder.

 These wallet have been generated using sparrow, you can launch sparrow in signet mode using `Sparrow -n signet`, then import it w/ File => Import wallet => Sparrow => Import file... or copy `.db` files in sparrow signet folder (~/.sparrow/signet/wallets/).

 These wallets can also be imported in core using descritors located in `faucet/bitcoin_core_descriptor/`.

## Test reports

Test reports are simple `.md` files containing checklists/notes (a file report template is available in TEMPLATE.md) and are stored in `tests/<version>/<stage>`.

Stages should be like:

 - v3
 - v4-dev1
 - v4-dev2
 - v4-dev-pr401
 - v4-pre-rc-1
 - v4-pre-rc-2
 - v4-rc1
 - v4-rc2
 - v4

Into the `<stage>` folder, you can name the report `<stage>/<your-nickname>.md` and store screenshot and external files relevant to your test in a folder `<stage>/<your-nickname>/`.

