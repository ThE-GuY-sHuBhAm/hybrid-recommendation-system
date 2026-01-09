# 🎵 Hybrid Recommender System for Music

An end-to-end **Hybrid Music Recommendation System** that combines **content-based filtering**, **collaborative filtering**, and a **weighted hybrid strategy** with user-controlled diversity.

The project is designed as a **scalable, experiment-driven ML system**, integrating **cloud storage (AWS S3)**, **reproducible pipelines (DVC)**, and **distributed computation support**, and is deployed via an interactive **Streamlit application**.

---

## 🚀 Project Overview

This system recommends music tracks by combining:

- **Content similarity** derived from song metadata and engineered features  
- **User listening behavior** from large-scale interaction logs  
- A **hybrid weighting mechanism** that balances personalization and discovery  

The architecture is built to support **local experimentation**, **cloud-backed data versioning**, and **future scalability**.

---

## 🎯 Key Features

- 🎧 Content-based recommendations using vectorized song features  
- 👥 Collaborative filtering from user–item interaction matrices  
- 🔀 Weighted hybrid recommendation engine with diversity control  
- 📊 Interactive **Streamlit** UI with audio previews  
- 📦 End-to-end **DVC pipeline** with cloud (S3) support  
- ☁️ AWS-ready data and artifact storage  
- ⚙️ Distributed computation support (Dask)  
- 📒 Notebook-driven experimentation and analysis  
- 🐳 Dockerized and deployment-ready  
- 🧪 Automated application health testing  

---

## 🗂️ Dataset & Data Management

The system uses a combination of:

- **Million Song Dataset**
- **Spotify metadata & preview URLs**
- **Last.fm user listening history**

### Data Handling

- Data preprocessing and transformations are tracked using **DVC**
- Datasets and intermediate artifacts can be stored locally or on **AWS S3**
- Versioned pipelines ensure reproducibility across environments

---

## 🧠 Recommendation Approaches

### 1️⃣ Content-Based Filtering

- High-dimensional feature representations of songs  
- Similarity computed using vector-based methods  
- Effective for cold-start scenarios and new content discovery  

### 2️⃣ Collaborative Filtering

- User–song interaction matrix built from implicit feedback  
- Captures collective listening patterns across users  
- Supports large sparse matrices  

### 3️⃣ Hybrid Recommendation System

- Weighted combination of content-based and collaborative scores  
- User-controlled diversity slider adjusts recommendation behavior  
- Enables smooth trade-offs between personalization and exploration  

---

## 🧩 Design Decisions & Trade-offs

- **Why Hybrid Recommendation?**  
  Hybrid models mitigate the limitations of pure content-based or collaborative approaches and perform better across diverse user scenarios.

- **Why Cloud & Distributed Tooling?**  
  The project is structured to scale beyond local experimentation, enabling cloud-backed data storage (AWS S3) and distributed processing (Dask).

- **Why Streamlit?**  
  Streamlit enables rapid iteration and intuitive interaction with recommendation results while remaining lightweight for prototyping.

- **Why DVC with S3?**  
  DVC ensures reproducible pipelines, while S3 enables scalable storage of datasets and artifacts.

- **Why Jupyter & Visualization Libraries?**  
  Jupyter, Matplotlib, Seaborn, and Bokeh are used for exploratory analysis, debugging, and result interpretation during experimentation.

---

## 🧪 ML Pipeline (DVC)

```text
data_cleaning
│── raw music data → cleaned_data.csv

transform_data
│── feature engineering → transformed_data.npz

interaction_data
│── user listening history → interaction matrix

transformed_filtered_data
│── hybrid-ready feature matrix
```

---

## 🖥️ Application Interface

The Streamlit application provides:

- Song and artist input  
- Configurable number of recommendations  
- Diversity control slider  
- Spotify audio previews  
- Visual feedback for recommendation balance  

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone <repository-url>
cd hybrid-recommender-system
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ (Optional) Configure AWS

```bash
aws configure
```

### 4️⃣ Run the application

```bash
streamlit run app.py
```

---

## 🐳 Docker Support

```bash
docker build -t hybrid-recommender .
docker run -p 8501:8501 hybrid-recommender
```

---

## 🧪 Testing

```bash
pytest test_app.py
```

Performs a basic health check to ensure the application loads correctly.

---

## 📁 Project Structure

```text
├── app.py
├── content_based_filtering.py
├── collaborative_filtering.py
├── hybrid_recommendations.py
├── data_cleaning.py
├── transform_filtered_data.py
├── data/
├── notebooks/
├── dvc.yaml
├── dvc.lock
├── Dockerfile
├── requirements.txt
├── test_app.py
```

---

## ⚠️ Limitations

- Offline evaluation metrics are not yet integrated  
- Cold-start handling relies primarily on content similarity  
- Distributed execution is currently optional  
- Not optimized for real-time, high-throughput inference  

---

## 🚧 Current Status

- ✅ Core recommendation logic implemented  
- ✅ Streamlit UI functional  
- ✅ Cloud-ready DVC pipeline  
- ✅ Experimentation environment established  
- 🚀 Deployment-ready (not currently live)

---

## 🔮 Future Improvements

- Advanced evaluation metrics and model benchmarking  
- Improved cold-start strategies  
- Fully asynchronous inference pipeline  
- Background task orchestration (Celery)  
- Production deployment on AWS infrastructure  

---

## 📌 Tech Stack

- Python  
- Streamlit  
- Pandas, NumPy, SciPy, Scikit-learn  
- DVC + AWS S3  
- Dask (distributed processing)  
- Jupyter, Matplotlib, Seaborn, Bokeh  
- Docker  
- PyTest  

---

## 📄 License

This project is intended for educational, experimental, and portfolio purposes.
