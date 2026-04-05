# Databricks-DB
# 🚀 Nivesh-Mitra: Democratizing Wealth Creation for Bharat

[![Track](https://img.shields.io/badge/Hackathon_Track-Digital_Aartha-blue)](#)
[![Python](https://img.shields.io/badge/Python-3.10+-yellow.svg)](#)
[![Databricks](https://img.shields.io/badge/Databricks-ML-red.svg)](#)
[![Sarvam AI](https://img.shields.io/badge/Sarvam_AI-Sovereign_LLM-orange.svg)](#)

**Nivesh-Mitra** is an end-to-end, multilingual GenAI pipeline that acts as a localized financial advisor. It bridges the gap between institutional-grade quantitative investing and retail investors in Tier-2 and Tier-3 Indian cities by translating complex market math into simple, native-language audio narratives.

## ⚠️ The Problem
Right now, data-backed stock market investing in India is a privilege reserved for the English-speaking elite. Everyday investors want to grow their wealth, but they are locked out by complex financial jargon, language barriers, and a lack of personalized, accessible advice.

## 💡 Our Solution
We built a **Neuro-Symbolic AI Architecture**. Instead of relying on a standard LLM wrapper (which is prone to financial hallucinations), Nivesh-Mitra uses deterministic Machine Learning to calculate risk-adjusted returns, and Generative AI to safely and natively explain those returns in languages like Hindi, Telugu, and Tamil.

---

## 🧠 Architecture & Data Flow

![Nivesh-Mitra Architecture](parquets/databricks.drawio%20(3).png)

Our pipeline executes in under 10 seconds through four distinct stages:

1. **The Quantitative Engine (Databricks + LightGBM):**
   * Ingests historical data for 300 NSE stocks via Yahoo Finance.
   * Computes complex momentum, volatility, and MACD features.
   * Uses LightGBM to predict future ROI and extracts the Top-K optimal stocks.
2. **Live RAG & Sentiment (HuggingFace + FinBERT):**
   * Scrapes real-time financial news via Google News.
   * Runs articles through FinBERT to calculate a live Sentiment Score (-1 to 1).
   * Generates a **Composite Weighted Score** (70% ROI + 30% Sentiment).
3. **The Neuro-Symbolic Agent (Sarvam-m):**
   * Constructs a strict, dynamic prompt combining the math, news context, and user intent.
   * Synthesizes the data into a completely objective, 40-word English narrative.
4. **Localization & Voice (Sarvam Translate + Bulbul:v3):**
   * Translates the English narrative into the user's chosen local language.
   * Synthesizes the text into a native `.wav` audio file for seamless mobile listening.

---

## 🛠️ Key Engineering Features (Built for Production)

* **Zero Financial Hallucinations:** The LLM does *not* calculate stock weights; it only formats pre-calculated Databricks data.
* **Automated Data Imputation:** Real-world data is messy. If a stock lacks weekend news, our pipeline safely injects a neutral baseline to prevent application crashes and hallucination.
* **Fault-Tolerant Prompting:** Engineered with strict character limits and Regex markdown-stripping to bypass Text-to-Speech API constraints.
* **Regulatory Compliance:** Automated injection of *"Invest at your own risk"* disclaimers before translation.

---

## 💻 Tech Stack
* **Data & ML:** Databricks, LightGBM, `yfinance`, Pandas
* **Context & NLP:** HuggingFace Inference API, FinBERT, `gnews`
* **Generative AI:** Sarvam AI (`sarvam-m`)
* **Voice & Localization:** Sarvam Translate API, Sarvam TTS (`bulbul:v3`)

---

## 🚀 Installation & Usage

**1. Clone the repository**
```bash
git clone [https://github.com/YourUsername/nivesh-mitra.git](https://github.com/YourUsername/nivesh-mitra.git)
cd nivesh-mitra
