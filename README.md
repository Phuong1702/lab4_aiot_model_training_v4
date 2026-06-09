# LAB 4 - AIoT Forecasting & Predictive Analytics

## Giới thiệu

Dự án **LAB 4** thuộc học phần Triển khai, phát triển ứng dụng AI và IoT.
Bài lab tập trung vào xây dựng mô hình AI để dự báo dữ liệu IoT, đánh giá sai số và triển khai mô hình dự báo bằng FastAPI.

## Mục tiêu

* Xử lý dữ liệu cảm biến IoT dạng time-series.
* Huấn luyện mô hình dự báo dữ liệu.
* Đánh giá mô hình bằng các chỉ số như MAE, RMSE.
* So sánh kết quả dự báo với dữ liệu thực tế.
* Lưu model và kết quả dự đoán.
* Triển khai API dự báo bằng FastAPI.

## Công nghệ sử dụng

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* FastAPI
* Uvicorn
* Joblib
* Jupyter Notebook

## Cấu trúc thư mục

```text
LAB4/
├── data/
├── figures/
├── models/
├── notebooks/
├── outputs/
├── src/
├── requirements.txt
└── README.md
```

## Cài đặt

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

## Chạy chương trình

### Chuẩn bị dữ liệu

```bash
python src/download_data.py
```

### Train model

```bash
python src/train_forecast.py
```

Hoặc chạy toàn bộ pipeline nếu project có file `run_all.py`:

```bash
python src/run_all.py
```

### Vẽ biểu đồ kết quả

```bash
python src/plot_results.py
```

## Chạy API

```bash
uvicorn src.app:app --reload
```

Mở trình duyệt:

```text
http://127.0.0.1:8000/docs
```

## Kết quả đầu ra

Sau khi chạy project, các kết quả được lưu trong:

```text
models/
outputs/
figures/
```
Bao gồm:

* Model dự báo đã huấn luyện.
* File kết quả dự đoán.
* File đánh giá sai số.
* Biểu đồ so sánh dữ liệu thực tế và dữ liệu dự báo.

