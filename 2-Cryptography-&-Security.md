# Cryptography & Security in Blockchain

To become a **blockchain developer**, understanding cryptography and security is essential. Here’s a **brief explanation** of the key topics:

---

## 1️⃣ Hash Functions (SHA-256, Keccak-256)

**Hash functions** are cryptographic algorithms that take an input and generate a fixed-size output (hash). They are **irreversible** and play a crucial role in ensuring **data integrity** and **security** in blockchain.

### ✅ SHA-256 (Secure Hash Algorithm - 256 bit)
- Used in **Bitcoin** to hash transactions.
- Generates a **256-bit (64-character)** unique output.
- Even a small change in input produces a completely different hash (Avalanche Effect).

### ✅ Keccak-256
- Used in **Ethereum** for hashing.
- Similar to SHA-256 but follows a different cryptographic standard.
- Provides strong security and resistance to attacks.

### 💡 Why are Hash Functions important?
✔ Ensure immutability (once data is recorded, it cannot be changed).
✔ Used in **Merkle Trees** for verifying transactions efficiently.
✔ Prevents tampering and ensures **proof-of-work** in consensus mechanisms.

---

## 2️⃣ Public & Private Keys, Digital Signatures

Blockchain uses **public-key cryptography (PKC)** to secure transactions and ensure authenticity.

### 🔑 Public Key (Receiver’s Address):
- Used to receive funds.
- Derived from the **private key**.
- Can be shared publicly without security concerns.

### 🔐 Private Key (Secret Key):
- Used to **sign transactions** and prove ownership of assets.
- Must be kept **private**—losing it means losing access to funds.

### 🖊️ Digital Signatures:
- Uses a private key to generate a **unique cryptographic signature** for a transaction.
- Verifiable using the **public key**, ensuring the transaction was made by the rightful owner.

### 💡 Why are Public-Private Keys & Digital Signatures Important?
✔ **Prevents fraud** and ensures **ownership**.
✔ Guarantees **non-repudiation** (sender cannot deny making the transaction).
✔ Essential for **wallets, transactions, and smart contracts**.

---

## 3️⃣ Wallets & Transactions

A **blockchain wallet** is a tool for managing cryptocurrency **private keys** and interacting with the blockchain.

### 🔹 Types of Wallets:
- **Hot Wallets** (Online, connected to the internet) – e.g., MetaMask, Trust Wallet.
- **Cold Wallets** (Offline, more secure) – e.g., Ledger, Trezor.

### 🔹 How Transactions Work:
1. A user **creates a transaction** and signs it using their **private key**.
2. The transaction is broadcasted to the blockchain network.
3. **Miners/Validators** verify it and add it to the blockchain.
4. Once confirmed, the transaction becomes **permanent** and **immutable**.

### 💡 Security Considerations for Wallets & Transactions:
✔ Always keep your **private key secure** and never share it.
✔ Use **multi-signature wallets** for extra security.
✔ Be cautious of **phishing attacks** and **fake wallet apps**.

---

## 4️⃣ Smart Contract Security

Smart contracts are self-executing programs on the blockchain. However, poorly written contracts can be vulnerable to attacks.

### 📌 Common Smart Contract Vulnerabilities:

### 🔹 Reentrancy Attack:
- A malicious contract repeatedly calls the vulnerable contract before the initial execution is completed.
- Example: **The DAO Hack (Ethereum, 2016) – $60M lost**.
- 🔒 **Prevention:** Use **checks-effects-interactions pattern** and **reentrancy guards**.

### 🔹 Front-Running:
- Attackers exploit **pending transactions** in the **mempool** by submitting higher gas fees.
- Common in **DEX trading (e.g., Uniswap)**.
- 🔒 **Prevention:** Use **commit-reveal schemes**, **batch processing**, or **private mempools**.

### 🔹 Integer Overflow & Underflow:
- Happens when a number exceeds the storage limit, causing unexpected behavior.
- 🔒 **Prevention:** Use **SafeMath libraries** (now built into Solidity 0.8+).

### 💡 Best Practices for Smart Contract Security:
✔ Use **Solidity 0.8+** (built-in overflow protection).
✔ Implement **access control** (e.g., OpenZeppelin’s Ownable).
✔ Regularly conduct **security audits** and use tools like **Slither, MythX, and OpenZeppelin Defender**.
✔ Follow the **principle of least privilege** (limit contract permissions).
