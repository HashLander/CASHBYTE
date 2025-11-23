# CASHBYTE

CASHBYTE is a Komodo SmartChain and, by inheritance, a fork of Zcash. It supports both transparent and shielded transactions, offering optional privacy at the protocol level.

## Consensus Model

CASHBYTE uses a hybrid consensus mechanism:
- **55% Proof-of-Stake**
- **45% Proof-of-Work**

This model makes 51% attacks economically and practically unfeasible. All coinbase rewards require **20+ confirmations** to reach finality through `coinbase_maturity`.

## Key Specifications

- **Maximum Supply:** ~84,000,000 CBYTE  
- **Block Halving:** Every 3,000,000 blocks (≈ 4 years)  
- **Decimals:** 8 (Bitcoin-compatible)  
- **Token Support:** Fungible and Non-Fungible Tokens (NFTs)

## Motto

**BUILD. BUILD. BREATHE. BUILD MORE.**

## Official Website
https://cashbyte.cash

---

## Installation (Windows / Linux / macOS)

## GUI Wallet (Full Node)

- **Windows (QT Wallet):**  
  https://github.com/DeckerSU/KomodoOcean/releases/download/v0.9.1-beta2/komodo-qt-win.zip

- **Linux (QT Wallet):**  
  https://github.com/KomodoPlatform/komodo/releases/download/v0.9.1/komodo-0.9.1-linux.tar.gz

- **macOS (QT Wallet):**  
  https://github.com/DeckerSU/KomodoOcean/releases/download/v0.9.1-beta2/komodo-qt-mac.zip

### Start the QT Wallet on the CASHBYTE Chain

Launch the wallet with:

```
komodo-qt-win.exe -ac_name=CASHBYTE -ac_supply=2000000 -ac_cbmaturity=20 -ac_cc=2 -ac_blocktime=60 -ac_reward=2000000000 -ac_halving=2100000 -ac_end=70000000 -ac_staked=55 -addnode=172.93.187.46
```

Then, in another terminal:

```
komodo-cli.exe -ac_name=CASHBYTE addnode 172.93.187.46 add
komodo-cli.exe -ac_name=CASHBYTE addnode 172.93.187.46 onetry
```

After the wallet finishes syncing, you may start mining:

```
komodo-cli.exe -ac_name=CASHBYTE setgenerate true 2
```

(Replace **2** with the number of CPU cores you want to dedicate.)

---

## Daemon (Headless Node)

Download the daemon for your operating system:

- **Windows Daemon:**  
  https://github.com/KomodoPlatform/komodo/releases/download/v0.9.1/komodo-0.9.1-win.zip

- **Linux Daemon (Ubuntu 20/22 and related distros):**  
  https://github.com/KomodoPlatform/komodo/releases/download/v0.9.1/komodo-0.9.1-linux.tar.gz

- **macOS Daemon:**  
  https://github.com/KomodoPlatform/komodo/releases/download/v0.9.1/komodo-0.9.1-mac.zip

### Start the CASHBYTE Daemon

```
komodod.exe -ac_name=CASHBYTE -ac_supply=2000000 -ac_cbmaturity=20 -ac_cc=2 -ac_blocktime=60 -ac_reward=2000000000 -ac_halving=2100000 -ac_end=70000000 -ac_staked=55 -addnode=172.93.187.46
```

Add the official node:

```
komodo-cli.exe -ac_name=CASHBYTE addnode 172.93.187.46 add
komodo-cli.exe -ac_name=CASHBYTE addnode 172.93.187.46 onetry
```

After syncing, start mining:

```
komodo-cli.exe -ac_name=CASHBYTE setgenerate true 2
```

---

## CLI Commands

List all available RPC commands:

```
komodo-cli.exe -ac_name=CASHBYTE help


--------------------
If you prefer the source code: https://github.com/DeckerSU/KomodoOcean/archive/refs/tags/v0.9.1-beta2.tar.gz
