# Edit-Field-IF-Node-Customer-Data-Manually-Automation
This workflow automates the processing of customer data by combining records from an n8n Datastore with data from a Google Sheet. It manually triggers, retrieves, cleans, evaluates, and processes customer information through conditional logic using Edit Fields and IF nodes.

🧩 How the Workflow Works

When executed, the workflow starts with a manual trigger inside n8n. It first pulls all customer records from the Customer Datastore (n8n training) using the getAllPeople operation. Next, it connects to a Google Sheet to read rows that contain additional or updated information, allowing the workflow to merge or compare multiple data sources. After retrieving both datasets, the workflow uses an Edit Fields node to modify, restructure, or prepare the combined data for further logic.

The core decision-making occurs in the IF node, where the workflow evaluates a specific condition to determine how each customer record should be processed. If the condition returns true, the data flows into Edit Fields1, where targeted transformations or updates are applied. If the condition returns false, the data is sent to Edit Fields2, where alternate adjustments are made. This branching logic makes it easy to handle customers differently based on data quality, status, or segmentation rules.

🔍 Key Features

Manual Execution for full control during testing or training

Datastore Integration to fetch existing customer profiles

Google Sheet Connectivity for importing external or supplementary customer data

Data Cleaning & Preparation through Edit Fields

Conditional Processing using IF logic

Two Independent Output Paths to handle different scenarios or customer groups

📚 Use Cases

Customer segmentation

Data validation and cleanup

Merging internal and external customer records

Running manual checks before syncing to CRMs

Learning or teaching n8n workflow fundamentals

🗂 Repository Contents

workflow.json — The exported n8n workflow

README.md — Documentation for setup and understanding

🚀 Importing the Workflow

Open n8n

Click Import → From File

Select the workflow JSON

Activate or manually execute the workflow

🔧 Customization Possibilities

You can extend this automation by adding:

Auto-sync to Google Sheets, Airtable, or CRMs

Email/SMS updates

Data validation rules

API integrations

Automated notifications

📄 License

This project is released under the MIT License and is free for personal and commercial use.
