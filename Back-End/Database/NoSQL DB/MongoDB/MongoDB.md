---
Title: MongoDB
tags: TechSkills
DateStarted: 2023-01-09
DateModified: 2023-11-28
status: 
Progress: NaN%
sr-due: 2023-07-02
sr-interval: 4
sr-ease: 276
---

## Repo

[GitHub - Jenniferwonder/mongodb-e-commerce: An e-commerce website using MongoDB, Next.js and TailwindCSS](https://github.com/Jenniferwonder/mongodb-e-commerce)

## MongoDB Account

- Username: Jenniferwonder
- MM: mCyj7qiT9ntjxl0h

## Reference

[MongoDB Course Catalog Homepage | MongoDB University](https://learn.mongodb.com/catalog?labels=%5B%22Language%22%5D&values=%5B%22Node.js%22%5D)  
[MongoDB: The Developer Data Platform | MongoDB](https://www.mongodb.com/)  
[GitHub - mongodb-developer/jumpstart-series](https://github.com/mongodb-developer/jumpstart-series)

## What & Why MongoDB?

Why? > [Comparing The Differences - MongoDB Vs MySQL | MongoDB](https://www.mongodb.com/compare/mongodb-mysql)

#### 1. Challenges and Concerns

- ![[z-Assets/Pasted image 20230320070956.png]]

##### 1.1. Data Model

- Collections
- Structure of documents
- How relationships are modeled
- How to deal with `join`?
- Too denormalized

##### 1.2. Teminology difference

![[z-Assets/Pasted image 20230320083604.png]]

#### 2. MongoDB Options & Tools

- Self-hosted
  - Open source MongoDB server
- MongoDB Atlas
  - SAAS
- MongoDB Compass
  - GUI
- MongoDB Realm
- MongoDB Atlas Search
- MongoDB Charts
- MongoDB Online Archive
- MongoDB Atlas Data Lake

## Run MongoDB Locally

#### 1. Download MongoDB Community Server

- [Download MongoDB Community Server | MongoDB](https://www.mongodb.com/try/download/community)
- offers a flexible document data model along with support for ad-hoc queries, secondary indexing, and real-time aggregations to provide powerful ways to access and analyze your data.
- The database is also offered as a fully-managed service with [MongoDB Atlas](https://www.mongodb.com/atlas/database). Get access to advanced functionality such as auto-scaling, serverless instances, full-text search, and data distribution across regions and clouds. Deploy in minutes on AWS, Google Cloud, and/or Azure, with no downloads necessary.

#### 2. Connect MongoDB local server to the app

- MongoDB Compass
- [[Mongoose]]

## Run MongoDB with MongoDB Atlas?

> [GitHub - mongodb-developer/jumpstart-series at compass](https://github.com/mongodb-developer/jumpstart-series/tree/compass)

#### 1. Set up a project and create a database in MongoDB Atlas

- Sign up/ in: [Log in | MongoDB](https://cloud.mongodb.com/v2/6417bb52bfb15d1d8f3fe4e3#/clusters)
- Create a project
  - Name your project
  - Add member (Owner is added by default)
- Build a database
  - Add current IP Address
  - Choose a plan (M0-Free)
    - ![[z-Assets/Pasted image 20230320101118.png]]
  - Provider (Azure)
  - Recommended Region (Hongkong)
  - Name for the cluster
    - ![[z-Assets/Pasted image 20230320101328.png]]
- Security > Quickstart
  - Authenticate your connection > Username and password
- Deployment > Database> Load Sample Dataset
  - 8 Databases, 21 collections

#### 2. Connect to MongoDB (with MongoDB Shell/ application/ Compass/ VS Code)

- Connect > Copy connection string
- Install [[VSCode]] Extension > MongoDB for VS Code

##### 2.1. MongoDB Compass

- Use cases
  - Visually explore data
  - Run **ad hoc queries**
  - Full CRUD functionality
  - Query performance
  - Construct **aggregation**s...
- Create Database > Collection
- Import sample data
  - [GitHub - mongodb-developer/jumpstart-series at compass](https://github.com/mongodb-developer/jumpstart-series/tree/compass)

#### 3. MongoDB Realm - Serverless Platform/ Backend as a service (without having to set up your own ==server==)

- Install Realm SDK:
  - [Install Realm - Web SDK — Realm](https://www.mongodb.com/docs/realm/web/install/#std-label-web-install)
- Connect Realm with a Next.js web app
  - [Next.js Integration Guide - Web SDK — Realm](https://www.mongodb.com/docs/realm/web/nextjs/)
  - [How to connect your NextJs app to MongoDB - YouTube](https://www.youtube.com/watch?v=mOvW3iheF14)
- Use Cases
  - Easily and securely access data from MongoDB Atlas database and bring our data into our applications
  - Functions
  - User authentication
  - Triggers
    - User authentication events
    - Preset schedule
  - Data access control
  - 3rd party services
  - GraphQL...
  - Realm sync (Sync data among different devices in real time)

#### 4. Frontend MongoDB Integration

- [How to connect your NextJs app to MongoDB - YouTube](https://www.youtube.com/watch?v=mOvW3iheF14)
- `npm i @heroicons/react`

#### 5. Search and autocomplete with MongoDB Atlas

- Lucene powered search engine
- Typo tolerance with fuzzy search
- Autocomplete
- Filters & Facets
- Custom sorting...

#### 6. Atlas Data Lake

> [Atlas Data Lake | Federated Query of .csv & .json files from AWS S3 Bucket | Jumpstart - YouTube](https://www.youtube.com/watch?v=e4BNH8SeGVs&list=PL4RCxklHWZ9v2lcat4oEVGQhZg6r4IQGV&index=7)

- It's a dederated query engine that supports MongoDB query API
- It's simple and fast to query MongoDB databases, allow object storage and HTTP data sources
  - Can get access to data files from AWS S3 bucket, analyze their data using MongoDB query language
  - Can combine and query real time Atlas data and cloud storage data, making multiple data sources seem like a single source.
  - Can save money by pushing historical data out to AWS S3 and use it as a tool to transform and enrich your application and cloud data without complex pipelines
  - Can analyze data stored in JSON, BSON, CSV, TSV, Avro, ORC and Parquet in place without complexity cost and time sync of data ingestion
  - Can run a single query to analyze data across multiple MongoDB databases and AWS S3 together, and in place for faster insights and easily persist the results to your preferred storage tier
  - Serverless: no infrastructure to set up and manage
    - Simple connect your S3 bucket within your Atlas dashboard
- Fully integrated with MongoDB Atlas and provides access to tools like MongoDB charts for data visualization, compass and realm...
- Only pay for the queries run and only when actively working with your data, eliminating the need to predict demand or capacity

## Query Language > MQL

## MongoDB Schema Design Best Practices

[MongoDB Schema Design Best Practices - YouTube](https://www.youtube.com/watch?v=leNCfU5SYR8)

## Data Modeling for MongoDB

[The Principles of Data Modeling for MongoDB - YouTube](https://www.youtube.com/watch?v=YsaOcUDUJKY&t=1085s)

### Difference between SQL and MongoDB approach

To face and answer to Constrains (physical, hardwre, software)  
![[z-Assets/Pasted image 20230320072127.png]]

#### 1. SQL Approach (3rd normal form)

![[z-Assets/Pasted image 20230320072225.png]]

#### 2. MongoDB Approach

![[z-Assets/Pasted image 20230320072315.png]]

### Techniques to Model for MongoDB

#### 1. Methodology

![[z-Assets/Pasted image 20230320072445.png]]

#### 2. Different thinking procedures

![[z-Assets/Pasted image 20230320072640.png]]

#### 3. Analyze the workload

- Listing operations
  - ![[z-Assets/Pasted image 20230320072739.png]]
- Details for an operation
  - ![[z-Assets/Pasted image 20230320072903.png]]

#### 4. Identify relationships

- Different Data Modeling
  - ![[z-Assets/Pasted image 20230320073319.png]]
- Criteria: What is used together in the application is stored together in the database.

##### 4.1. Determines Performance

- How to deal with `join`?  
  ![[z-Assets/Pasted image 20230320071530.png]]

##### 4.2. Two ways of modeling relationships

![[z-Assets/Pasted image 20230320073743.png]]

- Reference/Link
  - when the "many" side is a huge number
  - for integrity on write operations on many-to-many
  - when a piece is frequentyly used but not the other and memory is an issue
- Embeding (using one collection)
  - for integrity of read operations
  - for integrity of write operations on one-to-one and one-to-many
  - for data that is deleted or archived together
  - by default

##### 4.3. Design Patterns

![[z-Assets/Pasted image 20230320080304.png]]

#### 5. Evolving the model with the "Schema versioning" pattern

Applying the **extended reference, computed, subset, schema versioning** patterns:  
![[z-Assets/Pasted image 20230320080750.png]]  
schema versioning pattern is to optimize the releasing process  
![[z-Assets/Pasted image 20230320081256.png]]
