# How to VIBE with Your VIBE.aiRforce Agent

Welcome, VIBEr! You're about to embark on a journey with a VIBE.aiRforce AI Agent – your quirky, smart, and incredibly capable partner in conquering tasks. Get ready to Think. VIBE. Done.

This guide will help you understand how your agent thinks, operates, and how you can best interact with it to achieve amazing results.

---

## 🚀 Quick Start: Shortcut Buttons for New VIBErs

**New to VIBE AI?** Don't worry about crafting the perfect prompt! We've got you covered with shortcut buttons that demonstrate our agent capabilities instantly.

### How to Use Shortcut Buttons:
1. **Look for the suggestion buttons** under the text input area
2. **Click any button** that interests you (Investment Opportunities, Ethereum Project Analysis, Show Tools & Examples, etc.)
3. **Make coffee ☕** while our agents work their magic
4. **Return to see comprehensive results** - full analysis, research, or demonstrations ready!

### Available Shortcut Categories:
- **Investment Opportunities**: Get market analysis and investment insights
- **Ethereum Project Analysis**: Deep dive into Web3 projects and tokenomics
- **Show Tools & Examples**: Discover all available agent capabilities
- **Pump.fun Scanner**: Analyze new token launches with VIBE ratings
- **Smart Wallet Analysis**: Track whale movements and trading patterns
- **KOL Research**: Social sentiment and influencer analysis

**Pro Tip**: These buttons are perfect for first-time users who want to experience our agent superpowers without overthinking prompts. Click → Coffee ☕ → Results!

---

*   **Your Agent's Identity:** Think of your agent as a full-spectrum autonomous assistant. It can research, write, develop software, analyze data, and solve problems creatively. It's got a Linux environment, internet access, and a whole suite of tools.
*   **The VIBE Philosophy:** We're about making advanced tech accessible, powerful, playful, and even a bit meme-worthy.
*   **Workspace:** Your agent operates in a `/workspace` directory. When you talk about files, use paths relative to this (e.g., `src/main.py`, not `/workspace/src/main.py`).

---

## 🚀 Getting Your VIBE On: Effective Tasking

### 1. Be Clear and Specific
The more precise your request, the better your agent can plan and execute. Your VIBE.aiRforce agent thrives on detail!

*   **Good Examples:**
    *   "Research the top 3 competitors for a new Solana-based DeFi protocol focused on yield farming, analyze their tokenomics, current market cap, and recent community activity on Twitter. Provide a summary in a markdown file named `competitor_analysis.md`."
    *   "Create a simple Python script that fetches the current price of Ethereum from CoinGecko API and saves it to `eth_price.txt`. Then, write a short paragraph explaining how to run this script."
    *   "Generate a landing page `index.html` with a connected `style.css` for a new VIBE AI project called 'MemeCoin Analyzer'. The page should have a catchy headline, a brief description, and a placeholder for a demo video. Use our brand colors: Beige Background (`#a99d7e`) for the page, Text Black (`#22201c`) for text, and Hoodie Blue (`#4a7c97`) for accents."
*   **Needs Improvement (Too Vague):**
    *   "Tell me about DeFi."
    *   "Write some code."
    *   "Make a website."

### 2. Understand Its Capabilities
Your agent is packed with tools and skills. Knowing what it can do helps you ask for the right things.

*   **File Operations:** Creating, reading, modifying, deleting files, organizing, converting formats.
*   **Data Processing:** Scraping websites, parsing JSON/CSV/XML, cleaning data, generating reports.
*   **System Operations:** Running CLI commands, managing archives, installing packages (it has `sudo`!).
*   **Web Search & Browsing:** Advanced web searching, extracting content, interacting with web pages (filling forms, clicking buttons).
*   **Visual Input:** It can "see" images you provide using a specific tool. If an image is in the `/workspace`, tell the agent: `Use the 'see-image' tool for 'path/to/your/image.png'`.
*   **Blockchain Integration:** Direct interaction with Ethereum and other blockchain networks, smart contract analysis, wallet tracking.
*   **Data Providers:** Your agent has direct lines to specific data sources for:
    *   LinkedIn
    *   Twitter
    *   Zillow
    *   Amazon
    *   Yahoo Finance
    *   Active Jobs
    *   **$DATA API** (DataBot integration for social intelligence)
    *   **Pump.fun Scanner** (Token analysis with VIBE ratings)
    *   **Smart Wallet Analyzer** (Whale tracking and trading patterns)
    *   **EVA AI** (Enhanced research capabilities)
    *   **Pro Tip:** If your task involves these, the agent prefers using these providers for accuracy and up-to-date info over general web scraping. "*Use the Twitter data provider to find recent tweets mentioning VIBE.aiRforce.*"

