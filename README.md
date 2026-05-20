# Enhancing Social Recommendation through Sequential and Session Modeling with Transformers

A unified deep learning framework that combines **Sequential Recommendation**, **Session-based Modeling**, and **Social Recommendation** using **Transformer Networks** to generate more personalized and context-aware recommendations.

---

# 📌 Overview

Modern recommender systems often focus on only one aspect of user behavior:

- Long-term interaction history  
- Short-term session behavior  
- Social influence  

However, real-world user preferences are influenced by all three.

This project proposes a **social-aware transformer-based recommendation framework** that integrates:

✅ Sequential user interactions  
✅ Session-level behavioral patterns  
✅ Social network influence  

to improve recommendation accuracy and ranking quality.

---

# ✨ Key Features

- 🔹 Transformer-based sequential recommendation
- 🔹 GRU-based session encoder
- 🔹 Social embedding integration using user social graphs
- 🔹 Dual-encoder fusion architecture
- 🔹 Attention-based temporal modeling
- 🔹 Top-K recommendation generation
- 🔹 Evaluation using Recall@10 and NDCG@10

---

# 🧠 Proposed Architecture

The framework combines three major signals:

## 1️⃣ Sequential Behavior
Captures long-term user interaction patterns using Transformer Encoder.

## 2️⃣ Session-based Behavior
Captures short-term user intent using GRU networks.

## 3️⃣ Social Influence
Uses social embeddings derived from the Douban social graph.

These representations are fused using an **MLP-based Fusion Layer** to generate final recommendations.

---

# 🏗️ Architecture Flow

```text
User Interaction Sequence
            ↓
     Embedding Layer
(Item + Position Encoding)
            ↓
    Transformer Encoder
            ↓
 Sequential Representation
                    ↘
 Session Data → GRU Encoder
                    ↘
 Social Network → Social Embedding
                        ↓
                Fusion Layer (MLP)
                        ↓
               Top-K Recommendations

# 📂 Datasets Used

## 🎬 MovieLens 1M

### Used for:
- Sequential recommendation
- User-item interaction modeling

### Contains:
- 1M+ ratings
- 6000+ users
- 3900+ movies

### Dataset Source:
```bash
https://grouplens.org/datasets/movielens/1m/
```

---

## 🌐 Douban Dataset

### Used for:
- Social relationship modeling
- Social embeddings

### Contains:
- User friendships
- Ratings
- Social interactions

### Dataset Source:
```bash
https://www.kaggle.com/datasets/fengzhujoey/douban-datasetratingreviewside-information
```

---

# ⚙️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core implementation |
| PyTorch | Deep learning framework |
| NumPy | Numerical operations |
| Pandas | Data preprocessing |
| NetworkX | Social graph processing |
| Matplotlib | Visualization |
| Scikit-learn | Evaluation utilities |

---

# 🔄 Workflow

## 1️⃣ Data Preprocessing

- Cleaning interaction logs
- Timestamp conversion
- Sorting user interactions
- Session construction

---

## 2️⃣ Sequential Modeling

Transformer Encoder captures:

- Long-term dependencies
- User preference evolution
- Contextual relationships

---

## 3️⃣ Session Modeling

GRU-based session encoder captures:

- Recent activity
- Short-term intent
- Dynamic session patterns

---

## 4️⃣ Social Embedding Generation

Social graphs are constructed from Douban data using NetworkX.

Normalized node degree embeddings are generated to represent:

- User influence
- Trust relationships
- Social similarity

---

## 5️⃣ Fusion Layer

Sequential + Session + Social representations are combined using:

- Multi-Layer Perceptron (MLP)

---

# 📊 Evaluation Metrics

The model is evaluated using:

## 🔹 Recall@10
Measures retrieval quality.

## 🔹 NDCG@10
Measures ranking quality.

## 🔹 Precision@10
Measures relevance among recommended items.

---

# 📈 Results

| Model | Recall@10 | NDCG@10 | Precision@10 | Accuracy |
|---|---|---|---|---|
| Sequential Transformer | 0.2854 | 0.1732 | 0.0284 | 0.418 |
| Social-aware Transformer | **0.3291** | **0.1958** | **0.0332** | **0.457** |

---

# 🚀 Improvements Achieved

- Recall@10 improved by **15.3%**
- NDCG@10 improved by **13.1%**

These results demonstrate that incorporating social influence significantly improves recommendation performance.

---

# 🎯 Research Contributions

✅ Unified framework combining:

- Sequential recommendation
- Session recommendation
- Social recommendation

✅ Improved ranking quality using social context

✅ Enhanced personalization using Transformer architectures

✅ Context-aware recommendation generation

---

# 🔮 Future Scope

Possible future enhancements include:

- Cross-domain recommendation systems
- Richer social graph embeddings
- Temporal social dynamics
- Large-scale distributed training
- Real-time recommendation pipelines

---

# 📄 Research Paper

## Title:
**Enhancing Social Recommendation through Sequential and Session Modeling with Transformers**

## Presented at:
**DoSCI-2026 — 7th Doctoral Symposium on Computational Intelligence**

---

# 👩‍💻 Authors

- **Jyoti Shokeen**
- **Jahnvee Srivastava**
- **Dodda Sai Manisri**

**Indira Gandhi Delhi Technical University for Women (IGDTUW)**

---

# ⭐ Acknowledgements

We sincerely thank our mentors, faculty members, and peers for their guidance and support throughout this research work.

---

# 📬 Connect

If you found this project interesting, feel free to:

- ⭐ Star the repository
- 🍴 Fork the project
- 🤝 Connect and collaborate

---
