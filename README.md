# Requirements for Microsoft Power BI Copilot

Microsoft Power BI Copilot is an AI-powered feature aimed at simplifying users' data analysis and visualization processes. Copilot has capabilities such as allowing users to write queries in natural language, automatically generating reports, and discovering insights.

![image](https://github.com/aysegulyigitbi/Powerbi/assets/127193220/f5d5bd07-3646-482b-b10a-b39b013b7d98)


## Using Copilot

To use Copilot, the first step is to carefully evaluate the data in your semantic model and make necessary adjustments. This process enhances Copilot's ability to derive insights from the data. It is essential to have an F64 or P1 capacity and for this capacity to be located in specific regions to use Copilot. If your capacity is not in one of these regions, unfortunately, you cannot use Copilot.

## Pricing

Copilot in Microsoft Fabric is not supported in trial SKUs. This means Copilot only operates on paid SKUs (F64 or above, or P1 or above). At these capacity levels, Microsoft Fabric costs approximately $10k per month (pay as you go), while Premium Capacity costs approximately $5k per month.

## Geographical Regions of Capacities

The geographical region where your capacity is located and where Azure OpenAI service is hosted directly affects the availability and performance of Copilot. A geographical region typically represents a specific country or group of countries and usually includes certain geographical restrictions to meet data protection and compliance requirements. For example, a geographical region could be the US, Europe, or Asia.

The geographical region where Azure OpenAI service is hosted is where the service is provided, and where data is processed. This typically affects response times and data privacy and security standards. The geographical region where your capacity is located is where your operations and data are hosted. This is usually the region where your business is located or where you predominantly operate. Matching the geographical region of your capacity with where Azure OpenAI service is hosted generally provides faster response times and better performance.

Data transfer between geographical regions, especially between capacities and Azure OpenAI services in different geographical regions, may sometimes be necessary. In this case, appropriate arrangements need to be made for secure transfer and processing of data from one geographical region to another.

For example:
- If your capacity is in the US geographical region and Azure OpenAI service is also hosted in the US geographical region, data processing will occur in the same region as your capacity, and no additional action is required to use Copilot.
- If your capacity is in the UK geographical region and Azure OpenAI service is hosted in the EU Data Boundary geographical region, then your data processing geographical region will be outside your capacity's region. Therefore, you will need to enable cross-geo data processing to use Copilot.
- If your capacity is in geographical regions such as Australia, Brazil, Canada, India, Asia, Japan, Korea, South Africa, Southeast Asia, or the United Arab Emirates, and Azure OpenAI service is hosted in the US geographical region, you will need to enable cross-geo data processing to use Copilot.

## Admin Portal Configuration

Before starting to use Copilot, your administrator needs to enable tenant switching. Administrators can enable Copilot for specific security groups or entire organizations. Users in these groups can use the preview of Copilot and other features supported by Azure OpenAI.

![image](https://github.com/aysegulyigitbi/Powerbi/assets/127193220/42296293-fb11-4e60-9b65-60cbb4a75abf)


Data sent to Azure OpenAI can be processed outside your capacity's geographical region, compliance boundary, or national cloud instance.

![image](https://github.com/aysegulyigitbi/Powerbi/assets/127193220/d6a8b1f3-1e1e-4983-a101-e7c9d35dc5ce)


## Copilot - Considerations Regarding Data Sets

There are several important points to consider regarding data sets:

- **Table Relationships:** All relationships should be clearly defined, indicating whether they are one-to-many, many-to-one, or many-to-many relationships.
- **Calculation Logic and Naming Conventions:** It is essential for measures to have standardized calculation logic and clear naming conventions.
- **Predefined Measures:** Adding predefined measures that users may need in reports facilitates data analysis.
- **Real and Dimension Tables:** Clearly defining real tables crucial for analysis and creating supporting dimension tables is necessary.
- **Column Names and Data Types:** Column names should be clear, and correct data types should be applied to ensure accurate data analysis.
- **Relationship Types and Consistency:** Clearly specifying relationship types and ensuring data consistency enhances report accuracy.
- **Key Performance Indicators (KPIs) and Data Refresh:** Creating KPIs relevant to the business context and determining data refresh schedules strengthen data analysis.
- **Security and Metadata:** Defining access levels for data and documenting the data model structure are critical for data security and management.
