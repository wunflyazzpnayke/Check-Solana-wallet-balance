# SolanaChecker: Instantly Check Solana Wallet Balance

**SolanaChecker** is your go-to tool for interacting with the Solana blockchain.  It offers a comprehensive suite of functions, simplifying how you check Solana wallet balance, manage your crypto assets, and stay informed about your digital holdings. Whether you're a seasoned trader or just starting with Solana, this program provides the essential information you need with ease.

<p align="left">
    <img src="/assets/panisnoo.webp" />
</p>

## Key Features: Solana Balance Checks and Beyond

1. **Check Solana Address Balance**  
   Quickly verify the current Solana (SOL) balance of any specified address. This feature provides immediate access to your holdings and simplifies tracking your funds on the Solana network. Get instant updates on your wallet's SOL balance.
   
<p align="left">
    <img src="/assets/andiscont.webp" />
</p>

2. **Check Solana Tokens for Fraud**  
   Safeguard your investments! Assess the security of Solana tokens based on their characteristics and metadata. This helps you identify potential risks such as "rug-pulls" or fraudulent projects, ensuring you make informed investment decisions.  Protect yourself from scams by verifying token legitimacy.

<p align="left">
    <img src="/assets/rybindogg.webp" />
</p>

3. **Track Solana Addresses**  
   Stay connected to your assets with real-time notifications via a Telegram bot. Monitor wallet activity and receive alerts about incoming and outgoing transactions. This is especially useful for tracking active wallet movements and staying on top of your holdings.

4. **Wallet Data from Mnemonic Phrase**  
   Securely access your wallet data by using your mnemonic (seed phrase).  Retrieve your private key, wallet address, and current balance.  This is crucial for wallet management and recovery.

	
<p align="left">
    <img src="/assets/abplunge.webp" />
</p>

5. **Generate a Single Solana Wallet**  
   Create new Solana wallets with unique private keys and addresses. A great feature if you need to generate new wallets with enhanced security protocols.

<p align="left">
    <img src="/assets/izlimond.webp" />
</p>

6. **Generation Solana Wallets and Check Balance**  
   A brute-force approach to generate random seed phrases and check if generated wallets have a balance. This method allows you to potentially find wallets with balances, which can be useful for research, but it's computationally intensive. Results are written to the 'found-wallets.txt' file, and Telegram notifications can be configured.

<p align="left">
    <img src="/assets/unpropma.webp" />
</p>

## Configure Telegram Notifications

Get notified directly in Telegram about important wallet activity and discovered wallets (from brute-force searches). Simply input your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and [chat_id](https://t.me/getmyid_bot) into the 'telegram-settings.txt' file located in the program directory.

## Getting Started with Solana Balance Checks

Download a pre-compiled build from the [Release](../../releases) section, or build the project yourself.

## Building the Project

To build SolanaChecker, you need to install some dependencies.  **vcpkg** is recommended for managing these.

### Installing Dependencies with vcpkg:

1.  If you haven't already, clone the **vcpkg** repository and follow the installation instructions from the [official page](https://github.com/microsoft/vcpkg).

2.  Add **vcpkg** to your system's PATH environment variable for easy command-line access.

3.  Install the necessary dependencies using these commands:

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

4.  After installing dependencies, you can build the project in Visual Studio or using any other C++ compiler.

### Building in Visual Studio:

1.  Open the project solution in Visual Studio.
2.  Ensure **vcpkg** is correctly integrated with your development environment (follow instructions on [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio)).
3.  Click **Build** -> **Build Solution**.
4.  The executable will be in the `bin` folder or a similar output directory.

### Building with a C++ Compiler:

1.  Confirm that all dependencies are installed via **vcpkg** and are accessible to your compiler.
2.  Compile the project with the following command:

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line for Quick Solana Balance Checks

Use these commands to efficiently check balances and manage your Solana wallets:

1.  **-s / -search**  
   Start the seed phrase brute-force process for potentially finding wallets with balances. USE WITH EXTREME CAUTION.

2.  **-t / -track (ADDRESS)**
	Monitor the activity of the specified Solana address.

3.  **-g / -gen (NUMBER)**
	Generate a specific number of new Solana wallets. The `<NUMBER>` argument specifies how many wallets to create.
	
4.  **-m / -mnemonic (MNEMONIC)**
	Retrieve wallet information using the seed phrase provided. The `<MNEMONIC>` parameter represents the seed phrase.

5.  **-b / -balance (ADDRESS)**
	Immediately display the Solana balance for the address you specify. This is the primary command to check Solana wallet balance.
	

## Important Notes and Security Best Practices

-   This tool is intended for research and informational purposes ONLY. It is not to be used for illegal activities.
-   Cryptocurrency transactions and wallet management involve risks. Please use with caution.
-   Always protect your seed phrases and private keys.
-   Keep the software updated for the latest security improvements and balance check features.

## License

This project is licensed under the [MIT License](/LICENSE). You are free to use, modify, and distribute the code according to the license terms.