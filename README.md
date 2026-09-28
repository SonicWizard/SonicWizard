I build Solidity smart contracts with Foundry and Chainlink. Current projects are deployed on Ethereum Sepolia and ZKsync Sepolia.

**Current work**

- [ccip-vault-for-zksync](https://github.com/SonicWizard/ccip-vault-for-zksync) —
  bridges tokens and deposits them into a vault in a single Chainlink CCIP
  message. Foundry, 20 tests, deployed and verified on Ethereum Sepolia and
  ZKsync Sepolia. Reworks the course's deposit flow so the bridged tokens are
  deposited directly, with no pre-approved wallet or manual sweep on the
  destination chain.
- [chainlink-functions-to-cre](https://github.com/SonicWizard/chainlink-functions-to-cre) —
  migrating a Chainlink Functions consumer to CRE after the June 2026 sunset.
  Solidity and TypeScript, 24 tests, both contracts deployed on Sepolia.
- [chainlink-vrf-housepicker](https://github.com/SonicWizard/chainlink-vrf-housepicker) —
  Chainlink VRF v2.5 consumer in Foundry, deployed and rolled on Sepolia.
  Fixes an id collision in the source lesson that made one of four outcomes
  indistinguishable from never having rolled. Four regression tests and a
  fuzz test cover it.

**Stack**

Solidity, Foundry, Chainlink (CCIP, CRE, VRF, Data Feeds), TypeScript, Angular, Node.
