# REST-API-INGESTION-ADF
Tested and Learnt Live Inremental REST API ingestion from News API.
# 📰 News API to Azure Data Lake Pipeline

A lightweight Azure Data Factory pipeline that fetches news articles from NewsAPI.org and stores them as CSV files in Azure Data Lake Storage Gen2.

## 🎯 What It Does

This pipeline dynamically pulls news data based on your search criteria and transforms JSON responses into structured CSV format for easy analysis.

## 🛠️ Tech Stack

- **Azure Data Factory** - Orchestration
- **NewsAPI.org** - Data Source
- **Azure Data Lake Storage Gen2** - Data Storage
- **REST API** - Integration

## 📋 Prerequisites

- Azure subscription with ADF and ADLS Gen2
- NewsAPI.org API key ([Get free key](https://newsapi.org/register))

## 🚀 Quick Setup

1. **Create Linked Services**
   - REST API for NewsAPI.org base URL
   - ADLS Gen2 for storage

2. **Configure Datasets**
   - Source: REST with dynamic parameters (q, from, sortBy, page, pageSize)
   - Sink: DelimitedText (CSV) in ADLS Gen2

2. **Output Schema**
   - CSV includes: author, title, description, url, publishedAt, content

## ⚠️ Common Issues

- **400 Error**: Check API key and parameter encoding
- **Empty Results**: Verify date range and query terms
- **Rate Limits**: Free tier allows 100 requests/day

## 🔐 Security Tip

Store API keys in Azure Key Vault instead of hardcoding!

---

⭐ Star this repo if it helped you!
