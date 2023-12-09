# Graph Based Recommendation System for E-commerce using FAISS

### Business Context
There are hundreds of eCommerce websites with millions of products listed. Personalizing the content is much needed to engage the user with the platform. This is where recommendation systems come into the picture. You must have heard aboutsome recommendation systems such as Content-Based, Collaborative filtering, etc. In recent years Graph Learning-based Recommendation systems have witnessed fast development

In this project, we will focus on building a recommendation system for our eCommerce platform by converting generated graphs into embeddings and utilizing similarity search.

---

### Aim
To build a Graph based recommender system that will recommend the best product forthe users in e-commerce platforms depending on their purchase and search history

---

### Data Overview
The dataset contains user information with 9 attributes for an eCommerce website.

> Note: Embeeding data is not pushed because of upload size limitations.

---

### Tech Stack
- Language: `Python`
- Packages: `pandas`, `numpy`, `pecanpy`, `gensim`, `plotly`, `umap`, `faiss`, `DuckDB`
- File Management: `Parquet`
- Database Management: `SQL`, `SQL querying`

---

### Code Overview
1. **Data**
    - *ConstructedGraph*: The generated graphs from the previous project are saved here.
    - *Edg_Graphs_DataFile*: The graphs are saved in (.edg) format for further processing.
    - *Embedding_Data*: Generated embeddings are saved here.
2. **Documentation**: This folder consists of different learning resources and references.
3. **Model**: Generated models are saved in this folder.
4. **Notebook**: This folder contains the notebooks we have used.
    - Data Exploration and Data Analysis.ipynb
    - GraphConstruct.ipynb
    - Deepwalk and Node2vec Model Training.ipynb
    - Result Analysis.ipynb
    - Embedding Vector Search with ANN FAISS (Recommendation).ipynb
    - Constants.py
5. **Script**: Scripts available in .py files.
6. **requirements.txt**: The requirements.txt file has all the required libraries with respective versions. Kindly install the requirements at the beginning.

---

## Approach

1. **Understand the problem statement**
2. **Deepwalk and Node2vec Model Training**
   - Import the necessary packages and libraries
   - Read the selected graph
   - Save the graph in .edg format
   - Generate graph random walks
   - Build models using Word2Vec and Node2Vec
   - Save the embeddings in Parquet format
3. **Result Analysis and Visualization**
   - Import the necessary packages and libraries
   - Read the data
   - Define a function for generating levels of category
   - Use UMAP (Uniform Manifold Approximation and Projection) as a dimension reduction strategy
   - Visualize the clusters
4. **Embedding Vector Search**
   - Import the necessary packages and libraries
   - Use FAISS (Facebook AI Similarity Search) for generating recommendations

---

