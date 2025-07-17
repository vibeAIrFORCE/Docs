# 🚀 VIBE AI Backend - Complete Endpoints Reference

## 📊 Overview

The VIBE AI backend system provides **129 total endpoints** across multiple categories, making it one of the most comprehensive AI agent platforms in the Web3 space.

**Total Endpoint Count:**
- **Core API Endpoints:** 14
- **Agent Tool Endpoints:** 115
- **Grand Total:** 129 endpoints

---

## 🎯 Core API Endpoints (14 endpoints)

### Agent Management API (`/agent`, `/thread`)

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/agent/initiate` | Initiate new agent session with optional file uploads |
| `POST` | `/thread/{thread_id}/agent/start` | Start agent for specific thread |
| `POST` | `/agent-run/{agent_run_id}/stop` | Stop running agent |
| `GET` | `/thread/{thread_id}/agent-runs` | Get all agent runs for thread |
| `GET` | `/agent-run/{agent_run_id}` | Get agent run details |
| `GET` | `/agent-run/{agent_run_id}/stream` | Stream agent responses in real-time |

### MCP (Model Context Protocol) API (`/mcp`)

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/mcp/servers` | List all configured MCP servers |
| `POST` | `/mcp/servers` | Add new MCP server |
| `DELETE` | `/mcp/servers/{server_id}` | Remove MCP server |
| `GET` | `/mcp/tools` | List available tools from MCP servers |
| `POST` | `/mcp/discover` | Trigger tool discovery on MCP servers |
| `POST` | `/mcp/execute` | Execute tool on MCP server |
| `GET` | `/mcp/health` | Check MCP service health |

