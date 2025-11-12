Azure Data Factory – Incremental Data Load Pipeline

Overview
This project demonstrates an Azure Data Factory (ADF) pipeline designed to:

Copy data from a source system to a destination.
Implement incremental data loading using watermark strategy.
Provide an option for backdated data loads for historical processing.


Features
✅ Full data copy for initial load.
✅ Incremental load based on last modified date.
✅ Parameterized backdate option for historical data.
✅ Error handling and logging.
✅ Scalable and secure design

Architecture
<img width="1597" height="461" alt="image" src="https://github.com/user-attachments/assets/8d815ded-c774-43eb-92e2-67b765842011" />

<img width="1135" height="324" alt="image" src="https://github.com/user-attachments/assets/d8f99164-3301-422b-abe4-e27e5592a128" />


Prerequisites
Azure subscription.
Azure Data Factory instance.
Source and destination data stores (e.g., Azure SQL, Blob Storage).
Linked services configured for source and sink.


Setup Instructions

Clone the repository:
Shellgit clone https://github.com/<your-repo>.gitShow more lines

Import pipeline JSON into Azure Data Factory.
Configure linked services and datasets.
Set pipeline parameters:

LoadType (Full / Incremental)
BackDate (Optional date for historical load)


How It Works

Full Load: Copies all data from source to destination.
Incremental Load: Uses watermark column to fetch only new or updated records.
Backdate Load: Allows loading data for a specific historical date.



arameters

















ParameterDescriptionLoadTypeFull or Incremental loadBackDateDate for historical data processing

Monitoring

Use ADF Monitor tab to track pipeline runs.
Check activity logs for errors and performance metrics.
