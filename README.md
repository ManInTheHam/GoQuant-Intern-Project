# 📈 Deribit API Trading System in C++

A C++ trading system that interacts with the [Deribit Test API](https://test.deribit.com/).  
It enables you to place, cancel, and modify orders, view the order book, and check position details.

---

## 🚀 Features

- **Order Placement**: Submit buy/sell orders with specified price and quantity.
- **Order Management**: Cancel or modify existing orders.
- **Order Book Retrieval**: Fetch real-time bids, asks, and other market data.
- **Position Info**: View your open positions for a specific instrument.

---

## 🧠 Code Description

The core logic is implemented through the following functions:

1. **`WriteCallback`**  
   Handles response data from the Deribit API. cURL calls this function to append incoming data to a string.

2. **`sendRequest`**  
   Sends HTTP POST requests to the Deribit API, setting up the URL, payload, and authorization headers.

3. **`getAccessToken`**  
   Retrieves an access token using your client ID and secret. Required for private API calls.

4. **`placeOrder`**  
   Places a buy order by specifying the instrument, price, and amount.

5. **`cancelOrder`**  
   Cancels an existing order based on its order ID.

6. **`modifyOrder`**  
   Modifies an already placed order.

7. **`getOrderBook`**  
   Retrieves the order book for a specified instrument, printing bid/ask prices and quantities.

8. **`getPosition`**  
   Retrieves the current position for an instrument with details like liquidation price, size, and PnL.

9. **`getOpenOrders`**  
   Lists all open orders for your account.

10. **`main`**  
    Entry point of the program. Authenticates the user and displays a menu to interact with API functions.

---

## 🧰 Requirements

- C++11 or later compiler (e.g., GCC)
- cURL (HTTP client library)
- [nlohmann/json](https://github.com/nlohmann/json) (Modern C++ JSON parser)

---

## 📦 Dependencies

### 1. Install cURL

```bash
sudo apt update
sudo apt install libcurl4-openssl-dev

```

2. Install nlohmann/json
Via APT:

```bash
sudo apt install nlohmann-json3-dev
```
Or manually:
```bash
wget https://github.com/nlohmann/json/releases/latest/download/json.hpp
mkdir -p include/
mv json.hpp include/
```

## 🛠️ Setup
1. Clone the Repository
```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
```
2. Install Required Libraries
Make sure libcurl and nlohmann/json are installed on your system.

3. (Optional) Add JSON Header
If installing manually, place json.hpp inside an include/ directory:

```bash
mkdir include
mv path/to/json.hpp include/
```

## 🧪 Compilation
To compile the system:

```bash
g++ main.cpp -o trading_system -lcurl -I include
```
If using apt to install nlohmann-json3-dev, the -I include is optional.

## ▶️ Usage
Run the compiled executable:

```bash
./trading_system
```
The program will display a menu of options.

Enter the number corresponding to the desired action (e.g., place order, get order book, etc.).

Follow prompts to provide input like:
Instrument name (e.g., BTC-PERPETUAL)
Order ID
Price
Amount

## ⚠️ Important Considerations
API Credentials
Update the main function with your own Deribit client ID and secret.
Tip: Use environment variables or a .env config file instead of hardcoding them.

Error Handling
Basic cURL error checks are included, but you should add robust error handling for:
-API response parsing
-Invalid input
-Failed requests
-Rate Limiting
Be aware of Deribit’s API rate limits. Use sleep/delays or exponential backoff on HTTP 429 errors.

Test Environment
This code is designed for the Deribit Test API.
❗ Do not use with real funds.

## 🧪 Test Environment
1. OS: Ubuntu 22.04
2. Compiler: GCC 11.4
3. API: Deribit Testnet

## Author
Created by ManInTheHam
GitHub: @ManInTheHam
[X](https://x.com/ManInTheHam_)
[LinkedIn](https://www.linkedin.com/in/soham-joshi-54aa171aa/)