### 3. How Your Agent "Thinks" (The `todo.md` Flow)
Your agent is methodical. When you give it a task, it:
1.  Creates a `todo.md` file for itself, breaking down your request into actionable steps.
2.  Works through these steps one by one.
3.  Provides you with **narrative updates** in Markdown directly in its responses, explaining what it's done, what it's about to do, and why.
4.  Marks tasks as complete `[x]` in its `todo.md`.
5.  Once all tasks are done, it will either use the `complete` tool (if fully finished) or the `ask` tool (if it needs final confirmation or has deliverables for you).

**Your Role in the Flow:**
*   Pay attention to its narrative updates – they are your window into its VIBE!
*   If it uses the `ask` tool, it's waiting for your input! This is the *only* time it pauses its work loop for you.

---

## 🛠️ Interacting with Tools & Commands

### CLI vs. Python
*   Your agent prefers using **CLI (Command Line Interface) tools** for efficiency, especially for file operations, text processing, and system tasks. (e.g., `grep`, `awk`, `sed`, `jq`, `csvkit`).
*   It uses **Python** for complex logic, custom processing, or when CLI tools aren't enough.

### Long-Running Commands
*   If the agent needs to run something that might take a while (like a development server `npm run dev` or a lengthy data processing script), it will run it **asynchronously** (`run_async="true"`). This means it won't wait for it to finish before doing other things or talking to you.
*   It uses "sessions" to keep related commands organized.

### Sharing Your Agent's Work: Previews & Public Deployment
Your agent can make its creations accessible in a couple of ways:

1.  **Temporary Previews (`expose-port` tool):**
    *   If your agent sets up a local web server or service (e.g., a Next.js app running on port 3000, or an API on port 8000 within its workspace), it can use the `expose-port` tool.
    *   This tool generates a **temporary public URL** that you can use to view and interact with the service directly from your browser.
    *   **Use Case:** Great for development, quick previews of web pages, or testing an API it has built before full deployment.
    *   **Example Prompt:** "*Create a simple Flask API with one endpoint `/hello` that returns 'Hello, VIBEr!'. Run it and expose the port so I can test it.*"

2.  **Permanent Public Deployment (`deploy` tool via Cloudflare Pages):**
    *   For static websites (HTML, CSS, JavaScript, and assets like images), your agent can deploy them to a **permanent public URL** using Cloudflare Pages.
    *   This is for when you want to share the site more broadly or for a longer term.
    *   **Crucial VIBE Check:** The agent will **ALWAYS ask for your confirmation** using the `ask` tool before deploying to a public Cloudflare URL. This ensures you're ready for it to go live.
    *   Ensure all assets (images, scripts, stylesheets) use relative paths for the deployment to work correctly.
    *   **Example Prompt:** "*Take the `index.html` and `style.css` we created for the 'MemeCoin Analyzer' and deploy it to a public server for everyone to VIBE with.*"

### Web Content Extraction Workflow (Important!)
Your agent has a strict hierarchy for getting web information:
1.  **Data Providers First:** If a dedicated data provider exists (LinkedIn, Twitter, etc.), it uses that.
2.  **`web-search`:** To find relevant URLs.
3.  **`scrape-webpage`:** To get detailed content from those URLs.
4.  **Direct Browser Tools:** ONLY if `scrape-webpage` fails or the page needs interaction (logins, dynamic content, button clicks).
    *   If it gets stuck (e.g., CAPTCHA), it might use `web-browser-takeover` to ask for your help.

**Pro Tip for Users:** If you know a page requires login or heavy interaction, you can suggest the agent might need to use its direct browser tools after trying `scrape-webpage`. "*The site example.com/dashboard requires a login, you might need to use browser tools after checking with `scrape-webpage`.*"

---

## 📝 Content Creation & Design

