# n8n-stock-portfolio-chat-agent
AI chat agent built with n8n that tracks my stock portfolio using Marketstack and Google Sheets
# Stock Portfolio Chat Agent (n8n)

I built this small project in n8n to keep track of my stock portfolio by just chatting with it. It reads my holdings from a Google Sheet, gets the latest prices from Marketstack, and can add new trades to the sheet when I ask.

## What it can do

- Show the stocks I own and how many shares I have
- Get the latest end-of-day price for any ticker
- Work out the total value of my portfolio
- Add a new trade to the sheet, for example "add 10 shares of AAPL"
- Remember what we talked about earlier in the same chat

## How it's built

- Chat Trigger to start the workflow when I send a message
- AI Agent with an OpenAI chat model to understand the request
- Simple Memory so it can handle follow-up questions
- Marketstack node to fetch stock prices
- Two Google Sheets nodes, one to read the portfolio and one to add new rows


## What you need

- An n8n account (cloud or self-hosted)
- An OpenAI API key, or n8n AI credits
- A Marketstack API key. The free plan works, just turn off "Use HTTPS" in the credential
- A Google account for Google Sheets

## How to set it up

1. Download the `Stock Portfolio Chat Agent.json` file from this repo.
2. In n8n, go to Workflows, choose Import from File, and select the file.
3. Make a Google Sheet with two columns in the first row: `Ticker` and `shares`. Add a few stocks, like:

   | Ticker | shares |
   |--------|--------|
   | AAPL   | 10     |
   | MSFT   | 5      |
4. Add your own credentials for OpenAI, Marketstack and Google Sheets.
5. In both Google Sheets nodes, pick your sheet.
6. Open the chat and try it out.

## Things you can ask

- What stocks do I own?
- What's the latest price of TSLA?
- How much is my portfolio worth today?
- Add 15 shares of NVDA

## A note on keys

There are no API keys in this file. n8n keeps credentials separately, so if you import it you'll need to connect your own accounts.

---

Made by AHAD38. Feel free to use it or change it however you like.
