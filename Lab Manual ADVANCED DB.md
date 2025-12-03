**Lab Manual: Introduction to the Document Data Model (MongoDB)**

**98283: Mark Murungi Mwenda**

|**Unit Code**|**Assignment**|**Data Model**|**Database System**|
| :- | :- | :- | :- |
|MIT 8107 |Continuous Assessment Test (CAT) |Document Data Model |MongoDB 6.0|

**1. Objectives **

Upon successful completion of this lab, the user will be able to:

1. **Install & Configure** a MongoDB instance using Docker.
1. **Execute** fundamental **CRUD** operations (Create, Read, Update, Delete) on MongoDB collections.
1. **Model** a realistic application scenario (e.g., Student Records) using the document data structure.
1. **Query** data effectively using nested fields and array structures.
-----
**2. Prerequisites and Environment Setup** 

To complete this lab, you must have the following tools installed and operational on your local machine:

- **Docker Engine** (or Docker Desktop).
- **Docker Compose** (usually included with Docker Desktop).
- A basic understanding of JSON/BSON structure.

2\.1 MongoDB Installation via Docker Compose <sup>9</sup>

We will use Docker Compose for a consistent and reproducible setup.

**Step 1: Create the Docker Compose File**

Create a file named docker-compose.yml and add the following configuration.

![A screen shot of a computer](Aspose.Words.1737e543-35b0-4817-849f-bd86256253bd.001.png)

**Step 2: Launch the Database Container**

Execute the following command in the same directory as the docker-compose.yml file:

![A screen shot of a computer](Aspose.Words.1737e543-35b0-4817-849f-bd86256253bd.002.png)

**Step 3: Access the MongoDB Shell**

Once the container is running, access the mongosh interactive shell inside the container:

![](Aspose.Words.1737e543-35b0-4817-849f-bd86256253bd.003.png)

You are now connected to the MongoDB server and ready to proceed.

**3. Basic CRUD Operations and Sample Data** 

We will demonstrate Create, Read, Update, and Delete operations using a sample database called productDB and a collection called electronics.

3\.1 Create (C) - Inserting Data

First, switch to the target database. MongoDB will create it on the first insertion.

![A screen shot of a computer&#x0A;&#x0A;AI-generated content may be incorrect.](Aspose.Words.1737e543-35b0-4817-849f-bd86256253bd.004.png)

Insert a single document:

![A computer screen shot of a computer program](Aspose.Words.1737e543-35b0-4817-849f-bd86256253bd.005.png)







Insert multiple documents:

![A computer screen shot of a program&#x0A;&#x0A;AI-generated content may be incorrect.](Aspose.Words.1737e543-35b0-4817-849f-bd86256253bd.006.png)

3\.2 Read (R) - Retrieving Data

![A computer screen shot of a computer code&#x0A;&#x0A;AI-generated content may be incorrect.](Aspose.Words.1737e543-35b0-4817-849f-bd86256253bd.007.png)

3\.3 Update (U) - Modifying Data 

Update Winnie Ngutuku's status to "Active" and add a new course.

![A screenshot of a computer program&#x0A;&#x0A;AI-generated content may be incorrect.](Aspose.Words.1737e543-35b0-4817-849f-bd86256253bd.008.png)

3\.4 Delete (D) - Removing Data 

Remove Abel Kanake's profile.

![A screen shot of a computer code&#x0A;&#x0A;AI-generated content may be incorrect.](Aspose.Words.1737e543-35b0-4817-849f-bd86256253bd.009.png)

**4. Applied Scenario: Complex Student Profile Querying ⚙️**

**Scenario:** Find all **"Active"** students enrolled in **"MIT 8107"** who are **missing** the **contact.emergency** field. This highlights querying nested fields and array elements.



4\.1 Executing the Complex Query

![A computer screen shot of a computer program&#x0A;&#x0A;AI-generated content may be incorrect.](Aspose.Words.1737e543-35b0-4817-849f-bd86256253bd.010.png)


