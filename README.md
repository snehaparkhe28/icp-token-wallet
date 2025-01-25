# ICP Token Wallet

This is a Rust-based token wallet for the Internet Computer Protocol (ICP) blockchain. It allows users to send, receive, and display token balances.

## Features
- **Send Tokens**: Transfer tokens to another wallet.
- **Receive Tokens**: Receive tokens and update wallet balance.
- **Display Balance**: Fetch and display the current token balance.

## Directory Structure

icp-token-wallet/
├── src/
│   ├── lib.rs            # Main contract logic
│   ├── types.rs          # Token data types
│   ├── tests.rs          # Unit tests
│   └── utils.rs          # Helper functions
├── canisters/
│   ├── wallet.did        # Candid interface for wallet
│   ├── token.did         # Candid interface for IRCRC2
├── Cargo.toml            # Rust dependencies and project metadata
└── README.md             # Documentation


## Setup

### Prerequisites
- Rust environment
- DFINITY SDK
- Local ICP testnet

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/icp-token-wallet.git
   cd icp-token-wallet
   ```
2. Install dependencies:
   ```bash
   cargo build
   ```

3. Start the local testnet:
   ```bash
   dfx start --background
   ```

4. Deploy the wallet canister:
   ```bash
   dfx deploy wallet
   ```

5. Test the functionalities:
   ```bash
   dfx canister call wallet send_tokens '(principal, 50)'
   dfx canister call wallet get_balance '()'
   ```

## Testing
Run unit tests:
```bash
cargo test
```
