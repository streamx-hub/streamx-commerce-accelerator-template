# 📁 Project Directory Documentation

---

#### 📂 `data/`

Contains all the **sample data** needed to be ingested for the website to be functional. It stores:

- Layouts
- Dynamic templates
- Static pages
- Page fragments
- **CSS, JS** files
- Product and category data

This is the **place where we simulate source systems** such as **CMS, PIM, etc.**

---

#### 📂 `mesh/`

Definition of the **StreamX Mesh** and all its associated **configurations and secrets**.

The configuration and secrets files are referenced as configuration sources in `mesh.yaml`,
by using the `environmentFrom: configs:` and `environmentFrom: secrets:` nodes.

#### 📂 `mesh/secrets`

Secrets can be managed in one of the following ways:

* Plaintext secrets  
  Place them in the `/mesh/secrets/plaintext` directory.  
  ⚠️ This directory is listed in `.gitignore`, ensuring that plaintext secrets are never committed to the Git repository.


* Encrypted secrets  
  Place them in the `/mesh/secrets/encrypted` directory.  
  Refer to the `StreamX Dashboards` documentation for details on the supported encryption mechanism and how to use it.



#### 📂 `scripts/`

Collection of **scripts** responsible for:

- **Ingesting data**
- **Setting up environments**

---

#### 📂 `spec/`

Contains the **data model definition**, which serves as the **contract** between the website and the
source systems.

---