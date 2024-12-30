# New-Limit-Azure-Project
## Overview
This project's aim is to display my skills leveraging various Azure AI services to build a scalable and intelligent solution for translating and managing community feedback. Below, you will find a breakdown of the Azure AI services used, their purposes, and how they are integrated into the project.

## Services Used

### 1. **Azure AI Services previously known as Azure Cognitive Services**
- **Text Translation**: Used for automatically translating community feedback into multiple languages.
- **Sentiment Analysis**: Helps determine the overall sentiment (positive, neutral, or negative) of the feedback.

### 2. **Azure Functions**
- **Purpose**: Acts as the backend for processing untranslated comments.
- **Implementation**: Azure Functions listen to new feedback stored in Azure Blob Storage and trigger the translation process.

### 3. **Azure Blob Storage**
- **Purpose**: Serves as the central storage for all feedback data.
  - **Untranslated Feedback**: Raw user submissions.
  - **Translated Feedback**: Outputs from the Azure Cognitive Services translation API.

### 4. **Azure API Management**
- **Purpose**: Acts as a gateway for managing API calls securely and efficiently.
- **Integration**: Routes user feedback from the frontend to Azure Blob Storage and ensures secure communication.

### 5. **Azure Logic Apps**
- **Purpose**: Automates workflows for error handling, such as retrying failed translations or notifying administrators of system issues.

### 6. **Azure Monitor**
- **Purpose**: Tracks the performance and health of the services.
- **Key Metrics**: Latency, error rates, and throughput of feedback processing.

## Project Workflow
1. Users submit feedback through a simple web interface [New Limit Website Repo](https://github.com/Xaidor/New-Limit-Website-.git).
2. Feedback is sent to Azure Blob Storage via the API gateway.
3. Azure Functions process new untranslated feedback and invoke the translation API from Azure Cognitive Services.
4. Translated feedback is stored in a separate container in Blob Storage.
5. Optional: Sentiment analysis is performed to tag feedback with emotional context.
6. Monitoring and logging ensure the system runs smoothly and errors are addressed promptly.

## Why Azure AI?
Azure AI services provide:
- **Scalability**: Handle large volumes of feedback with minimal latency.
- **Flexibility**: Integrate seamlessly with other Azure services.
- **Intelligence**: Use state-of-the-art models for translation and sentiment analysis.

## Getting Started
1. Clone the repository.
2. Configure the Azure resources as per the project documentation.
3. Deploy the Azure Functions and API Management configurations.
4. Run the web interface locally or deploy it to Azure App Service.
5. Test the end-to-end workflow by submitting feedback.

## Future Improvements
- Incorporate additional AI capabilities like entity recognition or custom text analytics.
- Add a dashboard for administrators to view feedback trends and insights.
- Enhance error-handling mechanisms with more robust logic apps.

## Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request to improve the project.

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.