### System API

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/health` | System health check |

---

## 🛠️ Agent Tool Endpoints (115 endpoints)

### 1. Data Provider Tools (88 endpoints)

Access through `execute_data_provider_call` tool across 11 providers:

#### Nansen API (19 endpoints)
Premium on-chain intelligence and Smart Money tracking

**Smart Money API (5 credits each):**
- `smart_money_inflows` - Net flow of tokens by Smart Money addresses
- `smart_money_holdings` - Current holdings of Smart Money addresses
- `smart_money_dex_trades` - DEX trades by Smart Money in last 24h
- `smart_money_dcas` - Jupiter DCA orders by Smart Money addresses

**Profiler API (0-5 credits):**
- `profiler_address_balances` - Current token balances (0 credits)
- `profiler_address_transactions` - Transaction history (0 credits)
- `profiler_address_historical_balances` - Historical holdings (0 credits)
- `profiler_pnl_summary` - Trade summary with top 5 trades (1 credit)
- `profiler_address_related_wallets` - Related wallets analysis (1 credit)
- `profiler_pnl` - Past trades performance (1 credit)
- `profiler_address_counterparties` - Top counterparties (5 credits)

**Token God Mode API (0-5 credits):**
- `tgm_flow_intelligence` - Token flow summary (1 credit)
- `tgm_who_bought_sold` - Recent buyers/sellers (1 credit)
- `tgm_dex_trades` - All DEX trades (1 credit)
- `tgm_transfers` - Top token transfers (0 credits)
- `tgm_holders` - Balance analysis (5 credits)
- `tgm_flows` - Inflow/outflow analysis (1 credit)
- `tgm_pnl_leaderboard` - PnL rankings (5 credits)
- `tgm_jup_dca` - Jupiter DCA orders (0 credits)
- `tgm_token_screener` - Token screening (5 credits)

#### $DATA API (17 endpoints)
Social intelligence and KOL analysis

**Discovery Intelligence:**
- `daily_discoveries` - Daily trending projects
- `weekly_discoveries` - Weekly trending analysis
- `monthly_discoveries` - Monthly trend patterns
- `latest_discoveries` - Real-time emerging discoveries
- `discovery_info` - Detailed discovery metadata
- `discovery_followers` - Key followers tracking
- `discovery_tweets_stats` - Social engagement metrics

**KOL Analysis:**
- `available_kols` - List tracked influencers
- `kol_info` - KOL profiles and background
- `kol_stats` - Performance metrics
- `kol_mentions` - Real-time mention tracking
- `kol_mentions_count` - Quantified analytics
- `kol_followers_history` - Network evolution
- `kol_followings` - Network analysis
- `kol_similarity` - Find similar accounts

**Market Intelligence:**
- `chain_mindshare` - Blockchain attention tracking
- `narrative_mindshare` - Trending narratives

#### EVA AI (4 endpoints)
Web3 security analysis and contract auditing

- `token_audit` - Comprehensive token security analysis
- `contract_audit` - Smart contract security audit
- `latest_lock` - Latest liquidity pool lock information
- `code_audit` - Solidity code security review

#### Blokiments (4 endpoints)
Token metrics and trending research

- `general_token_metrics` - General token metrics with timeframes
- `historic_data` - Historical token data
- `get_networks` - List supported blockchain networks
- `get_tokens` - List available tokens per network

#### Pump.fun Scraper (5 endpoints)
Real-time Solana token data

- `list_coins` - List newly launched coins
- `get_latest_token` - Most recent token
- `search_tokens` - Search by name/symbol
- `get_token_info` - Detailed token information
- `get_king_of_the_hill` - Current "King of the Hill" token

#### Twitter (10 endpoints)
Social media data and sentiment analysis

- `search_tweets` - Search tweets by keywords/hashtags
- `user_profile` - User profile information
- `user_tweets` - User timeline tweets
- `trending_topics` - Current trending topics
- `tweet_details` - Single tweet details
- `user_followers` - User followers list
- `user_following` - Following list
- `post_tweet` - Post new tweet
- `like_tweet` - Like specific tweet
- `retweet` - Retweet functionality

#### LinkedIn (8 endpoints)
Professional network data

- `person_profile` - User profile by URL
- `company_profile` - Company information
- `search_people` - Search by keywords/titles
- `search_companies` - Search by name/industry
- `search_jobs` - Job posting search
- `job_details` - Specific job details
- `my_network` - User's network information
- `send_message` - Send message to connection

#### Yahoo Finance (7 endpoints)
Financial market data

- `get_quote` - Real-time stock quotes
- `get_historical_data` - Historical price data
- `get_financials` - Financial statements
- `get_analysis` - Analyst recommendations
- `search_symbols` - Stock symbol search
- `market_summary` - Market status summary
- `get_options_chain` - Options chain data

#### Amazon (6 endpoints)
E-commerce and product data

- `search_products` - Product search by keyword
- `product_details` - Detailed product information
- `product_reviews` - Customer reviews
- `product_pricing` - Current pricing/offers
- `bestsellers` - Category bestsellers
- `deal_of_the_day` - Daily deals

#### Zillow (5 endpoints)
Real estate market data

- `get_property_details` - Property information
- `get_zestimate` - Zillow price estimate
- `search_properties` - Property search
- `get_local_market_data` - Market trends
- `get_mortgage_rates` - Current mortgage rates

### 2. File System Tools (4 endpoints)

- `create_file` - Create new file with content
- `str_replace` - Replace string within file
- `full_file_rewrite` - Rewrite entire file content
- `delete_file` - Delete specified file

### 3. Browser Automation Tools (15 endpoints)

- `browser_navigate_to` - Navigate to URL
- `browser_go_back` - Browser back navigation
- `browser_wait` - Pause execution
- `browser_click_element` - Click page element
- `browser_input_text` - Enter text in input field
- `browser_send_keys` - Send keyboard commands
- `browser_switch_tab` - Switch browser tab
- `browser_close_tab` - Close browser tab
- `browser_scroll_down` - Scroll page down
- `browser_scroll_up` - Scroll page up
- `browser_scroll_to_text` - Scroll to specific text
- `browser_get_dropdown_options` - Get dropdown options
- `browser_select_dropdown_option` - Select dropdown option
- `browser_drag_drop` - Drag and drop action
- `browser_click_coordinates` - Click at coordinates

### 4. Shell/Command Tools (1 endpoint)

- `execute_command` - Execute shell command in sandbox

### 5. Web Search Tools (2 endpoints)

- `web_search` - Perform web search
- `scrape_webpage` - Extract webpage content

### 6. Vision Tools (1 endpoint)

- `see_image` - Analyze image content

### 7. Deployment Tools (2 endpoints)

- `deploy` - Deploy static website to public URL
- `expose_port` - Expose sandbox port to internet

### 8. Communication Tools (2 endpoints)

- `ask` - Pause and request user input
- `complete` - Signal task completion

---

## 📊 Supported Blockchains

### Nansen API Support
- Ethereum (ETH)
- Solana (SOL)
- Polygon (MATIC)
- Binance Smart Chain (BSC)
- Avalanche (AVAX)
- Arbitrum
- Optimism
- Base
- Fantom
- Cronos

### EVA AI Support
- Ethereum (eth)
- Binance Smart Chain (bsc)
- Base (base)
- Sonic (sonic)

### Blokiments Support
- Multi-chain token metrics
- Historical data across networks
- Cross-chain trending analysis


## 📈 Performance Metrics

### System Stats
- **Total Endpoints:** 129
- **Data Providers:** 11
- **Supported Chains:** 10+

### Rate Limits
- **Nansen API:** 20 req/sec, 500 req/min
- **$DATA API:** 1 req/sec
- **EVA AI:** Standard rate limits
- **Other Providers:** Varies by provider

---

## 🔮 Upcoming Features

### Planned Integrations
- **DefiLlama** - Protocol analytics
- **0xGasless** - Gasless transactions
- **Enhanced MCP** - More external tools
- **Advanced Analytics** - Deeper insights

### Development Roadmap
- Agent flow optimization
- Performance improvements
- New data provider integrations
- Enhanced security features

---

## 📞 Support & Community

### Developer Resources
- **Documentation:** [GitHub Docs](https://github.com/vibeAIrFORCE/Docs)
- **Telegram:** [VIBE AI Community](https://t.me/VIBEaiRforce)
- **Website:** [vibe.airforce](https://vibe.airforce)

### Reporting Issues
- **Bug Reports:** Telegram community
- **Feature Requests:** GitHub issues
- **Performance Issues:** Dev team direct contact

---

*Last Updated: 17. July 2025*  
*VIBE AI Backend - 129 Endpoints of Pure Power* 