# StreamX Commerce Accelerator

This repository provides a **Commerce Accelerator built on StreamX**, designed to quickly deliver a fully functional e-commerce frontend powered by a **microservices-based mesh architecture**.

The accelerator enables you to **launch an e-commerce experience with minimal or no custom development**, while still allowing full flexibility through integration with your own data sources (e.g. PIM systems).

---

# Overview

The StreamX Commerce Accelerator delivers:

* A ready-to-use **e-commerce frontend architecture**
* A **microservices mesh** 
* Built-in support for:

    * **Product Detail Pages (PDP)**
    * **Product Category Pages (PCP)**
    * **Search and filtering (faceted search)**

The system is designed to work with **external data sources**, allowing you to plug in your own **Product Information Management (PIM)** system.

---

# Key Features

## Dynamic Commerce Pages

The accelerator provides out-of-the-box support for:

* **Product Detail Pages (PDP)** — dynamically rendered product views
* **Product Category Pages (PCP)** — dynamically rendered category views
* **Product Listings** — product listings
* **Static pages** — CMS-like content support

Dynamic pages are generated based on ingested data.

---

## Search & Faceted Filtering

Built-in search capabilities include:

* Indexing of:

    * Products
    * Categories
    * Static pages
* Full-text search
* **Faceted search** for filtering products by attributes

---

# Architecture Overview

```
PIM (emulate or external one)
     │
     │ (Cloud Events)
     ▼
StreamX Ingestion
     │
     ├── Product & Content Storage
     ├── Search Index
     └── Delivery Services
             │
             ▼
        E-commerce Frontend
```

---

# Result

You can launch a fully functional e-commerce site **in a very short time**, with the flexibility to extend and customize as needed.
