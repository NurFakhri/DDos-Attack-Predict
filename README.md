# 🔐 DDoS Attack Prediction using Machine Learning

This project aims to detect potential Distributed Denial of Service (DDoS) attacks using machine learning techniques on historical network traffic data. It explores multiple models and compares performance across different feature subsets.

---

## 📂 Project Structure

- `ddos_model.ipynb`: Main notebook containing EDA, preprocessing, training, and evaluation
- `data/`: All dataset (unprocessed, preprocessed)
- `images/`: Visuals and results from model
---

## 🚀 Models Used

We implemented and compared the following classification models:

- **Random Forest**  
- **XGBoost**  
- **TabNet**

Each model was trained on:
- Full feature set  
- Top 6 highly correlated features  
- 6 least correlated features  

Data was split into **80% train, 10% validation, 10% test**.

---

## 📈 Results Summary

| Model         | Full Features | High Correlation Only | Low Correlation Only |
|---------------|----------------|------------------------|------------------------|
| Random Forest | 100%           | 99%                    | 75%                    |
| XGBoost       | 99%            | 98%                    | 74%                    |
| TabNet        | 97%            | 92%                    | 72%                    |

> Strongly correlated features proved nearly as effective as using the full dataset. Low-correlated features performed poorly, highlighting the importance of feature selection.

---

## 💡 Key Features Used

- `bytecount`  
- `pktcount`  
- `byteperflow`  
- `pktperflow`  
- `pktrate`  
- `tot_dur`

---

## 🧠 Future Work

- **Real-time implementation** using live traffic streams  
- **Automated alert system** for suspicious behavior  
- **Explainability with SHAP/TabNet attention** to interpret model decisions  
- **Scalability testing** on larger datasets or multiple network sources

---

## 📬 Contact

For questions or collaboration, feel free to reach out:

- **Name**: Muhammad Hadi Nur Fakhri  
- **LinkedIn**: linkedin.com/in/nur-fakhri/  

---

## 📄 License

This project is open-source
