# Azure Data Factory - Climate Data Ingestion Pipelines

## Purpose
Manages ingestion and processing of climate data from external sources (e.g., GitHub) into Data Lake Storage.

## Configuration Details
- **Data Factory Name**: `ClimateDataFactory`
- **Region**: East US
- **Pipelines**:
  - **TestCopyPipeline**: Basic pipeline that copies sample data from GitHub to Data Lake.

## Setup Instructions
1. **Create Data Factory in Azure Portal**.
2. **Configure Linked Services**:
   - **Source**: HTTP linked service for GitHub (public dataset).
   - **Sink**: Azure Data Lake Storage Gen2 (linked to `climatedatahubstorage`).
3. **Create a Pipeline**:
   - Go to **Author** in Data Factory Studio.
   - Add a **Copy Data** activity with GitHub as the source and Data Lake as the sink.

## Common Issues
- **Permission Denied**: Check Data Factory managed identity permissions in Data Lake.
- **Pipeline Fails**: Review pipeline logs in **Monitor** for details on failures.

## Future Development
- Schedule pipelines for regular ingestion of updated data.
- Add transformations to clean and prepare data before storage.
