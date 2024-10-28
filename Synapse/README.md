# Azure Synapse Workspace - Climate Data Aggregation Hub

## Purpose
The Synapse Workspace is configured to clean, transform, and analyze climate data stored in Azure Data Lake Storage. It integrates data ingestion and transformation pipelines with Azure Data Factory.

## Configuration Details
- **Workspace Name**: `climate-data-synapse`
- **Region**: East US (or chosen region)
- **Linked Services**:
  - **Data Lake Storage**: `climatedatahubstorage`
  - **GitHub Repository**: Linked for version control of Synapse resources.

## Setup Instructions
1. **Workspace Creation**: Set up in Azure Portal with serverless SQL.
2. **GitHub Integration**: 
   - Go to **Manage > Git Configuration** in Synapse Studio.
   - Link to your GitHub repository to track changes and maintain version control.
3. **Data Lake Connection**:
   - Go to **Access Control (IAM)** in Data Lake Storage.
   - Assign **Storage Blob Data Contributor** role to Synapse Managed Identity.

## Common Issues
- **Data Lake Access Denied**: Check IAM permissions for the Synapse Managed Identity.
- **Git Sync Issues**: Ensure GitHub access is configured correctly in **Manage > Git Configuration**.
  
## Future Development
- Integrate with Power BI to visualize analysis results.
- Implement predictive models using Synapse ML.
