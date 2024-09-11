# LLMs-Lab-2024

This repository contains projects, research, and educational resources focused on Large Language Models (LLMs).

## 1. Task-oriented Dialogue System

   This demo implements a multi-turn, task-oriented intelligent customer service system using the OpenAI API.
   
## 2. Function-Calling

This folder contains various demos showcasing the capabilities of Function Calling.

### Function Calling Demos

   - **`POI`**:  
     This demo uses Amap's (Gaode Map) public API to retrieve information about hotels, restaurants, attractions, and other points of interest (POIs) near a specific location. It allows querying nearby POIs relative to a given point.

   - **`SQL`**:  
     This demo demonstrates how Function Calling handles sophisticated database tasks and generates SQL queries.

   - **`Stream`**:  
     This demo showcases examples of Function Calling in Stream mode.


## 3. RAG

This folder contains two different **RAG (Retrieval-Augmented Generation)** pipelines. The first one is based on Elasticsearch (ES), and the second one is based on a vector database, ChromaDb.  

- The Offline Steps are as follows:

| Document Loading      | Document Splitting | Vectorization | Insert into Vector Database |
|-----------------------|---------------------|---------------|------------------------------|
| →                     | →                   | →             | →                            |

- The Online Steps are as follows:

| Receive User Query    | Vectorize User Query | Retrieve from Vector Database | Populate Prompt Template | Call LLM with Final Prompt | Generate Response |
|-----------------------|----------------------|-------------------------------|---------------------------|----------------------------|---------------------|
| →                     | →                    | →                             | →                         | →                          | →                   |  


### Pipelines

- **`run_RAG_vector_database_pipeline`**:  
  RAG Pipeline based on ChromaDB Vector Database.

- **`run_RAG_ES_pipeline`**:  
  RAG Pipeline based on Elasticsearch (ES).

- **`RAG_pipeline_pdf_table_processing`**:  
  Offline: Extract data from tables in PDF files, embedding and then store it in a vector database.  
  Online: RAG Pipeline based on ChromaDB Vector Database.   
  The pipeline flowchart is as follows:    
  ![Alt text](RAG/data/table_rag.png)

