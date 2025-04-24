# 🌍 Web-Scraping-Projects

# Project 1️⃣ - 🧠 Huntr.co Job Listings Scraper

A Python-powered project that scrapes structured job data from [Huntr.co](https://huntr.co/jobs) by parsing the site's internal JSON response. This scraper is designed to capture detailed job and company information — ideal for researchers, job seekers, and data analysts alike.

---

## 🚀 Project Highlights

🔍 **Extracts detailed job listing information including:**
- 📄 **Job Title**
- 🏢 **Employer Details** (Name, Domain, Employee Range)
- 🌍 **Location Data** (Address, Country, Coordinates)
- 🧭 **Remote or Multi-City?**
- 📅 **Dates** (Created At, Original Post Date, Last Crawl)
- 🔗 **Job URL**
- 🧾 **Text Description**
- 🗃️ **Job Category & Location Metadata**

📦 All results are saved to a structured CSV file for easy consumption or analysis.

---

## 📂 Extracted Fields

| Field Name                | Description                                      |
|--------------------------|--------------------------------------------------|
| `id`                     | Unique job identifier                            |
| `created_at`             | Date the job was added                           |
| `original_title`         | Original job title from source                   |
| `original_post_date`     | Date posted by original job site                 |
| `textDescription`        | Job summary or full description                  |
| `isRemote`               | Whether the job is remote                        |
| `isMultiCity`            | Whether the job is available in multiple cities  |
| `original_location`      | Raw location string from original source         |
| `place_name`             | Parsed location name                             |
| `place_address`          | Street address                                   |
| `place_country`          | Country                                          |
| `place_lat` / `place_lon`| Geographic coordinates                           |
| `url`                    | Link to the job post                             |
| `employer_name`          | Employer name                                    |
| `employer_legalName`     | Legal entity name                                |
| `employer_domain`        | Company domain (e.g. stripe.com)                 |
| `employer_employees`     | Exact number of employees (if available)         |
| `employer_employeeRange` | Range of employee size (e.g. 100-500)            |

---

## 🛠️ How It Works

The script sends a request to Huntr’s job listings endpoint and parses the embedded JSON structure. Each job listing is looped over and safely extracted into a dictionary using `.get()` and `try-except` blocks to ensure robustness.

---

## 📦 How to Use

### ✅ Requirements

Install dependencies from `requirements.txt`:

```bash
pip install -r requirements.txt
```
## ▶️ Run the script
```bash
python huntr_scraper.py
```
Or, if you're using the Jupyter Notebook version:

```bash
jupyter notebook Web_Scraping_Project1.ipynb
```
## 📁 Output
A CSV file such as huntr_job_listings.csv will be generated in your working directory containing all the scraped job data.

## 💡 Use Cases
- 📊 Job market analysis

- 🔁 Job aggregation feeds

- 📬 Daily job alert tools

- 📉 Trend analysis for remote vs local roles

- 🧠 Machine Learning job classification models

## ⚠️ Notes
- ✅ This project doesn't rely on Selenium or dynamic rendering — it's lightweight and efficient.

- 🔄 If the site's response structure changes, field mappings may need to be updated.

- 🕵️‍♂️ Currently scrapes only the first page of job results — modify page logic to loop over multiple pages if needed.
