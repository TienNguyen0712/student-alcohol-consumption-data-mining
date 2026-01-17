![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Academic%20Project-orange)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-ML-yellow)

# 👨‍🎓 Student Alcohol Consumption - Data Mining Project

## 📌 Giới thiệu
Trong bối cảnh thế hệ trẻ đang ngày càng có vai trò quan trọng trong sự phát triển tương lai, việc dự đoán điểm số dựa trên các đặc trưng đóng vai trò quan trọng giúp nhận biết được:
- Yếu tố nào ảnh hưởng đến điểm số ?
- Có bao nhiêu nhóm học sinh được chia dựa theo năng lực ?
- Dự đoán điểm số dựa trên các mô hình học máy hay không ?  
- Các nhóm học sinh này có đặc điểm gì ?

Đề tài này áp dụng **quy trình Khai phá dữ liệu (Data Mining)** để khám phá tri thức tiềm ẩn từ **Student Alcohol Consumption dataset**

---

## 🎯 Mục tiêu & Câu hỏi nghiên cứu

### Mục tiêu
- Áp dụng toàn bộ pipeline Khai phá dữ liệu:  
  **Tiền xử lý → Phân tích mô tả → Mô hình hóa → Đánh giá → Insight**
- Thực nghiệm và so sánh nhiều thuật toán học máy (Phân loại - Phân cụm)
- Rút ra insight có ý nghĩa cho bài toán điểm số học sinh

### Câu hỏi nghiên cứu
1. Các **yếu tố** nào ảnh hưởng tiêu cực đến điểm số học sinh ? 
2. Có thể **phân cụm** thành các nhóm học sinh dựa theo đặc điểm hay không ?
3. Các nhóm học sinh có những yếu tố nào thì có thể phân chúng về một nhóm  ?
4. Ta có thể **phân loại** điểm số của những học sinh dược không ?

---

## 📂 Dataset

- **Tên:** Student Alcohol Consumption 
- **Nguồn:** Public dataset ([Kaggle – dữ liệu nghiên cứu học thuật](https://www.kaggle.com/datasets/uciml/student-alcohol-consumption))
- **Số dòng:** ~
- **Số cột:** 
- **Đối tượng:** Điểm só của những học sinh cấp hai của lớp **Toán** và **Tiếng Bồ Đào Nha**
### Một số thuộc tính quan trọng
- **Thông tin cá nhân:** `sex`, `age`, `address`, `famsize`, `Pstatus`, `Medu`, `Fedu`, `Mjob`, `Fjob`
- **Thông tin học tập:** `school`, `reason`, `guardian`
- **Thông tin thời gian:** `traveltime`, `studytime`, `failures`
- **Thông tin tài chính:** `schoolsup`, `famsup`, `paid`
- **Thông tin sinh hoạt:** `activities`, `nursery`, `higher`, `internet`, `romantic` 
- **Thông tin sức khỏe tinh thần:** `famrel`, `freetime`, `goout`, `Dalc`, `Walc`, `health`, `absences`
- **Thông tin điểm số:** `G1`, `G2`, `G3`

---

## 🧪 Quy trình Khai phá dữ liệu

### 1️⃣ Tiền xử lý dữ liệu ✔️
- Bộ dữ liệu gồm 2 bảng **Toán** và **Tiếng Bồ Đào Nha**
- Bộ dữ liệu không có dữ liệu thiếu hay trùng
- Thực hiện gộp 2 bảng lại tạo bảng mới phục vụ quá trình huán luyện mô hình
- Loại bỏ các giá trị không hợp lệ 
- Loại bỏ các đặc trưng không hợp lệ

### 2️⃣ Phân tích mô tả (EDA) ✖️

### 3️⃣ Huấn luyện mô hình ✖️

### 4️⃣ Đánh giá mô hình ✖️

### 5️⃣ Rút ra insight - ý nghĩa ✖️

---

## 🤖 Các kỹ thuật Khai phá dữ liệu được sử dụng

### 🔹 Phân lớp (Classification)
**Mục tiêu:** Dự đoán khách có hủy booking hay không  
**Thuật toán:**
- Logistic Regression
- KNN
- SVM
- Random Forest
- XGBoost

**Đánh giá:**
- Accuracy
- Precision / Recall
- F1-score
- Confusion Matrix

---

### 🔹 Phân cụm (Clustering)
**Mục tiêu:** Phân khúc khách hàng đặt phòng  

**Thuật toán:**
- K-Means
- Hierarchical Clustering
- DBSCAN 

**Đánh giá:**
- Elbow Method
- Silhouette Score

---

## 📊 Kết quả & Insight chính


---

## 🗂️ Cấu trúc thư mục
```text
student-alcohol-consumption-data-mining/
│
├── README.md
│
├── configs/
│   ├── base.yaml
│   ├── classification.yaml  # Định nghĩa các cáu trúc phân loại 
│   └── clustering.yaml      # Định nghĩa các cấu trúc phân cụm  
|
├── data/
│   ├── raw/
│   │   ├── student_mat.csv  # Học sinh lớp Toán 
│   │   └── student_por.csv  # Học ính lớp Tiếng Bồ
│   └── processed/ 
|       ├── student_mat_classification.csv # Bộ dữ liệu sử dụng cho phân loại (Toán)
|       ├── student_mat_clustering.csv     # Bộ dữ liệu sử dụng cho phân cụm (Toán)
|       ├── student_por_classification.csv # Bộ dữ liệu sử dụng cho phân loại (Bồ)
│       └── student_por_clustering.csv     # Bộ dữ liệu sử dụng cho phân cụm (Bồ)
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_eda.ipynb
│   ├── 04_classification.ipynb
│   └── 05_clustering.ipynb
│
├── reports/
│   ├── Report.pdf
│   └── Poster.pdf
|
├── requirements.txt
└── .gitignore
```

---

## 🚀 Công nghệ & Thư viện
- Python 3.12
- pandas, numpy
- matplotlib, seaborn
- scikit-learn

---

## ⚠️ Hạn chế & Hướng mở rộng


---

## 👨‍🎓 Thông tin học thuật
- Sản phẩm là **bài làm gốc**
- Các tài liệu, thư viện được trích dẫn rõ ràng
- Tác giả: **Nguyễn Đăng Tiến**

---

## 📎 Tài liệu tham khảo
- *P. Cortez and A. Silva. Using Data Mining to Predict Secondary School Student Performance*
- Kaggle: Student Alcohol Consumption Dataset