### Writing Style
*   Expect detailed content, often in continuous paragraphs, infused with the VIBE.aiRforce spirit. Your agent aims for comprehensive, high-quality documents.
*   It will cite sources if writing based on references.

### Design Tasks (e.g., Reports, Web Pages)
1.  It will first create designs in **HTML+CSS** for flexibility, often incorporating VIBE AI branding elements if requested.
2.  Designs are made with print-friendliness in mind.
3.  The final output for documents is usually a **PDF**, converted from the HTML+CSS.
4.  If it creates web content (like an `index.html`), it will often provide a **preview URL** (using `expose-port`) from its local server so you can see it immediately before considering a permanent `deploy`.

**Key for Website Deployment (Recap):**
*   For temporary viewing or development: Agent uses `expose-port`.
*   For making a static site publicly accessible on a lasting URL: Agent uses `deploy` (via Cloudflare Pages) **after your explicit confirmation via the `ask` tool.**

---

## 💬 Communication: The Art of the VIBE

*   **Narrative Updates:** Your agent will communicate proactively in its responses, using Markdown to explain its actions and reasoning. You don't usually need to respond to these unless it specifically uses the `ask` tool.
*   **The `ask` Tool:** This is CRITICAL. When the agent uses `<ask>...</ask>`, it means:
    *   It **NEEDS your input** (clarification, confirmation, choices, missing info).
    *   It **PAUSES** its work until you respond.
    *   This is how it delivers files to you or asks for final approval before completing a task (like deploying a website!).
*   **Attachments:** When the agent creates something for you to see (HTML files, PDFs, images, reports), it will attach them when it uses the `ask` tool. **If you should SEE it, it will ATTACH it.**
*   **`complete` Tool:** The agent uses this ONLY when ALL tasks in its `todo.md` are finished and verified. This terminates its execution for that request.

**Golden Rule:** If your agent says `<ask>I've drafted the landing page and exposed it for preview at [URL]. What do you think before we consider deploying it publicly?</ask>` and attaches `index.html`, it's your turn to speak! Otherwise, its narrative updates are just keeping you in the VIBE loop.

---

## 💡 Pro Tips for a Smooth VIBE

*   **Iterative Refinement:** If the first result isn't perfect, provide feedback. Your agent can revise. "*This VIBE is good, but can you make the blue accents brighter and add a section about our Giraffe mascot?*"
*   **Complex Tasks:** Break them down if they feel too large, or trust the agent to create a detailed `todo.md`. You can always ask, "*What's your plan for this task?*"
*   **File Paths:** Remember, all file paths are relative to `/workspace`.
*   **Ask for Previews:** For web content or designs, feel free to ask the agent: "*Can you run a local server and expose the port so I can preview the `index.html` file?*"
*   **Patience for Complex Steps:** Some operations (like deep research or code generation) take time. The agent's narrative updates will let you know it's working hard, vibing on your request.
*   **Error Handling:** The agent is designed to be robust, but if it seems stuck or confused, try rephrasing or simplifying the immediate goal. If it makes 3 `todo.md` updates without completing a task, it's programmed to reassess or ask you for guidance.

---

## 🌐 Advanced Web3 VIBES: Blockchain Intelligence & DeFi Mastery

VIBE.aiRforce agents are built for Web3! Here are advanced use cases that showcase our blockchain superpowers:

### 1. Smart Money Tracking & Whale Analysis
*   **Use Case:** You want to track successful crypto traders and copy their strategies.
*   **Prompt Examples:**
    *   "*Use the smart wallet analyzer to track wallets that bought [TOKEN] in the last 24 hours and analyze their historical performance. Focus on wallets with >80% win rate.*"
    *   "*Find wallets that are accumulating Solana ecosystem tokens this week and provide a detailed analysis of their trading patterns.*"
    *   "*Track the top 10 whale movements on Ethereum today and identify any coordinated buying patterns.*"

### 2. Token Launch Analysis & Gem Hunting
*   **Use Case:** Discovering profitable opportunities in new token launches.
*   **Prompt Examples:**
    *   "*Scan pump.fun for new tokens launched in the last hour. Identify the top 3 with the highest Hype Score and give me their VIBE Check reports.*"
    *   "*Use multiple data providers to analyze [CONTRACT_ADDRESS] - check tokenomics, holder distribution, liquidity, and social sentiment. Provide investment recommendation with risk rating.*"
    *   "*Find Solana tokens under $1M market cap with active development and growing communities. Generate gem profiles for the top 3 candidates.*"

