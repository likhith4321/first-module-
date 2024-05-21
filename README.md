# Functions in ERC20 and Vault Contracts

## ERC20 Contract

The ERC20 contract implements the standard ERC20 interface, which includes the following key functions:

### `totalSupply() -> uint256`
- **Description**: Returns the total number of tokens in existence.
- **Returns**: The total supply of the token.

### `balanceOf(address account) -> uint256`
- **Description**: Returns the token balance of the specified address.
- **Parameters**: 
  - `account`: The address to query the balance of.
- **Returns**: The balance of the specified address.

### `transfer(address recipient, uint256 amount) -> bool`
- **Description**: Transfers `amount` tokens to the `recipient` address.
- **Parameters**: 
  - `recipient`: The address to transfer tokens to.
  - `amount`: The number of tokens to transfer.
- **Returns**: A boolean indicating whether the operation succeeded.
- **Events**: Emits a `Transfer` event.

### `approve(address spender, uint256 amount) -> bool`
- **Description**: Sets `amount` as the allowance of `spender` over the caller's tokens.
- **Parameters**: 
  - `spender`: The address allowed to spend the tokens.
  - `amount`: The number of tokens `spender` is allowed to spend.
- **Returns**: A boolean indicating whether the operation succeeded.
- **Events**: Emits an `Approval` event.

### `allowance(address owner, address spender) -> uint256`
- **Description**: Returns the remaining number of tokens that `spender` is allowed to spend on behalf of `owner`.
- **Parameters**: 
  - `owner`: The address which owns the funds.
  - `spender`: The address which will spend the funds.
- **Returns**: The remaining allowance.

### `transferFrom(address sender, address recipient, uint256 amount) -> bool`
- **Description**: Transfers `amount` tokens from `sender` to `recipient` using the allowance mechanism.
- **Parameters**: 
  - `sender`: The address to transfer tokens from.
  - `recipient`: The address to transfer tokens to.
  - `amount`: The number of tokens to transfer.
- **Returns**: A boolean indicating whether the operation succeeded.
- **Events**: Emits a `Transfer` event.

## Vault Contract

The Vault contract manages deposits and withdrawals of the ERC20 token.

### `deposit(uint256 amount)`
- **Description**: Allows a user to deposit `amount` tokens into the vault.
- **Parameters**: 
  - `amount`: The number of tokens to deposit.
- **Effects**: Transfers tokens from the user's address to the vault's address.
- **Events**: Emits a `Deposit` event.

### `withdraw(uint256 amount)`
- **Description**: Allows a user to withdraw `amount` tokens from the vault.
- **Parameters**: 
  - `amount`: The number of tokens to withdraw.
- **Effects**: Transfers tokens from the vault's address to the user's address.
- **Events**: Emits a `Withdrawal` event.

### `balanceOf(address account) -> uint256`
- **Description**: Returns the token balance of the specified address within the vault.
- **Parameters**: 
  - `account`: The address to query the balance of.
- **Returns**: The balance of the specified address within the vault.

### `totalDeposits() -> uint256`
- **Description**: Returns the total amount of tokens deposited in the vault.
- **Returns**: The total deposits in the vault.
