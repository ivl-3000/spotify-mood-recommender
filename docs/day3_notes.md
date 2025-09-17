# Day 3 – Research Notes  
## Paper: “Mood Detection in Music Using Lyrics / Multimodal Mood Detection”  

---

### 🎯 Task & Goals
- Predict mood/emotion of a song using **lyrics only**, or **lyrics + audio**.
- Mood can be modeled as:
  - **Continuous values**: valence (positive ↔ negative), arousal (calm ↔ energetic).  
  - **Discrete categories**: happy, sad, angry, relaxed, etc.  

---

### 📚 Datasets Used in Research
- **Delbouys et al. (ISMIR 2018)** – ~18,000 tracks with lyrics + audio.  
- **MoodNet (Bhattacharya et al., 2018)** – MIREX Multimodal Dataset + Million Song Dataset.  

---

### 🔧 Preprocessing Steps
- **Lyrics:**  
  - Clean text (lowercase, remove stop words, punctuation).  
  - Tokenization & word embeddings (Word2Vec, GloVe).  
- **Audio:**  
  - Convert raw signals into **Mel-spectrograms**.  
  - Extract acoustic features (tempo, energy, timbre).  
- **Labels:**  
  - Map to continuous valence/arousal or discrete mood classes.  

---

### 🧠 Models / Features
- **Classical ML:**  
  - Lexicon-based features from lyrics (emotion dictionaries).  
  - Audio features (tempo, rhythm, MFCCs).  
- **Deep Learning:**  
  - CNNs on Mel-spectrograms (audio).  
  - CNNs or RNNs on lyric embeddings (text).  
- **Fusion Approaches:**  
  - *Late Fusion:* train separate models, combine predictions.  
  - *Mid-level Fusion:* merge lyric + audio feature vectors before classification.  

---

### 📊 Key Findings
- **Audio** better captures *arousal* (energy/tempo).  
- **Lyrics** better capture *valence* (positive vs negative mood).  
- Fusing modalities (lyrics + audio) consistently outperforms single modality.  
- Deep learning outperforms classical ML when enough data is available.  

---

### 💡 Implications for My Project
- Collect both **lyrics** and **audio features** for tracks.  
- Use **pre-trained embeddings (BERT/LLMs)** for lyrics instead of simple word2vec.  
- Use **Spotify audio features API** for energy, tempo, danceability.  
- Build a **hybrid system**:  
  - Lyrics → valence prediction.  
  - Audio → arousal prediction.  
  - Combine both for mood-aware recommendations.  

---

📌 *These insights guide the Mood & Context-Aware Playlist Recommender.*  