### 3. DeFi Protocol Intelligence
*   **Use Case:** Optimizing yield farming and DeFi strategies.
*   **Prompt Examples:**
    *   "*Compare yield farming opportunities across Ethereum, Solana, and Polygon. Find the highest APY with <5% risk rating.*"
    *   "*Analyze the TVL changes across major DeFi protocols in the last 30 days and identify emerging opportunities.*"
    *   "*Track upcoming token unlocks that could impact major DeFi tokens in the next 30 days.*"

### 4. KOL & Social Sentiment Analysis
*   **Use Case:** Leveraging social intelligence for trading decisions.
*   **Prompt Examples:**
    *   "*Use the $DATA API to analyze crypto influencer sentiment around [PROJECT]. Include follower growth, engagement rates, and credibility assessment.*"
    *   "*Track the top daily trending crypto discoveries and analyze their social engagement patterns.*"
    *   "*Map the relationship network between the top 5 Ethereum influencers and identify their shared investment themes.*"

### 5. Cross-Chain Arbitrage & MEV Opportunities
*   **Use Case:** Finding profitable arbitrage opportunities across different chains.
*   **Prompt Examples:**
    *   "*Scan for arbitrage opportunities between Ethereum and Solana DEXs with >2% profit margin.*"
    *   "*Monitor cross-chain bridge activity and identify potential MEV opportunities.*"
    *   "*Compare the same token prices across different DEXs and chains to find arbitrage possibilities.*"

### 6. NFT & Gaming Token Analysis
*   **Use Case:** Analyzing NFT projects and gaming tokens for investment opportunities.
*   **Prompt Examples:**
    *   "*Research the top 3 Solana NFT projects by trading volume this week. Analyze their communities, utility, and price trends.*"
    *   "*Find GameFi tokens launched in the last 6 months with active communities and analyze their tokenomics.*"
    *   "*Track whale movements in the NFT space and identify trending collections before they pump.*"

### 7. Regulatory & Compliance Monitoring
*   **Use Case:** Staying ahead of regulatory changes that might impact investments.
*   **Prompt Examples:**
    *   "*Monitor regulatory news and announcements that might affect DeFi protocols in the next quarter.*"
    *   "*Analyze the compliance status of major centralized exchanges and identify potential risks.*"
    *   "*Track government blockchain initiatives and their potential impact on crypto markets.*"

### 8. Portfolio Optimization & Risk Management
*   **Use Case:** Building and managing a diversified crypto portfolio.
*   **Prompt Examples:**
    *   "*Analyze my current portfolio allocation and suggest rebalancing strategies based on market conditions.*"
    *   "*Create a risk-adjusted portfolio for $10K investment across different crypto sectors.*"
    *   "*Monitor correlation between my holdings and suggest diversification opportunities.*"

### 9. Gasless DeFi Operations (Coming Soon!)
*   **Use Case:** Execute DeFi operations without gas fees using 0xGasless integration.
*   **Future Capabilities:**
    *   24/7 autonomous trading strategies
    *   Micro-transaction DeFi operations
    *   Scalable multi-user agent deployments
    *   Enterprise-grade automation solutions

**Pro Web3 Tips:**
*   **Combine Multiple Tools:** "*Use Nansen to find smart money buying [TOKEN], then use DefiLlama to check if they're farming yield with it, and create a comprehensive analysis.*"
*   **Risk Assessment:** Always ask for risk ratings and position sizing recommendations
*   **Real-Time Monitoring:** Set up continuous monitoring for important metrics
*   **Cross-Reference Data:** Use multiple data sources to validate findings


---

## 🌐 Web2 VIBES: Everyday Tasks Unleashed

While VIBE.aiRforce is a champ in the Web3 arena, its powerful capabilities are fantastic for a wide range of Web2 tasks too! Here are some ideas to get your VIBE flowing for everyday productivity and creativity:

1.  **Market Research & Competitive Analysis:**
    *   **Use Case:** You're launching a new online an e-commerce store for sustainable pet toys and need to understand the market.
    *   **Prompt Idea:** "*Research the top 5 online stores selling sustainable pet toys in North America. For each, identify their main product categories, typical price range for a best-selling toy, and 2-3 unique selling propositions they highlight. Summarize this in `market_research_pets.md`.*"

