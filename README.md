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

## Screenshots from Azure

1. Complete Pipeline inside Until Loop
<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/29fa72c8-917e-4b3a-a0f9-ca8efb899e1b" />

2. Success workflow of Pipeline from ingestion to dumping
   - This executed within a minute showing fast processing
<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/4d7276c7-fa5f-4a87-8a5e-c8b6ccc2d391" />

3. Testing Deployement in Azure DevOps
<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/d1d4de42-a9a7-426f-a353-9969b5f56add" />

## ⚠️ Common Issues

- **400 Error**: Check API key and parameter encoding
- **Empty Results**: Verify date range and query terms
- **Rate Limits**: Free tier allows 100 requests/day

## 🔐 Security Tip

Store API keys in Azure Key Vault instead of hardcoding!

---

⭐ Star this repo if it helped you!
