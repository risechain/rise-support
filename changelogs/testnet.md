# RISE Public Testnet Changelog

### Upgrade #11: Key Rollup Improvements

- **Date:** 2025-06-23
- **Description:**
  - Activate OP Holocene
  - Switch DA to snap batching and optimize decoding speed
  - Add proper versioned identities to EL nodes
- **Action Items:**
  - Bump `rise-sequencer`, `rise-node`, and `rise-optimism` services with new images

---

### Upgrade #10: Several Quality-of-Life Improvements

- **Date:** 2025-05-20
- **Description:**
  - Subscribe to shred-enabled logs with `rise_subscribe`
  - Order transactions by gas price; avoid `re-executing` failed transactions in the same block
  - Increase contract size limit to 256 KB
  - Reduce nonce gaps and pending transactions
  - More RPC and mempool consistency
- **Action Items:**
  - Bump `rise-sequencer`, `rise-node`, and `rise-optimism` services with new images

---

### Upgrade #9: Ship `eth_sendRawTransactionSync`

- **Date:** 2025-04-28
- **Description:**
  - Ship `eth_sendRawTransactionSync` for much improved latency
  - Merge `--rollup.sequencer-http` and `RISE_SEQUENCER_WS` into `--rollup.sequencer-ws`
  - Reduce gas limit from `0xffffffffffffffff` to `0x7fffffffffffffff`
- **Action Items:**
  - Bump `rise-sequencer` and `rise-node` services with new images

---

### Upgrade #8: Fix Pending Block Hash

- **Date:** 2025-04-14
- **Description:**
  - Fix invalid state transition when reading the pending block hash during EVM pre-execution
- **Action Items:**
  - Bump `rise-sequencer` and `rise-node` services with new images

---

### Upgrade #7: More RPC Updates

- **Date:** 2025-04-10
- **Description:**
  - Faster pending `eth_callMany`
  - Improve RPC compatibility with popular tools like Foundry
  - Introduce `RISE_SEQUENCER_WS` for full nodes to subscribe to shreds via `rise_subscribe` and serve fast pending data
- **Action Items:**
  - Bump `rise-sequencer` and `rise-node` services with new images

---

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
