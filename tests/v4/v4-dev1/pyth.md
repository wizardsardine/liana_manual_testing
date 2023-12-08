# Signet faucet wallet (Sparrow)

- Mnemonic: rigid brother public ship curve holiday scrub plate furnace emerge weather derive
- P2PKH Descriptor => pkh([f004c855/44h/1h/0h]tpubDDmdqvCYBbUfSTV9r32Y9YeVH6tGySpK9VcxtZkXzpCLnZGZjD4D3RFNzNY2zRX9R22NsnGDhdXzieRhcmH7hKzcRn4aNqXusshoofHaieL/<0;1>/*)#65t0v9j8
- P2WPKH Descriptor => wpkh([f004c855/84h/1h/0h]tpubDDHWhCWGVx5BKaQRB55MTSwRJxNweb7YcXbiFBSgTjKn9sZ7xsGd6KxniBKZ1JiAk5EqL82ACfKPDtDnYYL7AhPYmDXDMpdjg2stjWkQ9m6/<0;1>/*)#49r7mq6p
- P2SH-P2WPKH Descriptor => sh(wpkh([f004c855/49h/1h/0h]tpubDCw3mF6vhBuv44sHkWtQdU2M7KNw9xUgrmzyZ9aK1utwegRWpd6GWjsvZiq3pnfdvNf8AX6kc82QweEXQ3HMoUoUQbiv7Qc6Z975KuT2G7Z/<0;1>/*))#0umhqc52
- P2TR Descriptor => tr([f004c855/86h/1h/0h]tpubDCQ5sLb3EZF5wgPzGaB9Nsxp9MAgfMhvmwxmjkYsSCFEp696nqrzDXWrZ9c3niMkpXbGJK78cVAy7QPkRotRshRAr26pMLsANA2uKEDFzqj/<0;1>/*)#y4mmnsqu

# Template
- [x] Build <platform> commit ed35a796ffa07948ca27b1d58312ae600839c70e

## test coin selection Nano S v2.2.0-beta

- [x] Generate 1 hot seed (A)
  - [501faa8c/48'/1'/0'/2']tpubDFhtc3gCzD9VEcnhRePA8vuBHP9C68zMYzZTmroo6DyXNQFYadasdEAqiUcxe3YrcJXLZU3PGjo5tBGRq2vMMcwZ7xBQMBirgj22AZyj9d1
  - evolve reunion joy victory vault middle ribbon patch amused weird polar fault
- [x] Import seed #1 on <signer> (Specter)
  - hotel organ vacuum praise bacon gentle love another absurd crystal cloud window
  - [6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r
- [x] Import seed #2 on <signer> (Ledger Nano S)
  - video cupboard ketchup sock armed color mobile rhythm marble credit until mosquito
  - [d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW
- [x] Generate new wallet multi(3, A, B, C) | multi(2, A, B, C) & 10 blocks | multi(1, A, B, C) & 10 Blocks
  - wsh(or_i(and_v(v:thresh(1,pkh([501faa8c/48'/1'/0'/2']tpubDFhtc3gCzD9VEcnhRePA8vuBHP9C68zMYzZTmroo6DyXNQFYadasdEAqiUcxe3YrcJXLZU3PGjo5tBGRq2vMMcwZ7xBQMBirgj22AZyj9d1/<4;5>/*),a:pkh([d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<4;5>/*),a:pkh([6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<4;5>/*)),older(10)),or_d(multi(3,[501faa8c/48'/1'/0'/2']tpubDFhtc3gCzD9VEcnhRePA8vuBHP9C68zMYzZTmroo6DyXNQFYadasdEAqiUcxe3YrcJXLZU3PGjo5tBGRq2vMMcwZ7xBQMBirgj22AZyj9d1/<0;1>/*,[d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<0;1>/*,[6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<0;1>/*),and_v(v:thresh(2,pkh([501faa8c/48'/1'/0'/2']tpubDFhtc3gCzD9VEcnhRePA8vuBHP9C68zMYzZTmroo6DyXNQFYadasdEAqiUcxe3YrcJXLZU3PGjo5tBGRq2vMMcwZ7xBQMBirgj22AZyj9d1/<2;3>/*),a:pkh([d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<2;3>/*),a:pkh([6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<2;3>/*)),older(5)))))#xzdr8y0d
- [x] Let Liana handle bitcoind
- [x] Register on Specter
- [ fail ] Register on Nano S v2.2.0-beta
- [ ] Receive from <type> faucet (<?> coin, <?> change)
- [ ] send back to <type> faucet (<?> coins, <?> change) primary path

## test coin selection round2 nano S v2.1.2

- [x] Generate 1 hot seed (A)
  - fee inner guitar milk over now trust van eternal duck army energy
  - [68b68c88/48'/1'/0'/2']tpubDFKn7QhbfPsnXfaTSXirWketv86Nx8zZmHhfp15hC7SaG51BMSc9RGvnVPuX18ZK6Fiqi7CE4hRU1SMo2dJq2fmXUgTWsKHoZYYf9rVGWXW
- [x] Import seed #1 on <signer> (Specter)
  - hotel organ vacuum praise bacon gentle love another absurd crystal cloud window
  - [6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r
- [x] Import seed #2 on <signer> (Ledger Nano S)
  - video cupboard ketchup sock armed color mobile rhythm marble credit until mosquito
  - [d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW
- [x] Generate new wallet multi(3, A, B, C) | multi(2, A, B, C) & 10 blocks | multi(1, A, B, C) & 10 Blocks
  - wsh(or_i(and_v(v:thresh(1,pkh([68b68c88/48'/1'/0'/2']tpubDFKn7QhbfPsnXfaTSXirWketv86Nx8zZmHhfp15hC7SaG51BMSc9RGvnVPuX18ZK6Fiqi7CE4hRU1SMo2dJq2fmXUgTWsKHoZYYf9rVGWXW/<4;5>/*),a:pkh([d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<4;5>/*),a:pkh([6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<4;5>/*)),older(65535)),or_d(multi(3,[68b68c88/48'/1'/0'/2']tpubDFKn7QhbfPsnXfaTSXirWketv86Nx8zZmHhfp15hC7SaG51BMSc9RGvnVPuX18ZK6Fiqi7CE4hRU1SMo2dJq2fmXUgTWsKHoZYYf9rVGWXW/<0;1>/*,[d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<0;1>/*,[6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<0;1>/*),and_v(v:thresh(2,pkh([68b68c88/48'/1'/0'/2']tpubDFKn7QhbfPsnXfaTSXirWketv86Nx8zZmHhfp15hC7SaG51BMSc9RGvnVPuX18ZK6Fiqi7CE4hRU1SMo2dJq2fmXUgTWsKHoZYYf9rVGWXW/<2;3>/*),a:pkh([d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<2;3>/*),a:pkh([6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<2;3>/*)),older(5)))))#pc5pevqr
- [x] Let Liana handle bitcoind
- [x] Register on Specter
- [ fail ] Register on Nano S v2.2.0-beta
- [ ] Receive from <type> faucet (<?> coin, <?> change)
- [ ] send back to <type> faucet (<?> coins, <?> change) primary path

## test coin selection round3 nano S v2.1.2 + liana v3

- [x] Generate 1 hot seed (A)
  - blush easy way dog warfare behind chicken room sock habit illegal actual
  - [b330636d/48'/1'/0'/2']tpubDEbBZhfk8runA11SMHcfgfK86ms9xEbau8KrH4Rd8BWoeLAzzNKzaMQVh2UczeHGQKKwcxVyjGrfkvsXAGJYS1MYNQGr8qno8q74kKjBJHF
- [x] Import seed #1 on <signer> (Specter)
  - hotel organ vacuum praise bacon gentle love another absurd crystal cloud window
  - [6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r
- [x] Import seed #2 on <signer> (Ledger Nano S)
  - video cupboard ketchup sock armed color mobile rhythm marble credit until mosquito
  - [d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW
- [x] Generate new wallet multi(3, A, B, C) | multi(2, A, B, C) & 10 blocks | multi(1, A, B, C) & 10 Blocks
  - wsh(or_i(and_v(v:thresh(2,pkh([b330636d/48'/1'/0'/2']tpubDEbBZhfk8runA11SMHcfgfK86ms9xEbau8KrH4Rd8BWoeLAzzNKzaMQVh2UczeHGQKKwcxVyjGrfkvsXAGJYS1MYNQGr8qno8q74kKjBJHF/<4;5>/*),a:pkh([d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<4;5>/*),a:pkh([6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<4;5>/*)),older(5)),or_d(multi(3,[b330636d/48'/1'/0'/2']tpubDEbBZhfk8runA11SMHcfgfK86ms9xEbau8KrH4Rd8BWoeLAzzNKzaMQVh2UczeHGQKKwcxVyjGrfkvsXAGJYS1MYNQGr8qno8q74kKjBJHF/<0;1>/*,[d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<0;1>/*,[6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<0;1>/*),and_v(v:thresh(2,pkh([b330636d/48'/1'/0'/2']tpubDEbBZhfk8runA11SMHcfgfK86ms9xEbau8KrH4Rd8BWoeLAzzNKzaMQVh2UczeHGQKKwcxVyjGrfkvsXAGJYS1MYNQGr8qno8q74kKjBJHF/<2;3>/*),a:pkh([d4ab66f1/48'/1'/0'/2']tpubDEXYN145WM4rVKtcWpySBYiVQ229pmrnyAGJT14BBh2QJr7ABJswchDicZfFaauLyXhDad1nCoCZQEwAW87JPotP93ykC9WJvoASnBjYBxW/<2;3>/*),a:pkh([6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<2;3>/*)),older(3)))))#5ql6plwq
- [x] Let Liana handle bitcoind
- [x] Register on Specter
- [ fail ] Register on Nano S v2.2.0-beta
- [ ] Receive from <type> faucet (<?> coin, <?> change)
- [ ] send back to <type> faucet (<?> coins, <?> change) primary path

## test coin selection round4 nano S v2.1.2 + new 24words seed

- [x] Generate 1 hot seed (A)
  - decrease struggle broken buddy wear useful joy sugar evolve enlist weekend laptop
  - [1b2c0a43/48'/1'/0'/2']tpubDEZ1YySP7sDmu2isUhtxoAAnaH2xF6jbzaDqMaBkJYmWbtCKaR4Vz7YTq1oyg1Torqjn8np9AkD5t5fPDDu2Tku5v3Dbk62HW1qambSJGAk
- [x] Import seed #1 on (Specter)
  - hotel organ vacuum praise bacon gentle love another absurd crystal cloud window
  - [6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r
- [x] Import seed #2 on (Ledger Nano S)
  - bomb sphere swim sphere must frame bounce ticket title winner tide decrease shuffle minute ugly seminar dash awful calm olive census girl merit smooth 
  - [7cab1066/48'/1'/0'/2']tpubDDvqWeedNeqAfoMYPAV5ewJcgQEuuAC9en8UzxZ3PSqiDZcjpLZSXs9yu2S4hYcQb6S7UrSy8eBvk199WgzAsjWmaE8TW87q3riaXfWcRQ6
- [x] Generate new wallet multi(3, A, B, C) | multi(2, A, B, C) & 10 blocks | multi(1, A, B, C) & 10 Blocks
  - wsh(or_d(multi(2,[1b2c0a43/48'/1'/0'/2']tpubDEZ1YySP7sDmu2isUhtxoAAnaH2xF6jbzaDqMaBkJYmWbtCKaR4Vz7YTq1oyg1Torqjn8np9AkD5t5fPDDu2Tku5v3Dbk62HW1qambSJGAk/<0;1>/*,[7cab1066/48'/1'/0'/2']tpubDDvqWeedNeqAfoMYPAV5ewJcgQEuuAC9en8UzxZ3PSqiDZcjpLZSXs9yu2S4hYcQb6S7UrSy8eBvk199WgzAsjWmaE8TW87q3riaXfWcRQ6/<0;1>/*,[6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<0;1>/*),and_v(v:thresh(1,pkh([1b2c0a43/48'/1'/0'/2']tpubDEZ1YySP7sDmu2isUhtxoAAnaH2xF6jbzaDqMaBkJYmWbtCKaR4Vz7YTq1oyg1Torqjn8np9AkD5t5fPDDu2Tku5v3Dbk62HW1qambSJGAk/<2;3>/*),a:pkh([7cab1066/48'/1'/0'/2']tpubDDvqWeedNeqAfoMYPAV5ewJcgQEuuAC9en8UzxZ3PSqiDZcjpLZSXs9yu2S4hYcQb6S7UrSy8eBvk199WgzAsjWmaE8TW87q3riaXfWcRQ6/<2;3>/*),a:pkh([6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<2;3>/*)),older(3))))#rncv6x8m
- [x] Let Liana handle bitcoind
- [x] Register on Specter
- [ fail ] Register on Nano S v2.2.0-beta
- [ ] Receive from <type> faucet (<?> coin, <?> change)
- [ ] send back to <type> faucet (<?> coins, <?> change) primary path

## test coin selection 

- [x] Generate 1 hot seed (A)
  - [6f21a59a/48'/1'/0'/2']tpubDEca8oRoQBG3tco1ZQK47VJv8qVxhhzb6d88F85pS89qewYN3bR3t6kqAqQdhx5jjJxmQxAz9Q71639D3BQw6e1H42Bk34SbV4ABe2sWD39
  - pencil debris divide family fantasy exhaust fluid treat attack soon axis ketchup
- [x] Import seed #1 on (Specter)
  - hotel organ vacuum praise bacon gentle love another absurd crystal cloud window
  - [6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r

- [x] Generate new wallet multi(2, A, B) | B & 3 blocks 
  - wsh(or_d(
  - multi(2,[6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<0;1>/*,[6f21a59a/48'/1'/0'/2']tpubDEca8oRoQBG3tco1ZQK47VJv8qVxhhzb6d88F85pS89qewYN3bR3t6kqAqQdhx5jjJxmQxAz9Q71639D3BQw6e1H42Bk34SbV4ABe2sWD39/<0;1>/*),and_v(v:pkh([6abb52a9/48'/1'/0'/2']tpubDFZTCVU1Sa9nJXCxx97UFvGausHQPFjJyaiDbdr8GNqjCLKwYc8ihegK7yJdcizs9HMbiGA7ke1HiCENVHaERvNANHW7U2Wo2qnRsuqB52r/<2;3>/*),older(3))))#0nkwvd0g
- [x] Let Liana handle bitcoind
- [x] Register on Specter
- [ ] Receive from <type> faucet (<?> coin, <?> change)
- [ ] send back to <type> faucet (<?> coins, <?> change) primary path

## test addresses verification

## Notes


