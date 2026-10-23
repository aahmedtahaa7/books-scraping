# Books Price & Category Analysis

An end-to-end data project: web scraping, SQL database design, and data analysis.

## Overview
Scraped 1,000 books from [books.toscrape.com](https://books.toscrape.com) (a practice site built for scraping),
stored them in a relational SQLite database, and analyzed pricing, ratings, and categories using SQL and Python.

## Tools
- **Python**: requests, BeautifulSoup, pandas, matplotlib
- **SQL**: SQLite (JOIN, GROUP BY, HAVING, window functions)
- **Google Colab** for development

## Pipeline
1. Scraped 50 listing pages (title, price, rating, availability, URL)
2. Scraped 50 category pages to map each book to its category
3. Cleaned data with pandas (types, duplicates, price tiers)
4. Stored in SQLite as two tables: `books` and `book_categories`
5. Joined tables and ran analytical SQL queries
6. Visualized results with matplotlib

## Database Schema
- `books` (book_id, title, price_gbp, rating, in_stock, url, price_tier)
- `book_categories` (url, category)

## Key Findings
- The dataset contains 1,000 books spread across 50 categories, joined from two scraped sources into a clean relational structure.
- Price and rating show almost no relationship: paying more does not mean getting a better-rated book.
- Category size varies widely, with a few large categories holding many books while many others hold only a handful.
- Average price and average rating differ from one category to another, so category is a more useful lens than price when comparing books.

## Files
- `books_final.csv`: final cleaned dataset
- `books.db`: SQLite database
- `*.png`: charts

## How to Run
Open the notebook in Google Colab and run all cells in order.
