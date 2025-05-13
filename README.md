# 🏆 CS:GO Round Winner Prediction

This project aims to predict the **winner of a CS:GO round** using **in-game snapshot data** with machine learning models.

---

## 📁 Dataset

- **Source**: Loaded from Google Drive:  
  `csgo_round_snapshots.csv`  
- **Total Rows**: ~122,410  
- **Columns**: 97 features including:
  - Player health, armor, money, weapons, and grenades
  - Map info, bomb planted or not
  - Number of players alive
  - Target variable: `round_winner` (Terrorist or Counter-Terrorist)

---

## 🔧 Data Preprocessing

- Removed **duplicates**: `df.drop_duplicates(inplace=True)`
- Verified **no null values**
- Converted categorical columns (`map`, `bomb_planted`, `round_winner`) using `LabelEncoder`

---

## 🔍 Feature & Target Split

python
X = df.iloc[:,:-1]       # All columns except round_winner
y = df['round_winner']   # Target column

