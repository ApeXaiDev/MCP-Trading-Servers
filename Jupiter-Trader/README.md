# ApeXai Jupiter Trader Server

This ApeXai server executes token swaps on the Solana blockchain using Jupiter's Ultra API.

## Purpose

The purpose of this ApeXai server is to provide a simple and easily accessible way for AI agents and decentralized applications to execute token swaps on the Solana blockchain using Jupiter's Ultra API. It can support automated trading strategies, portfolio rebalancing, and other DeFi use cases on Solana.

## Usage

To use this ApeXai server, follow these steps:

### 1. Install Python 3.7+

### 2. Install FastAPI and Uvicorn

```bash
pip install fastapi uvicorn
```
## 3. Run the server using Uvicorn
```bash
uvicorn apexai_jupiter_trader:app --host 0.0.0.0 --port 8007
```
## 4. Make a Request
Send a GET request to the /mcp/trade/jupiter endpoint with the following query parameters:

token_in: The address of the input token on Solana.

token_out: The address of the output token on Solana.

amount_in: The amount of the input token to swap.

slippage (optional): The maximum slippage allowed for the swap (e.g., 0.005 for 0.5%). Defaults to 0.005.

Example Request:
```bash
http://localhost:8007/mcp/trade/jupiter?token_in=So1111111111111111111111111111111111111112&token_out=EPjFWdd5AufqALUs2vEqk29iUMjYPN26sESpYRjhSyG&amount_in=1.0&slippage=0.01
```
The server will return a JSON response containing the details of the swap, including the input and output tokens, amounts, slippage, fee amount, and success status.

## $APEXAI Integration
This server can be integrated into the ApeXai ecosystem in several ways:

Marketplace Listing: List the server on the ApeXai marketplace so developers can access it using the $APEXAI token, either freely or through rental.

Transaction Fee Payments: Configure the server to use $APEXAI tokens for covering Solana transaction fees, offering discounts to $APEXAI holders.

Priority Routing via Staking: Users who stake $APEXAI tokens can receive priority routing for their swaps, allowing faster and more efficient trade execution.
