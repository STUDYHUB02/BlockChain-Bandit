Blockchain Bandit
=================

An educational project demonstrating the process of generating Ethereum private keys, deriving public keys, and computing Ethereum addresses using Python. This project uses libraries such as `eth-keys`, `eth-hash`, and `ecdsa` for cryptographic operations and includes functionality to generate multiple addresses in parallel with threading. It also features a method to check the balance of generated addresses by scraping Etherscan.

Description
-----------
This project demonstrates the following:

* **Ethereum Key Generation:** Generate Ethereum private keys and derive the corresponding public keys.
* **Address Derivation:** Compute Ethereum addresses from public keys.
* **Parallel Generation:** Generate multiple Ethereum addresses concurrently using Python's `ThreadPoolExecutor` for efficiency.
* **Balance Checking:** Check the balance of each generated address by scraping the Etherscan website.

The project serves as a practical tool to understand cryptographic principles and Ethereum address mechanics.

Prerequisites
-------------
Ensure you have the following installed:

* **Python 3.x**
* **Jupyter Notebook** (or any similar environment such as JupyterLab or Google Colab)

### Required Python Libraries
* `eth-keys`
* `eth-hash[pycryptodome]`
* `ecdsa`
* `requests`
* `beautifulsoup4`

Installation
------------
Install the necessary libraries using pip:

```bash
pip install eth-keys eth-hash[pycryptodome] ecdsa requests beautifulsoup4
```

Usage
------------
* **Generate a Single Ethereum Address**
The notebook begins by generating a single Ethereum private key, deriving its public key, and computing the corresponding Ethereum address. A custom private key ("2".zfill(64)) is used for demonstration purposes, though you can modify the code to generate random keys.

* **Generate Multiple Ethereum Addresses**
A function is provided to generate multiple addresses in parallel using the ThreadPoolExecutor from the concurrent.futures module. You can specify the number of addresses to generate when prompted.

* **Check Address Balance**
For each generated address, the notebook includes a method to:
Verify the existence of the address on Etherscan.
Display the balance of the address by scraping the Etherscan website.


Note
------------
Scraping Etherscan may not be the most efficient or reliable method for production use. For real-world applications, consider using the official Etherscan API or a blockchain interaction library such as web3.py.

Important Notes
------------
* **Security Warning**: The private keys generated in this notebook are for demonstration purposes only. Do not use them for actual Ethereum transactions or to store real funds. They are not generated in a secure environment.
* **Balance Check Limitation**: The balance check is performed by scraping the Etherscan website. Ensure you comply with Etherscan's terms of service, as excessive or unauthorized scraping may violate their policies.

Disclaimer
------------
This notebook is intended for educational purposes only. The private keys generated within it are not secure and should not be used for actual Ethereum transactions. For production use, always use secure methods to generate and store private keys, such as hardware wallets or cryptographically secure random number generators.

Conclusion
------------
Blockchain Bandit serves as an educational tool to illustrate the basics of Ethereum key generation, address derivation, and interaction with blockchain explorers like Etherscan. Use this project to gain hands-on experience with cryptographic operations and understand the mechanics behind Ethereum addresses.
