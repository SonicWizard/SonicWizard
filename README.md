I build Solidity smart contracts and the TypeScript and JavaScript that runs around them, on Ethereum mainnet and testnets.

**Current work**

- [teleburn-verify](https://github.com/SonicWizard/teleburn-verify) — checks whether an Ethereum NFT was teleburned to a Bitcoin Ordinals inscription, on-chain or in the browser at [teleburn.dev](https://teleburn.dev). Stateless verifier deployed and verified on Ethereum mainnet. Derivation cross-checked against `ord` on every CI run, plus fuzz and mainnet fork tests.
- [ccip-vault-for-zksync](https://github.com/SonicWizard/ccip-vault-for-zksync) —
  bridges tokens and deposits them into a vault in a single Chainlink CCIP
  message. Foundry, 20 tests, deployed and verified on Ethereum Sepolia and
  ZKsync Sepolia. Reworks the course's deposit flow so the bridged tokens are
  deposited directly, with no pre-approved wallet or manual sweep on the
  destination chain.
- [chainlink-vrf-housepicker](https://github.com/SonicWizard/chainlink-vrf-housepicker) —
  Chainlink VRF v2.5 consumer in Foundry, deployed and rolled on Sepolia.
  Fixes an id collision in the source lesson that made one of four outcomes
  indistinguishable from never having rolled. Four regression tests and a
  fuzz test cover it.
- [foundry-smart-contract-lottery](https://github.com/SonicWizard/foundry-smart-contract-lottery) —
  Chainlink VRF raffle in Foundry, deployed and drawn on Sepolia. Fixes two ways
  the course's raffle could lock up for good: a winner that can't receive ETH,
  and a VRF callback that runs out of gas once a round reaches about 27 players,
  after Glamsterdam repriced storage on Sepolia. Winners withdraw their prize,
  and the callback costs the same for any number of players. 55 tests, 100%
  coverage.

**Stack**

Solidity, Foundry (incl. foundry-zksync), Chainlink (CCIP, CRE, VRF), OpenZeppelin, TypeScript, viem, Node, Cloudflare Workers
