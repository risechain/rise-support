# RISE Public Testnet Changelog

### Upgrade #4: Bump rise-sequencer, rise-optimism, and Deploy RISE Replicas

- **Date:** 2025-03-18
- **Description:**
  - Bump rise-sequencer to fix a race condition that led to wrong execution; and improve performance.
  - Replace op-reth with RISE's own replica rise-node for much better latency.
  - Rebase rise-optimism on op-node v1.2.0 for Pectra stability and improve performance.

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