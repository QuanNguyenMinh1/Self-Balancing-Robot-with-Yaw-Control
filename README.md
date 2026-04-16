# Self-Balancing-Robot-with-Yaw-Control

[![Platform](https://img.shields.io/badge/MCU-STM32--Bare--Metal-blue?style=flat-square&logo=stmicroelectronics)](https://www.st.com/)
[![Control](https://img.shields.io/badge/Control-Double--Loop_PID-red?style=flat-square)]()
[![Yaw](https://img.shields.io/badge/Feature-Yaw_Setpoint_Recovery-green?style=flat-square)]()

## 📌 Overview
Dự án phát triển robot con lắc ngược hai bánh (TWIP) trên nền tảng **STM32 (Bare-metal)**. Điểm nhấn kỹ thuật của dự án là khả năng kiểm soát hướng (**Yaw Control**) kết hợp với hệ thống cân bằng, giúp robot duy trì và tự động quay về hướng chỉ định (`yaw_setpoint`) sau khi chịu tác động ngoại lực hoặc thực hiện các lệnh quay 90 độ chính xác.

## 🚀 Technical Highlights
* **Double-Loop PID Control:** * **Inner Loop (Velocity):** Kiểm soát góc nghiêng ở tần số cao để duy trì sự cân bằng động.
    * **Outer Loop (Yaw):** Kiểm soát tốc độ và vị trí, giữ robot đứng yên hoặc di chuyển ổn định.
* **Independent Yaw Management:** * Triệt tiêu hiện tượng trôi hướng (drift) đặc trưng của cảm biến IMU.
    * Thuật toán **Yaw Setpoint Recovery** giúp robot khóa mục tiêu hướng và tự quay lại vị trí ban đầu nếu bị tác động quay.
* **Sensor Fusion:** Sử dụng bộ lọc (**Kalman Filter**) để kết hợp dữ liệu từ **MPU6050** và **Encoder**, đảm bảo ước lượng trạng thái robot chính xác và phản hồi nhanh.
* **Firmware Bare-metal:** Phát triển trực tiếp trên thanh ghi (registers), tối ưu hóa Timer-driven Interrupts để đảm bảo tính thời gian thực (Real-time) tuyệt đối cho các vòng lặp điều khiển.

## 🛠 Hardware Stack
* **Microcontroller:** STM32 (ARM Cortex-M core).
* **Sensors:** MPU6050 (6-axis Accelerometer & Gyroscope), Hall-effect Encoders.
* **Actuators:** DC Geared Motors với điều khiển xung PWM.
* **Communication:** UART for debugging and telemetry.

## ✍️ Author
**Nguyễn Minh Quân**
* Sinh viên năm 3 - Chương trình PFIEV (Kỹ sư chất lượng cao).
* Trường Đại học Bách Khoa - ĐHQG TP.HCM.
* Chuyên ngành: Điện tử - Viễn thông.
