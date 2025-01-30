## Data Engineering Project

### Project Overview

This project aims to analyze the Tokyo Olympics dataset using Databricks and Apache Spark. The data is stored in Azure Data Lake Storage and is processed using PySpark to derive insights such as top coutnries with the highest number of gold medals, and gender distribution across various disciplines.

### Architecture

The architecture of the project involves the following components:

- **Data Source**: CSV files from Kaggle
- **Ingestion**: Azure Data Factory ingests the data into the `raw-data` folder in Azure Data Lake Storage Gen 2.
- **Transformation**: Databricks is used for data transformation.
- **Storage**: Transformed data is saved back into Azure DAta Lake Storage under the `transformed-data` folder.
- **Querying**: The tansformed data is loaded into Azure Synapse Analytics for querying.

![Architecture Diagram]()

### Techonologies Used

- **Terraform**: Infrastructure as Code (IaC) tool used for provisioning infrastructure
- **Azure Data Factory**: Data integration service for creating data pipelines.
- **Azure Data Lake Storage (ADLS)**: Scalable and secure data lake for high-performance analytics.
- **Databricks**: Cloud-based platform for data engineering adn machine learning.
- **Apache Spark**: Open-source unified analytics engine for large-scale data processing.
- **PySpark**: Python API for Spark, used for performing data processing tasks.

### Data Sources

Source: [Dataset]()

The data is stored in a container within Azure Data Lake Storage and includes the following datasets:

- **athletes.csv**: Information about the athletes.
- **coaches.csv**: Information about the coaches.
- **entriesgender.csv**: Gender distribution in different sports.
- **medals.csv**: Medal tally by country.
- **teams.csv**: Information about teams participating in different events.

### Configuration

To connect to Azure Data Lake Storage, configure the following settings in your Databricks environment:
```
configs = {}

```

### Data Mounting 

Mount the Azure Data Lake Storage container in Databricks:

```
dbutils.fs.mount()
```

### Data Ingestion

Data is ingested into the `raw-data` folder in Azure Data Lake Storage via Azure Data Factory. The following datasets are available for processing:

-`athletes.csv`
-`coaches.csv`
-`entriesgender.csv`
-`medals.csv`
-`teams.csv`

### Data Exploration and Processing

#### 1. Reading the Data
Read the datasets from the raw-data directory:

```
athletes = spark.read.format("csv").option("header", "true").option("inferSchema", "true").load("")
```

#### 2. Data Schema
Explore the schema of the datasets:

```
athlets.printSchema()
```

#### 3. Data Transformation
Perform transformations on the datasets as required:

 - **Casting Columns**: Convert `Female, Male,` and `Total` columns to IntergerType in `entriesgender` dataset.

 ```
from pyspark.sql.function import col
from pyspark.sql.types import IntegerType

```

- **Calculating Average Entries by Gender**: Compute the average number of male and female participants for each discipline.

```
```

- **Top God Medal Countries**: List the countries with the highest number of gold medals.

```
```


#### 4. Data Storage
After transformation, save the results in the `transformed-data` directory in Azure DAta Lake Storage:

```
```

#### 5. Loading into Synapse
 Load the transformed data into Azure Synapse Analytics for further querying. This step involves creating external tables in Synapse that reference the data stored in Azure Data Lake Storage.

### Results and Insights

 - **Top Gold Medal Countries**: The United States leads the gold medal tally, followed closely by China and Japan.
 - **Gender Distribution**: Athletics has the highest number of participants with failry balanced gender distribution gender distribution. Artistic Swimming is female-dominated.

### Conclusion

This project demonstrates the use of Databricks, PySpark, and Azure Data Lake Storage for data engineering tasks, including data ingestion, transformation, and analysis. It showcases the capability to process and analyze large datasets effectively in the cloud.



