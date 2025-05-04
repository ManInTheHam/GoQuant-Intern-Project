# GoQuant-Intern-Project


#  Deribit API Price Fetcher (C++)

This project demonstrates how to connect to the [Deribit cryptocurrency exchange API](https://docs.deribit.com/) using **C++** and **libcurl**, to fetch the latest index prices for major cryptocurrencies like BTC and ETH.

---

## Features

- Fetches real-time index price from Deribit.
- Uses `libcurl` for HTTP requests.
- Clean and extensible structure.
- Command-line interface for symbol input.

---

## Requirements

- C++ Compiler (e.g., `g++`)
- libcurl development package

Install libcurl on Debian-based systems:

sudo apt update
sudo apt install libcurl4-openssl-dev


# How to Build
1. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/yourusername/your-repo-name.git
    cd your-repo-name
    ```

# How to Run
Once compiled, run the executable:
./deribit
You'll be prompted to enter a crypto symbol like BTC, ETH, or XRP. The program will then fetch and display the real-time index price from Deribit.


# Code Overview
fetch_from_api(): Handles the GET request to the Deribit endpoint using libcurl.

WriteCallback(): Used by libcurl to store the server's response in a string.

main(): Takes user input, builds the API URL, and prints the result.

📂 File Structure
.
├── deribit.cpp      # Main C++ source file

├── README.md        # Project documentation


# Example Output:
Enter the cryptocurrency symbol (e.g., BTC, ETH): BTC

API Response:
{
  "jsonrpc": "2.0",
  "result": 29673.34,
  "usIn": 1688321971000123,
  "usOut": 1688321971000345,
  "usDiff": 222,
  "testnet": false
}

🙋‍♂️ Author
Created by ManInTheHam.
Feel free to connect on LinkedIn or GitHub!

