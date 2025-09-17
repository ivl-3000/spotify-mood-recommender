# Day 2 – Research Notes  
## Paper: The Million Playlist Dataset Challenge (RecSys 2018)

---

### 📄 Dataset Details
- **1,000,000 playlists** created by real Spotify users.  
- Covers ~ **2 million unique tracks** and ~ **300,000 artists**.  
- Metadata includes:
  - Playlist title  
  - Tracks list (track name, artist, album)  
  - Playlist length (# of tracks, albums, edits, followers)  
- Timeframe: playlists created between **2010–2017**.  
- Note: dataset does *not* include raw audio features → must fetch via Spotify API if needed.  

---

### 🎯 Task: Automatic Playlist Continuation (APC)
- Given **seed tracks** (and possibly playlist title), recommend additional tracks.  
- Test cases included multiple scenarios:
  - Only playlist title  
  - Title + first 5 tracks  
  - 10 tracks given  
  - 25 tracks given (title + random subset)  
  - Title only (cold start problem)  

---

### 📊 Evaluation Metrics
- **R-Precision:** measures relevant tracks retrieved.  
- **NDCG (Normalized Discounted Cumulative Gain):** evaluates ranking quality.  
- **Recommended Songs Clicks:** number of refreshes before a relevant track appears (lower is better).  

---

### ✅ What Worked
- **Collaborative Filtering (Matrix Factorization, ALS)** → strong baseline.  
- **Neighborhood-based models** (track-to-track similarity).  
- **Ensemble models** → combining collaborative + content-based performed best.  
- More seed tracks → better performance.  

---

### ⚠️ Challenges / What Didn’t Work
- **Playlist titles alone** → sparse, noisy, and low predictive power.  
- **Cold-start problem** → very hard to recommend when no seed tracks are given.  
- **Long-tail problem** → rare tracks/artists poorly predicted.  

---

### 🔮 Limitations & Future Work
- Missing **audio/acoustic features** in dataset (must fetch externally).  
- Scalability issues → dataset is huge, needs efficient methods.  
- Better handling of sparse titles and cold-start playlists required.  

---

### 💡 Ideas for My Project
- Don’t rely only on playlist titles → instead use **lyrics + sentiment + audio**.  
- Implement **hybrid recommender** (collab + content + mood-aware).  
- Use evaluation metrics like **Precision@K, Recall@K, NDCG** to measure model quality.  
- Add **mood/context detection** (lyrics + social media sentiment) to address cold-start.  

---

📌 *These notes will guide the design of my Mood & Context-Aware Playlist Recommender.*  
