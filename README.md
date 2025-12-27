# turbo-octo-system

# Reddit Market Pulse Analyzer

A lightweight, local CLI tool designed to analyze specific subreddits for recurring user pain points, unanswered questions, and sentiment trends.

## 🎯 Purpose

This project is a personal research tool intended to help understand community needs within specific technical and entrepreneurial niches (e.g., r/SaaS, r/rust, r/startups). 

Instead of manual browsing, this tool programmatically:
1.  Fetches recent threads based on keyword filters.
2.  Analyzes the ratio of "problem" statements vs. "solution" comments.
3.  Generates a local summary of high-interest topics.

## 🚀 Features (In Development)

* **Respectful Polling:** Strictly adheres to Reddit's API rate limits (X-Ratelimit-Remaining).
* **Keyword Filtering:** Filters out noise/spam to focus on genuine user discussions.
* **Local Processing:** No external data storage; all analysis happens in-memory or primarily on the local client.
* **OOD Detection:** (Planned) Filters out out-of-distribution topics that don't match the research criteria.

## 🛠️ Stack

* **Language:** Rust (using `reqwest` for API calls)
* **Analysis:** Local NLP heuristics for sentiment tagging.

## 📦 Usage

*Note: This tool requires a valid Reddit API Client ID and Secret.*

1.  Clone the repository.
2.  Create a `.env` file with your credentials:
    ```
    CLIENT_ID=your_id
    CLIENT_SECRET=your_secret
    USER_AGENT=local:market-analyzer:v0.1.0 (by /u/yourusername)
    ```
3.  Build and run:
    ```bash
    cargo run --release
    ```

## ⚠️ Disclaimer

This application is for **personal research and educational purposes only**. It does not scrape data for commercial resale, nor does it use data to train public LLMs. It is designed to be a read-only "listening" tool to better understand community problems.
