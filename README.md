Consumer Behavioral Dataset

Description

This repository contains a structured dataset of real-world consumer complaint records collected from a publicly available regulatory disclosure source.

The dataset represents actual customer–company interactions rather than survey responses.
Each record corresponds to a customer complaint regarding a financial product or service and includes metadata, timestamps, and written complaint text.

The purpose of the dataset is to enable behavioral analysis, sentiment analysis, and study of customer reaction patterns over time.

---

Dataset Size

- Total Records: ~788,000+
- Features: 16 columns
- Time Range: January 2010 – February 2026
- Data Type: Semi-structured (categorical + temporal + unstructured text)

---

Data Fields

Column Name| Description
record_id| Unique identifier of complaint
date| Complaint submission date
year| Extracted year from timestamp
month| Extracted month from timestamp
company| Company involved in the complaint
product_service| Product or service category (credit card, loan, mortgage, etc.)
issue| Specific issue reported by the customer
event_type| Type of event (complaint)
complaint_text| Written customer statement (unstructured text)
sentiment_score| Numeric sentiment indicator derived from text
sentiment_label| Positive / Neutral / Negative classification
customer_action| Action taken by the consumer
company_response| Company’s reported response
country| Reported location information
source| Source reference identifier
url| Public record reference link

---

Data Characteristics

Behavioral Nature

The dataset captures revealed behavior rather than stated opinion.
Records originate from real service interactions where a customer experienced a problem significant enough to file a complaint.

Semi-Structured Format

The dataset contains:

- categorical attributes (company, product type)
- temporal attributes (date, year, month)
- unstructured natural language text (complaint statement)

Class Imbalance

Complaints are naturally negative-biased events.
Therefore sentiment distribution is expected to be skewed toward negative sentiment.

---

Data Validation & Cleaning

The following validation steps were applied:

- Removed duplicate records using unique identifiers
- Standardized date formats
- Normalized company and product category naming
- Filtered empty complaint texts
- Basic text preprocessing (lowercasing, whitespace normalization)
- Generated sentiment indicators from complaint text

Missing Data

Observed missing values:

- rating: majority missing (not used in analysis)
- location fields: small percentage missing
- text field: minimal missing after filtering

---

Data Limitations

- Domain limited to financial services complaints
- Represents only customers who chose to file a complaint
- Geographically concentrated (primarily US-based reporting)
- Not representative of satisfied customers
- Sentiment labels are derived, not user-provided

---

Intended Uses

This dataset is suitable for:

- Sentiment analysis
- Topic modeling
- Time-series complaint trends
- Company comparison studies
- Customer pain-point identification
- Reaction analysis to product/service issues

---

Not Recommended Uses

- Market share estimation
- Customer satisfaction scoring
- Population behavior generalization
- Sales prediction

---

Ethical & Usage Note

The dataset is based on publicly available regulatory records.
No private or personally identifiable information is intentionally included.
The dataset is provided for research, educational, and analytical purposes only.

---

Repository Structure

/data_raw        Raw extracted records
/data_clean      Processed and validated dataset
/scripts         Extraction and preprocessing scripts
