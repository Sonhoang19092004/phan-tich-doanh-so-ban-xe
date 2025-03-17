# Dự án Phân tích Doanh thu Bán hàng với Spark & Machine Learning

## 1. Giới thiệu
Dự án này phân tích doanh thu bán hàng bằng R, Spark, và các thuật toán Machine Learning (Decision Tree, XGBoost, ARIMA). Dữ liệu bỏ trống được xử lý và chuyển đổi trên Spark trước khi trực quan hóa.

## 2. Cài đặt
Yêu cầu: R đã cài đặt, Spark, và các gói sau:

Chạy lệnh sau để cài đặt:
```r
install.packages("sparklyr")
install.packages("dplyr")
install.packages("ggplot2")
install.packages("forecast")
install.packages("rpart")
install.packages("rpart.plot")
install.packages("xgboost")
install.packages("Matrix")
```

Sau đó, thiết lập Spark:
```r
library(sparklyr)
sc <- spark_connect(master = "local")
Sys.setenv(SPARK_HOME = "C:/spark-3.5.4-bin-hadoop3")
sc <- spark_connect(master = "local", spark_home = Sys.getenv("SPARK_HOME"))
```

## 3. Cách sử dụng
1. **Tải dữ liệu**: Dữ liệu có định dạng CSV và nằm trong thư mục `F:/Big_Data/BTL_Big_Data/Sales.csv/`.
2. **Chạy file R**: Nạp và xử lý dữ liệu, trực quan hóa.
3. **Huấn luyện mô hình ML**: Decision Tree, XGBoost, ARIMA.
4. **Dự báo doanh thu**: Dành cho các năm 2025-2028.

## 4. Kết quả
- **Tổng doanh thu theo năm**: Biểu đồ xu hướng doanh thu.
- **Top 10 sản phẩm doanh thu cao nhất**: Biểu đồ cột.
- **Top 10 sản phẩm bán chạy nhất**: Biểu đồ cột.
- **Dự báo doanh thu**: Decision Tree, XGBoost, ARIMA.

## 5. Ngắt kết nối Spark
Sau khi chạy xong, ngắt kết nối:
```r
spark_disconnect(sc)
```

## 6. Liên hệ
Nếu bạn có bất kỳ câu hỏi nào, vui lòng liên hệ qua email hoặc GitHub Issues!

