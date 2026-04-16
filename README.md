# Self-Balancing-Robot-with-Yaw-Control
---
## Demo
### Turning 90 degrees
<video src="https://github.com/user-attachments/assets/d384eeeb-b339-4759-9bde-05d9948f5932" width="100%" controls>
</video>

### Self-balancing
<video src="https://github.com/user-attachments/assets/24c727ca-0a64-4b7e-a9e8-a64cf511929f" width="100%" controls>
</video>
---



## 📌 Overview
Điểm nhấn kỹ thuật của dự án là khả năng kiểm soát hướng (**Yaw Control**) kết hợp với hệ thống cân bằng, giúp robot duy trì và tự động quay về hướng chỉ định (`yaw_setpoint`) sau khi chịu tác động ngoại lực hoặc thực hiện các lệnh quay 90 độ chính xác.

## 🚀 Technical Highlights
* **Double-Loop PID Control:** * **Inner Loop (Velocity):** Kiểm soát góc nghiêng ở tần số cao để duy trì sự cân bằng động.
    * **Outer Loop (Yaw):** Kiểm soát tốc độ và vị trí, giữ robot đứng yên hoặc di chuyển ổn định.
* **Independent Yaw Management:** * Triệt tiêu hiện tượng trôi hướng (drift) đặc trưng của cảm biến IMU.
    * Thuật toán **Yaw Setpoint Recovery** giúp robot khóa mục tiêu hướng và tự quay lại vị trí ban đầu nếu bị tác động quay.
* **Sensor Fusion:** Sử dụng bộ lọc (**Kalman Filter**) để kết hợp dữ liệu từ **MPU6050** và **Encoder**, đảm bảo ước lượng trạng thái robot chính xác và phản hồi nhanh.

## 🛠 Hardware Stack
* **Microcontroller:** STM32F103C8T6 (ARM Cortex-M core).
* **Sensors:** MPU6050 (6-axis Accelerometer & Gyroscope), Encoder quang.
* **Actuators:** DC Geared Motors với điều khiển xung PWM.
* **Communication:** UART for debugging and telemetry.

## ✍️ Author
**Nguyễn Minh Quân**
* Sinh viên năm 3 - Chương trình PFIEV (Kỹ sư chất lượng cao).
* Trường Đại học Bách Khoa - ĐHQG TP.HCM.
* Chuyên ngành: Điện tử - Viễn thông.
