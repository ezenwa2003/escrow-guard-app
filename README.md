# EscrowGuard app

A web app for the EscrowGuard Intelligent Contract on GenLayer Studionet. A client locks GEN for a job, a freelancer submits their delivery, and if they disagree, validators read the evidence and decide who is paid.

**Live app:** https://ezenwa2003.github.io/escrow-guard-app/

**Contract source:** https://github.com/ezenwa2003/escrow-guard (`escrow_guard.py`)

## Try it without a wallet

Open the live app and click **Try the example**. It loads a finished escrow (`0x11D33E7d5CA2D8201088E14323F6B38adCd38ED4`) and shows the result: 1 GEN was locked, the validators ruled that the client should be refunded, and the contract paid the money back.

## How it works

1. Paste the address of a deployed EscrowGuard contract.
2. Connect a browser wallet (Rabby or MetaMask). The app switches it to Studionet.
3. Each wallet only sees the buttons for its own role and the current stage:
   - the client locks funds,
   - the freelancer submits the delivery,
   - the client approves, or raises a dispute,
   - on a dispute, validators fetch the delivery link, weigh both sides, and the contract pays the winner.

The coin on the track shows which stage the escrow is in.

## Built with

One `index.html` file using the official `genlayer-js` SDK. No build step.

## Run it yourself

Host the file with GitHub Pages, or serve the folder locally. Wallet extensions work on `https://` pages and on `localhost`, but not reliably when the file is opened straight from disk.

## Status

Tested on GenLayer Studionet only. Not tested on public testnets.
