# Optimism Token (OPT)

A minimal ERC20-like token deployable on [Optimism](https://www.optimism.io/) using [Remix IDE](https://remix.ethereum.org/).  
No external libraries (like OpenZeppelin) for easier verification on Optimism Explorer.

---

## 🚀 Deployment Steps
1. Open [Remix IDE](https://remix.ethereum.org/).
2. Create a new file `OptimismToken.sol` and paste the contract code.
3. Set compiler version to `0.8.20` (enable optimization recommended).
4. In Remix, go to **Deploy & Run** tab:
   - Environment → `Injected Provider - MetaMask`
   - Network → Switch to **Optimism Mainnet** or **Optimism Sepolia (testnet)**.
5. Deploy with constructor parameter `_initialSupply` (e.g., `1000000`).

---

## 🛠️ Usage
- `transfer(address to, uint256 value)` → Send tokens.
- `approve(address spender, uint256 value)` → Allow another address to spend tokens.
- `transferFrom(address from, address to, uint256 value)` → Spender moves tokens.

---

## ✅ Example
1. Deploy with `_initialSupply = 1000000` → Total supply = 1,000,000 OPT.
2. Owner wallet receives full supply.
3. Transfer to another wallet:  
   `transfer("0xRecipientAddress", 1000 * 10^18)`

---

## 📌 Notes
- This is a **minimal ERC20** (no burn/mint functions).
- For production, use OpenZeppelin ERC20 standard.
- Works on **Optimism mainnet & testnet**.


