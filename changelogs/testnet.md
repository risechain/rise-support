# RISE Public Testnet Changelog

### Upgrade #6: More Shred-Enabled RPCs and Stability

- **Date:** 2025-04-07
- **Description:**
  - Cheaper gas price at `eth_gasPrice` and `eth_maxPriorityFeePerGas`
  - Much faster `eth_getBalance`, `eth_getCode` and `eth_getStorageAt` with shreds
  - Faster pending `eth_estimateGas` and `eth_call`
  - More stability improvements for both EL & CL
- **Action Items:**
  - Bump `rise-sequencer`, `rise-node`, and `rise-optimism` services with new images

---

### Upgrade #5: Enter Shreds!

- **Date:** 2025-04-04
- **Description:**
  - Fix a race condition when there are mempool transactions during an L1 reorg
  - Shreds with `rise_subscribe`!
  - Much faster `eth_blockNumber`, `eth_getTransactionByHash` and `eth_getTransactionReceipt` with shreds
  - Improve overall performance and block building stability
- **Action Items:**
  - Bump `rise-sequencer`, `rise-node`, and `rise-optimism` services with new images.

---

### Upgrade #4: Bump `rise-sequencer`, `rise-optimism`, and Deploy RISE Replicas

- **Date:** 2025-03-18
- **Description:**
  - Bump `rise-sequencer` to fix a race condition that led to wrong execution; and improve performance.
  - Replace `op-reth` with RISE's own replica `rise-node` for much better latency.
  - Rebase `rise-optimism` on [`op-node v1.2.0`](https://github.com/ethereum-optimism/optimism/releases/tag/op-node%2Fv1.12.0) for Pectra stability and improve performance.

---

### Upgrade #3: Update Public Testnet Explorer URL

- **Date:** 2025-03-06
- **Description:**
  - Update the public testnet explorer to https://explorer.testnet.riselabs.xyz.
  - The old URL (https://testnet-explorer.riselabs.xyz) now redirects to the new one.

---

### Upgrade #2: Bump `rise-optimism` for Sepolia Pectra

- **Date:** 2025-03-05
- **Description:** RISE tesnet broke after the Sepolia Pectra hardfork. We needed to bump `rise-optimism` to be compatible.

---

### Upgrade #1: Bump `rise`, `rise-optimism`, and `op-reth`

- **Date:** 2025-03-05
- **Description:**
  - Bump `rise`, `rise-optimism`, and `op-reth` to new versions for better performance.
  - Running the latest versions may help us fix or easier debug the recent receipts root issue on public testnet.
