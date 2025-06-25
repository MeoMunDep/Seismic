# 🚀 Bot Setup Instructions

Welcome to the bot setup guide! Follow the steps below to install and configure the bot correctly. This guide is designed to be beginner-friendly, with clear explanations for each step.

> [Termux guides if you run on mobile](https://github.com/MeoMunDep/Guides-for-using-my-script-on-termux)

---

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Installation Steps](#installation-steps)
3. [Configuration Files](#configuration-files)
   - [`configs.json`](#1-configsjson)
   - [`privateKeys.txt`](#2-privateKeystxt)
   - [`proxies.txt`](#4-proxiestxt)
4. [Running the Bot](#running-the-bot)
5. [Contact and Support](#contact-and-support)

---

## Prerequisites

Before running the bot, make sure you have the following installed:

- **Node.js** (Version: `22.11.0`)
- **npm** (Version: `10.9.0`)

Download Node.js and npm here: [Download Link](https://t.me/KeoAirDropFreeNe/257/1462).

-> On Windows, double click on `run.bat`. For Linux/macOS, use `run.sh` to automatically run the bot. Remember to fill in all the necessary details before running.

---

## Installation Steps

### 1. **Clone the Bot Repository (GitHub)**

You can clone the bot repository using Git. If you don't have Git installed, [install Git here](https://git-scm.com/).

- Open your terminal (Command Prompt on Windows, Terminal on Linux/macOS) and navigate to the folder where you want to store the bot files.

- Run the following command to clone the repository:

  ```bash
  git clone https://github.com/MeoMunDep/siesmic.git
  ```

- After cloning, navigate into the bot's directory:

  ```bash
  cd seismic/seismic
  ```

### 2. **Install Dependencies:**

- Once inside the bot directory, install the necessary dependencies by running the following command:

```bash
npm install --force user-agents axios colors https-proxy-agent socks-proxy-agent ethers web3 solc
```

- If you're on **Windows** and encounter an Execution Policy error, run:

```bash
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Then, run the npm install command again.

- For **Linux/macOS**, if you face permission issues with the install command, prepend `sudo` to the command:

```bash
sudo npm install --force user-agents meo-forkcy-utils meo-forkcy-colors https-proxy-agent socks-proxy-agent ethers web3 solc
```

### 3. **Prepare Configuration Files:**

- Ensure all configuration files are set up correctly before running the bot (see [Configuration Files](#configuration-files) section).

---

## Configuration Files

### 1. `configs.json` - 📜 Adjust Bot Settings

This file controls the bot’s behavior. Below is an example configuration:

```json
{
  "howManyAccountsRunInOneTime": 200,
  "timeToRestartAllAccounts": 300,
  "delayEachAccount": [1, 2],
  "skipInvalidProxy": true,

  "tokenConfig": {
    "performTransfers": true,
    "numTransfers": [5, 10],
    "amountPerTransfer": [1000, 2000],
    "useConfiguredAddresses": false,
    "recipientAddresses": [""]
  },

   "faucet": {
    "maxCaptchaAttempts": 20,
    "2captchaApiKey": ""
  }
}
```

### 🔧 Main Configuration

| Field | Type | Description |
|-------|------|-------------|
| `howManyAccountsRunInOneTime` | `number` | Number of accounts to run concurrently in each batch. |
| `timeToRestartAllAccounts` | `number` | Time (in seconds) after which all accounts will be restarted. |
| `delayEachAccount` | `[number, number]` | Random delay range (in seconds) between processing each account. E.g., `[1, 2]` means a delay between 1 and 2 seconds. |
| `skipInvalidProxy` | `boolean` | If `true`, accounts with invalid proxies will be skipped instead of stopping execution. |

---

### 💰 `tokenConfig` – Token Deployment & Transfer Settings

| Field | Type | Description |
|-------|------|-------------|
| `performTransfers` | `boolean` | If `true`, token transfers will be performed after deployment. |
| `numTransfers` | `number` | Number of transfer actions to execute if `performTransfers` is enabled. |
| `amountPerTransfer` | `[number, number]` | Random token amount (between `min` and `max`) to send in each transfer. When transfer ETH(SEISMIC) it will divide by 100000 |
| `useConfiguredAddresses` | `boolean` | If `true`, transfers will only use addresses specified in `recipientAddresses`. |
| `recipientAddresses` | `string[]` | Array of wallet addresses to receive tokens (used only if `useConfiguredAddresses` is `true`). |

---

### 🚰 `faucet` – Faucet Claim Settings

| Field | Type | Description |
|-------|------|-------------|
| `maxCaptchaAttempts` | `number` | Maximum number of attempts allowed to solve CAPTCHA before giving up. |
| `2captchaApiKey` | `string` | Your API key for 2Captcha service, used to automatically solve CAPTCHA challenges. |

---

### 2. `privateKeys.txt` - 🗂️ User's Wallet Data

- Wallets generator: [Link](https://github.com/MeoMunDep/Automatic-Ultimate-Create-Wallets-for-Airdrop)
- EVM PRIVATEKEY

```txt
privatekey
privatekey
privatekey
```

_Note: Each row for each account._

### 3. `proxies.txt` - 🌐 Proxy List (Optional)

If you are using proxies, add them here. Leave the file blank if you are not using proxies. Supported formats:

- [Get it from here](https://www.webshare.io/?referral_code=4l5kb3glsce7)

```txt
http://host:port
https://host:port
socks4://host:port
socks5://host:port
http://user:password@host:port
https://user:password@host:port
socks4://user:password@host:port
socks5://user:password@host:port
```

_Note: each row for each account._

---

## Running the Bot

1. Navigate to the folder containing the bot files:

   ```bash
   cd /path/to/seismic
   ```

2. Run the bot using the following command:

   ```bash
   node meomundep.js
   ```

---

## Contact and Support

- **Faucet Link** [Here](https://faucet-2.seismicdev.net/)
- **Seismic document** [Link](https://docs.seismic.systems/appendix/devnet)

- **Support me via Donate** [Here](https://t.me/KeoAirDropFreeNe/312/27801)
- **Contact for work:** [Telegram](https://t.me/MeoMunDep)
- **Join the support group:** [Join here](https://t.me/KeoAirDropFreeNe)
- **Updates Channel:** [View channel](https://t.me/KeoAirDropFreeNee)
- **YouTube Channel:** [Watch here](https://www.youtube.com/@keoairdropfreene)
- **Instagram:** [Follow me](https://www.instagram.com/meomundep)
- **Tiktok:** [Follow me](https://www.tiktok.com/@meomundep)

Your support is greatly appreciated! 🐱

---

Enjoy using the bot! 🚀
