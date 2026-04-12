# PM25_NMKHDL
 DỰ BÁO PM2.5 TẠI HÀ NỘI – PHIÊN BẢN DỮ LIỆU THỰC
 Nguồn: Open-Meteo Air Quality API (10/2022 – 02/2026)
============================================================

CÀI ĐẶT:
  pip install -r requirements.txt

CHUẨN BỊ DỮ LIỆU:
  Đặt file "air_quality_historical.csv" vào cùng thư mục với notebook.

CHẠY:
  jupyter notebook PM25_HaNoi_RealData.ipynb

LƯU Ý QUAN TRỌNG:
  - KHÔNG đưa us_aqi / european_aqi vào features (Data Leakage!)
  - Chia train/test theo thứ tự thời gian

CẤU TRÚC NOTEBOOK:
  1. Import thư viện
  2. Tải dữ liệu thực (CSV)
  3. Tiền xử lý + Feature Engineering (lag ngày, rolling, sin/cos)
  4. EDA: chuỗi thời gian, boxplot theo tháng, heatmap tương quan
  5. Chia train/test (80/20, theo thời gian)
  6. Huấn luyện 4 mô hình: LR, RF, XGBoost, LightGBM
  7. Đánh giá: MAE, RMSE, R² + biểu đồ
  8. Phân tích sai số (Error Analysis)
