# Mine SolXen on Solana Devnet (python one-liner)

This is a one-liner **SolXen** Miner for Solana Devnet (only been tested on my Ubuntu machine). 

Feel free to test it on Mac or other platforms and submit the necessary fixes.


## Usage

Running it is as simple as executing this one-liner on your machine. Just don't forget to add your Ethereum address at the end of the command.

Note: You'll need to clone this repo and update the 'keypair_path' in solxen.py to reflect your computer's path, and then curl to your address in the command below.


```curl -s https://raw.githubusercontent.com/JozefJarosciak/SolXen-python/master/solxen.py | python3 - <YOUR_ETHEREUM_ADDRESS>```


## Video Demo:

https://www.youtube.com/watch?v=IourGFCEjKU

[<img src="https://i9.ytimg.com/vi_webp/IourGFCEjKU/mq3.webp?sqp=CODGwbEG-oaymwEmCMACELQB8quKqQMa8AEB-AH-CYAC0AWKAgwIABABGDggSyh_MA8=&rs=AOn4CLC7ldzT1SqwWbWMOhRF4JXC3vv97Q" width="50%">](https://youtu.be/IourGFCEjKU)

For mac users, Follow build below.

solXEN 420 miner v.1.1

This guide will install Rust and Solana, and create and fund wallets on Solana TESTnet/DEVnet. It will run a 420miner on top of a Solana to find 420 in hashes using the sha-3 script. Once 420 is found, a solXEN token is distributed to your wallet address. This miner creates a new wallet, you can’t important existing Solana accounts.

#### INSTALL ALL PACKAGES ####

# Update Homebrew (macOS package manager) and install necessary packages

brew update
brew upgrade
brew install nano python3 cmake gcc clang curl git

#Install pip (Python package manager)

curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3 get-pip.py
rm get-pip.py

#Install requests library using pip

pip install requests

#Install Rust using rustup (Rust version manager)

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y

#Add Cargo (Rust's package manager) binaries to the PATH

export PATH="$HOME/.cargo/bin:$PATH"

#Install Solana CLI using official installer

sh -c "$(curl -sSfL https://release.solana.com/stable/install)"
export PATH="/Users/DONB/.local/share/solana/install/active_release/bin:$PATH"


#Configure Solana CLI to use the Devnet

solana config set --url https://api.devnet.solana.com

#### RUN SCRIPT FOR MINING + GENERATE NEW WALLET ####

#Generate a new Solana wallet (ONLY ONE WALLET IS NEEDED)

solana-keygen new


#Fork, Edit, Pull and run the script for mining 

TO USE MAC YOU NEED TO EDIT THE KEY PAIR PATH. PLEASE FORK AND EDIT KEYPAIR PATH TO MATCH YOUR SYSTEM PATH. EDIT LINE 14 IN PYTHON SCRIPT)

curl -s https://raw.githubusercontent.com/BruhhBruhh/solXEN_PY4MAC/master/solxen.py | python3 - 0x8666DD0923415F580635c363Ad83bbEdc31E0db6
