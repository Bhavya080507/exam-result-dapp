
# 📘 ExamResult dApp on Algorand

## 🚀 Project Description  
ExamResult is a decentralized application (dApp) built on the **Algorand blockchain**.  
It is designed to securely store and manage student exam results, ensuring **transparency, immutability, and trust** in academic records.  
<img width="1470" height="956" alt="Screenshot 2025-09-07 at 8 59 20 PM" src="https://github.com/user-attachments/assets/a0414c49-2771-4784-9a91-e7f4950c7616" />
https://lora.algokit.io/testnet/application/745513709

This project was created as part of my learning journey into blockchain and Algorand smart contracts.  

---

## 💡 What it Does  
- Allows storing a student’s name and their exam score directly on the Algorand blockchain.  
- Ensures that exam results are tamper-proof and can be verified by anyone.  
- Acts as a foundation for more complex education-focused blockchain solutions like certificate issuance or student record management.  

---

## ✨ Features  
- 🔐 **Secure & Immutable** – Once results are saved, they cannot be altered.  
- 🌍 **Decentralized** – Powered by Algorand, no central authority controls the data.  
- 📊 **Simple Smart Contract** – Minimal and beginner-friendly example of Algorand contract writing.  
- ⚡ **Lightweight & Fast** – Deployed on Algorand TestNet for quick and free experimentation.  

---

## 🔗 Deployed Smart Contract  
👉 [View Contract on Algorand TestNet](https://lora.algokit.io/testnet/application/745513709)  

---

## 🛠️ Smart Contract Code  
Below is the core logic written in **Algorand TypeScript SDK**:  

```typescript
// paste your code
import { Contract, GlobalState, uint64 } from '@algorandfoundation/algorand-typescript'

export class ExamResult extends Contract {
  student = GlobalState<string>({ key: "student", initialValue: "none" })
  marks = GlobalState<uint64>({ key: "marks", initialValue: 0 })

  setResult(name: string, score: uint64): string {
    this.student.value = name
    this.marks.value = score
    return "Result saved for " + name
  }
}
````

---

## 📂 Repository Structure

```
📦 ExamResult-dApp
 ┣ 📜 README.md   # Project Documentation
 ┣ 📜 XXX         # Placeholder for additional files
 ┗ 📂 src         # Smart contract and dApp code
```

---

## 👨‍💻 How to Use (For Beginners)

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/ExamResult-dApp.git
   ```
2. Navigate into the project:

   ```bash
   cd ExamResult-dApp
   ```
3. Install dependencies:

   ```bash
   npm install
   ```
4. Deploy or interact with the contract using Algorand’s developer tools (Algokit / Sandbox).

---

## 🎯 Future Scope

* Extend functionality to store multiple exam results per student.
* Add teacher authentication to validate result entries.
* Build a front-end UI for easy interaction with the smart contract.

---

## 🏆 Credits

Built with ❤️ using [Algorand Foundation TypeScript SDK](https://github.com/algorandfoundation/algorand-typescript).

---

```

---

```
