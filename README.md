# Raghava Documentation
:octocat: Documentation by Raghava


### Week 1 - Tutorials/Introduction
- Learnt and went through intro tutorials for NetworkX, Neo4j and what ICD 11 API - for foundation data and MMS data
- Introduced to MongoDB and Elasticsearch.

### Week 2 - Data Management
- Ran Python scripts to download data from the ICD 11 API 
- Parsed raw json files to readable format
- Pushed local data to MongoDB

### Week 3 - Tree Development and Search Algorithm
- Imported the json file into a NetworkX graph and made each disease into a single node with childs as edges
-  Created a list of dictionaries corresponding to the diseases in ICD11
- Wrote a recursive function to extract all cardiovascular diseases from the nodes and stored the IDs in a separate list

### Week 4 - Tree Parsing and Advanced AI Search Algorithms
- Used the list of cardiovascular diseases created last week to create a hierarchical tree in NetworkX starting from the Root Cardiovascular code as taken from the ICD 11 Browser
- Plotted the tree to visualize the hierarchy and the spread of diseases
- Created a list of all paths (shortest) from the root node to different leaf nodes to gauge number of children per root
- Conducted some EDA to map codes to their titles and get a count of first degree children per root disease 
- Plotted simple bar and bubble plots to visualize the diseases with the maximum number of childs. 

### Week 5 - Visualizations based on ICD 11 Codes and Extension Codes
- Extracted lists of disease hierarchies for 4 main Cardiovascular disease groups: Cardiomyopathy, Ischaemic Heart Disease, Cardiac Arrhythmia and Heart Valve Disease using a recursive algorithm
- Inputted the resulting dictionaries into a d3.js to plot the tree hierarchies
- Got familiarized with Elastic search 

### Week 6 - Implement ICD-11 in exploration real scenarios (e.g.,case reports)
- Got set up on AWS server to work with the big ICD 11 data
- Created a list of all Cardiovascular diseases using recursion 
- Imported this file into the AWS server to run the indexing and the searching python scripts using elastic search which outputted a list of dictionaries with pmid, title and abstract of disease
- Then used the pmid and title to come up with a data frame of number of occurences of each disease in our case records 
- Then on this dataframe I performed TF-IDF and clustering using K-Means - Results were inconclusive