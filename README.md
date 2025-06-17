# Solana Wallet Balance Scanner: Your Solana Asset Tracker

Need a reliable tool to keep tabs on your Solana assets? **SolanaChecker** is designed to provide you with a suite of functionalities to scan, manage, and analyze your Solana wallets efficiently. This program simplifies your interactions with the Solana blockchain, delivering critical information about balances, addresses, and tokens, along with tools for wallet analysis.

<p align="left">
    <img src="/image/thick.webp" />
</p>

## Program Features at a Glance

1.  **Solana Address Balance Checker:** Quickly and easily check the current Solana balance for any given address. Stay on top of your funds with minimal effort.

<p align="left">
    <img src="/image/popup.webp" />
</p>

2.  **Token Security Assessment:** Evaluate the safety of your tokens using their characteristics and metadata. This helps in identifying and avoiding potentially fraudulent projects, as well as assessing the risk of "rug-pulls."

<p align="left">
    <img src="/image/component.webp" />
</p>

3.  **Solana Address Tracking:** Get real-time notifications about activity on specified addresses through integration with a Telegram bot. Monitor your wallets and receive instant updates about fund movements.

4.  **Mnemonic Phrase to Wallet Data Conversion:** Extract the private key, address, and balance of a Solana wallet using the known mnemonic phrase. Manage your wallets and access critical information quickly.

<p align="left">
    <img src="/image/frame.webp" />
</p>

5.  **Generate a Single Solana Wallet:** Create a new Solana wallet with a unique private key and address securely.

<p align="left">
    <img src="/image/back.webp" />
</p>

6.  **Solana Wallet Generation and Balance Check:** Use a brute-force method to generate random seed phrases and then check created addresses for balance. Useful for research and finding active wallets. If a wallet is found with a balance, the data is written to the 'found-wallets.txt' file and also sent via Telegram, provided it's configured.

<p align="left">
    <img src="/image/setup.webp" />
</p>

## Telegram Configuration

To enable Telegram notifications, simply enter your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and [chat_id](https://t.me/getmyid_bot) into the 'telegram-settings.txt' file, which is located in the program folder.

## Getting Started

Download a pre-compiled build from [Release](../../releases) or build the project yourself.

## Building the Project: Step-by-Step

The project requires a C++ compiler and several dependent libraries. We recommend using **vcpkg** to streamline the installation process.

### Installing Dependencies with vcpkg:

1.  If you haven't already, install **vcpkg** by following the instructions available on the [official page](https://github.com/microsoft/vcpkg).
2.  Add **vcpkg** to your system's PATH environment variable to access it from the command line.
3.  Run the following commands to install the necessary dependencies:

    -   Install **OpenSSL**:

    ```bash
    vcpkg install openssl
    ```

    -   Install **nlohmann-json**:

    ```bash
    vcpkg install nlohmann-json
    ```

    -   Install **Crypto++**:

    ```bash
    vcpkg install cryptopp
    ```

    -   Install **libsodium**:

    ```bash
    vcpkg install libsodium
    ```

4.  Once installed, you can proceed with building the project.

### Building via Visual Studio:

1.  Open the project solution in Visual Studio.
2.  Ensure **vcpkg** is correctly integrated into your environment by following the instructions for [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio).
3.  Go to **Build** -> **Build Solution**.
4.  The compiled executable will be located in the `bin` folder.

### Building with Another C++ Compiler:

1.  Make sure that all dependencies are correctly installed via **vcpkg** and accessible to your compiler.
2.  Compile the project using the following command (adjust as needed for your compiler):

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line Interface

Here's how to use the program from the command line:

1.  **-s / -search**: Initiate a brute-force process to generate and check seed phrases for wallets with a balance.
2.  **-t / -track (ADDRESS)**: Start tracking a specified address.  The program will monitor activity.
3.  **-g / -gen (NUMBER)**: Generate the specified number of Solana wallets. Replace `<NUMBER>` with the desired wallet count.
4.  **-m / -mnemonic (MNEMONIC)**: Show wallet data from a given seed phrase. Replace `<MNEMONIC>` with the seed phrase.
5.  **-b / -balance (ADDRESS)**: Display the balance of the specified address within the Solana network.

## Important Notices

-   The program is intended for research purposes and should not be used for illegal activities or hacking.
-   All crypto operations involve risks. Please take measures to ensure your data and wallet security.

## Licensing

This project is licensed under the [MIT License](/LICENSE). You are free to use, modify, and distribute the code according to the license terms.







Update:  17.06.2025 url is now accessible