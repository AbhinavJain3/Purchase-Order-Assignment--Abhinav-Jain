# Purchase-Order-Assignment--Abhinav-Jain

# Gmail Purchase Order Pipeline

This repository implements a complete pipeline to process Gmail purchase order emails efficiently. The pipeline includes the following steps:

1. **Login to Gmail**: Uses the `IMAPClient` library to securely connect to your Gmail inbox.
2. **Email Classification**: Filters and identifies emails related to purchase orders.
3. **Attachment Extraction**: Downloads and processes email attachments, such as PDF files.
4. **Data Extraction**: Extracts relevant information from attachments using `PyPDF2` and regex.
5. **Data Structuring**: Utilizes a Large Language Model (LLM) to convert unstructured data into a structured format.
6. **Data Presentation**: Formats and presents the extracted data in a visually appealing tabular format.

---

## Features

- **Automated Gmail Integration**: Fetches emails and downloads attachments seamlessly.
- **Robust Classification**: Identifies purchase order emails using keyword-based matching with confidence scoring.
- **Efficient Data Extraction**: Extracts key details like PO number, customer information, and item details from PDF attachments.
- **LLM Integration**: Uses an advanced LLM to structure unstructured data into a consistent JSON format.
- **Elegant Presentation**: Displays the structured purchase order details in a readable and attractive tabular format.

---

## Prerequisites

Ensure the following are installed:

- Python 3.7+
- Required libraries:
  ```bash
  pip install python-docx pandas PyPDF2 imapclient llama-index-llms-azure-openai llama-index-embeddings-azure-openai
  ```
- A valid Gmail account with IMAP enabled.
- Access to an Azure OpenAI service instance for LLM integration.

---

## How It Works

1. **Login to Gmail**  
   Connect to Gmail using `IMAPClient` and authenticate securely.

2. **Email Classification**  
   Emails are analyzed and classified based on subject and body content to identify those related to purchase orders.

3. **Attachment Extraction**  
   Attachments from the classified emails are downloaded, including PDFs containing purchase order details.

4. **Data Extraction**  
   Key information is extracted from attachments using `PyPDF2` and regex patterns for fields like:
   - PO Number
   - Customer Name
   - Total Quantity
   - Total Amount

5. **LLM for Structuring Data**  
   The raw extracted data is passed to an LLM to organize it into a well-defined JSON structure.

6. **Presentation**  
   The structured data is showcased in an HTML table for easy review and sharing.

---

Feel free to contribute and make this pipeline even better! 🚀
