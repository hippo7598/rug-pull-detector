> [!TIP] 
> # How to run
> 
> ## Install Python
> 
> 1. Go to the official Python website: https://www.python.org/downloads/release/python-3139/
> 2. Scroll down to the files part. Then download the Windows installer (64-bit)
> 3. Once downloaded, run the installer.
> 4. ✅ Important: On the first screen of the installer, check the box that says
> “Add Python to PATH” before clicking Install Now.
> ## How to download the repo
> Click the button below to download the code as a .zip:
>
> <a href="https://github.com/hippo7598/rug-pull-detector/archive/refs/heads/main.zip"><img src="https://img.shields.io/badge/⬇️_Download_ZIP-2ea44f?style=for-the-badge&logo=github&logoColor=white" alt="Download ZIP"></a>
>
> 
> Now extract the .zip folder
> 
> ## Run the script
> 
> Open the command prompt inside the extracted folder and run:
>
> `py defi_rug_pull_detector.py`
> 
>  or
> 
> `python defi_rug_pull_detector.py`


### README

---

# DeFi Rug Pull Detector

## Overview

The **DeFi Rug Pull Detector** is a Python tool designed to help users analyze Ethereum-based tokens for common red flags associated with rug pulls. The tool examines key characteristics of a token’s contract and ownership structure, providing indicators that can signal potential risks. This is a preliminary analysis tool and should be used in conjunction with thorough research.

### Features

- **Liquidity Lock Check**: Verifies whether the liquidity for the token is locked. (Requires manual verification or third-party services.)
- **Holders Concentration**: Identifies the top token holders to assess whether a small number of wallets hold a large percentage of the supply.
- **Minting and Burning Rights**: Analyzes the contract source code to see if the owner has the ability to mint or burn tokens, which could be exploited.
- **Contract Source Verification**: Checks if the contract source code is publicly verified on Etherscan, adding transparency.

### Prerequisites

To use this script, you’ll need:

1. Python 3.x
2. Required libraries: `requests`, `logging`, and `json` (standard libraries)

Install `requests` if you haven't already:

```bash
pip install requests
```

3. An [Etherscan API key](https://etherscan.io/apis) to access token and contract information.

### Usage

#### Step 1: Set Up Etherscan API Key

Replace `etherscan_api_key` with your actual Etherscan API key.

#### Step 2: Run the Script

Replace `contract_address` with the address of the token you want to analyze, then run the script:

```bash
py defi_rug_pull_detector.py
```

The script will analyze the specified token and print out a summary of findings.

### Important Notes

- **Liquidity Lock**: The script provides a placeholder for liquidity lock checking, as this typically requires integration with third-party platforms like Unicrypt or Team Finance.
- **Manual Verification Recommended**: This tool provides preliminary analysis; always conduct thorough due diligence.
- **Limitations**: Some aspects, like liquidity locking, require external verification tools.

### Example Output

The final output will provide a summary in JSON format, including:

- Basic Token Information
- Liquidity Lock Status
- Top Holders (up to 5)
- Minting Rights Status

### Future Enhancements

- **Multi-Chain Support**: Extend support for other chains by integrating APIs for networks like BSC or Polygon.
- **Automated Liquidity Checks**: Integrate with Unicrypt or similar services for automatic liquidity lock verification.
- **Comprehensive Report Generation**: Generate a downloadable PDF report summarizing the analysis for record-keeping and sharing.

---

This tool offers a simple way to conduct an initial risk assessment of DeFi tokens. Let me know if you need additional help or if you'd like to add more functionalities!
b