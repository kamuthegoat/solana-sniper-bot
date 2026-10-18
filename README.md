# Solana Raydium & Pump.fun Fast Token Sniper (Jito MEV Edition)

High-performance, low-latency token sniper built specifically for Solana memecoins on **Pump.fun** and **Raydium AMM V4**. 

Engineered to bypass mempool front-running and validator delays by routing transactions directly into **Jito Block Engine bundles** with dynamic priority tips.

---

## Key Architecture & Features

- **Direct Program Decoders:**
  - Pump.fun bonding curve program (`6EF8rrecthR5Dkzon8Nwu78hRvfCKubJ14M5uBEwF6P`)
  - Raydium AMM Liquidity Pool V4 (`675kPX9MHTjS2zt1qfr1NYHuzeLXfQM9H24wFSUt1Mp8`)
- **Jito MEV Bundles:** Direct bundle dispatch to Jito validators in Frankfurt, Amsterdam, New York, and Tokyo. Eliminates slippage failures and front-run attacks.
- **Micro-Lamport Compute Unit Optimization:** Automatically bids for compute units dynamically based on live block congestion.
- **Safety Filters:**
  - Mint authority verification
  - Freeze authority verification
  - Top 10 holders percentage cap
  - Minimum initial liquidity check
- **Automated Profit Taking & Stop Loss:** Real-time trailing profit taker and emergency stop-loss.

---

## Quickstart

### Prerequisites
- Python 3.10+ or Node.js v18+
- Solana RPC endpoint with WebSocket support (Helius, QuickNode, or Triton recommended)
- Funded Solana keypair

### Configuration
Edit `config.json`:
```json
{
  "rpc_url": "https://api.mainnet-beta.solana.com",
  "ws_url": "wss://api.mainnet-beta.solana.com",
  "private_key_base58": "YOUR_PRIVATE_KEY",
  "buy_amount_sol": 0.05,
  "slippage_pct": 15.0,
  "use_jito": true,
  "jito_tip_sol": 0.001,
  "take_profit_pct": 100.0,
  "stop_loss_pct": 30.0
}
```

### Running
```bash
python bot.py
```

---

## License & Commercial Turnkey Setup ($25 USD)

Want the turnkey binary bundle with multi-wallet volume pumping, multi-RPC fallback, and direct Discord/Telegram alert webhooks?

- **Price:** **$25 USD**
- **Instant Documentation & Setup:** [https://rentry.co/ons39mtf](https://rentry.co/ons39mtf)
- **Accepted Crypto:**
  - **SOL:** `3Uiis6Zv8fsxuvANCAvDPU5dGxrnjrGgg4HpN1Pz6HHn`
  - **BTC:** `bc1qm0kwx7ed4g5wzl3rzuu4wdh9lqf00knhs5r778`
  - **ETH:** `0xeC7056A6440F36b8616b4bF2B41501AaAd005c9D`

After transferring, open an issue with your transaction hash or check [https://rentry.co/ons39mtf](https://rentry.co/ons39mtf) for instant zip distribution and support.
