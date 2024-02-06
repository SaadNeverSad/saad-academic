---
title: (Cloud) Caching in BigQuery
subtitle: Understanding how caching works in BigQuery and leveraging it effectively can lead to significant cost savings and improved efficiency.

# Summary for listings and search engines
summary: Understanding how caching works in BigQuery and leveraging it effectively can lead to significant cost savings and improved efficiency.

# Link this post with a project
projects: []

# Date published
date: '2023-10-19T00:00:00Z'

# Date updated
lastmod: '2023-10-19T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: ''
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - Cloud

categories:
  - Tips
---

Greetings, fellow GCPwarriors 🛡️ ! 
BigQuery offers a caching mechanism that plays a crucial role in optimizing query performance. Understanding how caching works in BigQuery and leveraging it effectively can lead to significant cost savings and improved efficiency. In this article, we'll delve into the caching mechanism in BigQuery, its limitations, and provide tips to optimize its usage.

## 🔦 What is Caching in BigQuery :

Caching involves storing query results in temporary tables within BigQuery for faster data retrieval. This temporary storage helps optimize compute performance by reducing the need for repeated computations.

## 🪝 How Caching Works :

- All queries in BigQuery are cached by default.
- Cached results are retained for 24 hours.
- Retrieving data from the cache is free.
- Each IAM account has its unique cache.
- The cache key is the query itself, while the cache value is a temporary table.
- Query comparison is performed using a simple "=", any deviation such as extra spaces results in a cache miss.

## 🚫 Limitations of Caching:

- Query results are cached only if the subsequent query is an exact replica of the original.
- Changes to underlying data in views or tables invalidate cached results.
- No caching for external data sources other than Cloud Storage.
- Query results must not exceed 10 GB.
- Queries using non-deterministic functions or are not cached.
- No caching if you have security rules on your rows/columns.

## ✨ Tips for Cache Usage:

- Avoid non-deterministic functions like RAND or CURRENT_TIMESTAMP, and other functions such as SESSION_USER().
- Avoid querying wildcard tables `FROM my_tables_*`
- Ensure no streaming buffer is connected to the table. Even if there are no writes, the results will not be cached.
- Force caching to save money with `--require_cache`.
- Disable caching for testing purposes using `WHERE RAND() < 3` or `--nouse_cache` option.