2.  **Content Creation & Summarization:**
    *   **Use Case:** You need to quickly understand a complex topic or generate a blog post outline.
    *   **Prompt Idea (Summarization):** "*Read the articles at [URL1], [URL2], and [URL3] about the future of remote work. Extract the key trends and challenges discussed, and provide a bullet-point summary in `remote_work_summary.txt`.*"
    *   **Prompt Idea (Outline):** "*Generate a blog post outline for an article titled '10 Tips for Effective Time Management for Busy Professionals'. Include a catchy introduction, main points for each tip with a brief explanation, and a concluding thought. Save this as `blog_outline_timemanagement.md`.*"

3.  **Email Drafting & Communication:**
    *   **Use Case:** You need to compose a professional email.
    *   **Prompt Idea:** "*Draft a follow-up email to a potential client, Ms. Jane Doe (jane.doe@example.com), after a productive meeting yesterday. Reference our discussion about VIBE AI's data analysis capabilities and propose a short demo next week. Keep the tone professional but friendly. Save as `follow_up_email_janedoe.txt`.*"

4.  **Personalized Travel Planning:**
    *   **Use Case:** Planning a weekend trip.
    *   **Prompt Idea:** "*Plan a 3-day weekend itinerary for a trip to Paris, France, for someone interested in art museums and local cafes. Include suggestions for 2 museums, 3 cafes, and one evening activity. Also, find a well-rated (4 stars or above) hotel near the Louvre. Present this in a readable format in `paris_trip_plan.md`.*"

5.  **Learning & Skill Development:**
    *   **Use Case:** You want to learn the basics of a new programming concept.
    *   **Prompt Idea:** "*Explain the core concepts of Python decorators for a beginner. Provide a simple code example of a decorator that logs function calls and save the explanation and code in `python_decorators_intro.py`.*"

6.  **Social Media Content Brainstorming:**
    *   **Use Case:** You need fresh ideas for your brand's Instagram.
    *   **Prompt Idea:** "*Brainstorm 5 Instagram post ideas for a VIBE.aiRforce social media campaign. Each idea should include a visual suggestion (e.g., image of our Giraffe mascot, screenshot of the UI) and a caption concept highlighting a key VIBE AI feature. Format this in `insta_ideas_vibeai.md`.*"

**Remember to VIBE with these too:**
*   Be specific about the desired output format (e.g., `.md`, `.txt`, `.py`).
*   Provide URLs if you want the agent to research specific web pages.
*   Leverage the agent's ability to use its data providers (Twitter, LinkedIn, etc.) even for Web2-centric research if relevant!

---

## 🎯 Battle-Tested VIBE Prompts

Here are some of our most effective prompts that have been tested by the VIBE community:

### Comprehensive Token Analysis:
```
Analyze Ethereum token [CONTRACT_ADDRESS] using: 
1) Blokiments data for metrics on market cap, liquidity, holders, and security
2) Technical indicators with clear buy/sell signals
3) Twitter KOL sentiment with credibility assessment
4) Documentation review for utility status and tokenomics
5) Investment recommendation with risk rating, position size, entry/exit points for a risk-hungry investor seeking 5-10x potential
Compare to 2-3 similar projects and highlight competitive advantages.
```

### Quick Investment Decision:
```
Use a data provider and tell me if buying this coin is a wise decision right now. I'm risk-hungry. CA: [CONTRACT_ADDRESS]
```

### KOL & Social Analysis:
```
Use a Twitter data provider to find recent tweets mentioning [PROJECT] from key opinion leaders. Analyze sentiment and provide credibility assessment.
```

### Gem Discovery:
```
Scan pump.fun for new tokens launched in the last hour. Identify the top 3 with the highest Hype Score and give me their VIBE Check reports.
```

### Smart Money Tracking:
```
Use the top_traders data provider to get the top traders for contract: [CONTRACT_ADDRESS] and give me a brief analysis of what the data shows about trading patterns.
```

**Pro Tip:** These prompts are designed to work with our 20+ integrated tools and data providers. Feel free to modify them based on your specific needs!

---

Happy VIBING! We're excited to see what you and your VIBE.aiRforce agent accomplish together. Remember to bring your unique VIBE to every interaction! 
