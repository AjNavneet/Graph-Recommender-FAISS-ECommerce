# Graph-Based Recommendation System for E-commerce using FAISS

## Business Context

With the vast number of products available on eCommerce platforms, personalizing content for users has become crucial to enhance engagement and customer satisfaction. Recommendation systems play a vital role in achieving this personalization. While traditional recommendation systems like Content-Based Filtering and Collaborative Filtering are widely used, graph-based approaches have gained significant traction in recent years due to their ability to model complex relationships between users and items effectively.

This project focuses on building a graph-based recommendation system by generating graph embeddings and utilizing similarity search with FAISS (Facebook AI Similarity Search) to deliver personalized product recommendations for an eCommerce platform.

---

## Aim

To build a graph-based recommender system that recommends the best products to users on eCommerce platforms based on their purchase and search history.

---

## Data Overview

The dataset contains user information with nine attributes collected from an eCommerce website. The attributes include:

- User ID
- Product ID
- Purchase history
- Search queries
- Product categories
- Time of interaction
- Purchase frequency

**Note**: Embedding data is not pushed to the repository due to upload size limitations.

---

## Tech Stack

- **Programming Language**: [Python](https://www.python.org/)
- **Libraries and Frameworks**:
  - [`pandas`](https://pandas.pydata.org/) and [`numpy`](https://numpy.org/) for data manipulation and analysis.
  - [`pecanpy`](https://pecanpy.readthedocs.io/en/latest/) and [`gensim`](https://radimrehurek.com/gensim/) for graph embeddings.
  - [`umap`](https://umap-learn.readthedocs.io/en/latest/) for dimensionality reduction.
  - [`faiss`](https://github.com/facebookresearch/faiss) for similarity search and recommendations.
  - [`plotly`](https://plotly.com/) for interactive visualizations.
  - [`DuckDB`](https://duckdb.org/) for database management.
- **File Management**: Parquet format for efficient storage and processing.
- **Database Management**: SQL querying for data manipulation.

---

## Approach

### 1. Problem Understanding
- Define the scope of the recommendation system.
- Analyze the data to identify user-item interaction patterns.

### 2. Graph Construction
- Use interaction data to construct user-product graphs.
- Save the graphs in `.edg` format for compatibility with embedding tools.

### 3. Embedding Generation
- Generate random walks on the graph using techniques like DeepWalk and Node2Vec.
- Train embedding models using Word2Vec and Node2Vec algorithms.
- Save the embeddings in Parquet format for further use.

### 4. Dimensionality Reduction and Visualization
- Use UMAP (Uniform Manifold Approximation and Projection) for reducing embedding dimensions.
- Visualize user-product clusters to identify patterns and similarities.

### 5. Recommendation System Development
- Use FAISS (Facebook AI Similarity Search) to build a scalable recommendation engine.
- Perform similarity searches on the embedding vectors to recommend products.

### 6. Result Analysis
- Evaluate the quality of recommendations.
- Visualize clusters and analyze user preferences.

---

## Project Structure

```plaintext
.
├── data/                                  # Contains data files.
│   ├── ConstructedGraph/                  # Generated graphs from user-item interactions.
│   ├── Edg_Graphs_DataFile/               # Graphs saved in .edg format.
│   ├── Embedding_Data/                    # Generated graph embeddings.
├── documentation/                         # Learning resources and reference materials.
├── models/                                # Saved models for embeddings and recommendations.
├── notebooks/                             # Jupyter notebooks for experimentation.
│   ├── Data_Exploration_and_Analysis.ipynb
│   ├── Graph_Construct.ipynb
│   ├── Deepwalk_and_Node2Vec_Training.ipynb
│   ├── Result_Analysis.ipynb
│   ├── Embedding_Vector_Search_with_FAISS.ipynb
├── scripts/                               # Python scripts for modular tasks.
├── requirements.txt                       # List of dependencies with versions.
└── README.md                              # Project documentation.
```

---

## Getting Started

### 1. Clone the Repository

```bash
git clone <repository_url>
cd <repository_folder>
```

### 2. Install Dependencies

Install the required libraries using the following command:

```bash
pip install -r requirements.txt
```

### 3. Run the Project

- Train embedding models and generate recommendations:

```bash
python scripts/train_embeddings.py
```

- Perform similarity search using FAISS:

```bash
python scripts/faiss_search.py
```

### 4. Explore Results

- Visualize user-item clusters and analyze results using the Jupyter notebooks in the `notebooks` folder.
- Check the `Embedding_Data` folder for saved embeddings and recommendations.

---

## Results

- **Personalized Recommendations**:
  - Generated product recommendations based on user purchase and search history.
- **Graph Insights**:
  - Visualized clusters to understand user-product relationships.
- **Efficient Similarity Search**:
  - FAISS enabled fast and scalable recommendations.

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a feature branch:

```bash
git checkout -b feature-name
```

3. Commit your changes:

```bash
git commit -m "Add feature"
```

4. Push your branch:

```bash
git push origin feature-name
```

5. Open a pull request.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Contact

For any questions or suggestions, please reach out to:

- **Name**: Abhinav Navneet
- **Email**: mailme.AbhinavN@gmail.com
- **GitHub**: [AjNavneet](https://github.com/AjNavneet)

---

## Acknowledgments

Special thanks to:

- [FAISS](https://github.com/facebookresearch/faiss) for enabling fast and efficient similarity searches.
- [pecanpy](https://pecanpy.readthedocs.io/en/latest/) and [gensim](https://radimrehurek.com/gensim/) for graph embeddings.
- [umap](https://umap-learn.readthedocs.io/en/latest/) for dimensionality reduction.
- [DuckDB](https://duckdb.org/) for its fast and efficient database capabilities.

---
