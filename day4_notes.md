# Day 4 – Research Notes  
## Paper: “Hybrid Recommender Systems – A Survey” + Related Literature

---

### 🛠 Definition & Types of Hybrids
- Hybrid RS = combination of two or more approaches (Collaborative Filtering, Content-Based, Knowledge-Based, Demographic).  
- Common hybridization strategies:
  - **Weighted Hybrid:** blend scores from multiple recommenders.  
  - **Switching Hybrid:** choose algorithm based on situation (e.g. new user vs long-time user).  
  - **Cascade Hybrid:** one model refines results from another.  
  - **Feature-Combination / Meta-Level:** combine features or use output of one as input to another.  
  - **Mixed Hybrid:** present results from different recommenders together.  

---

### 🔧 Problems Hybrid Systems Address
- **Cold-start:** new users or new items.  
- **Data sparsity:** when user–item matrix has few interactions.  
- **Over-specialization:** pure content-based recommenders repeat similar items.  
- **Popularity bias:** pure CF tends to recommend only popular items.  

---

### 📊 Evaluation & Use Cases
- Domains: movies, music, e-commerce, news.  
- Metrics: Precision, Recall, F1, nDCG, novelty, diversity, coverage.  
- Hybrid systems often outperform single models in accuracy + robustness.  

---

### ⚖ Pros & Cons

| **Pros** | **Cons** |
|----------|----------|
| Higher accuracy & more robust | More complex architecture |
| Handles cold-start better | Requires more data/metadata |
| Reduces sparsity issues | Higher computation cost |
| Improves diversity & novelty | Harder to tune (weights, fusion logic) |
| Flexible, can use multiple data types (ratings, text, audio, metadata) | Maintenance overhead |

---

### 💡 Implications for My Project
- My recommender will combine:
  - **Collaborative Filtering (CF)** → captures user–item interaction patterns.  
  - **Content Features** (lyrics, audio, metadata).  
  - **Mood/Context Detection** → adds personalization by emotional state.  
- Important to evaluate beyond accuracy (e.g. diversity, novelty).  
- Need to manage compute cost → use efficient embeddings + scalable algorithms.  

---

📌 *These insights confirm that a hybrid approach is essential for the Spotify Mood & Context-Aware Playlist Recommender.*  
