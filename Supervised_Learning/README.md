## 1) Linear Regression

**Hồi quy tuyến tính:** Là thuật toán **học có giám sát (supervised learning)** cơ bản nhất, trong đó mối quan hệ giữa đầu vào và đầu ra được mô tả bởi một **hàm tuyến tính**. Nó còn được gọi là linear fitting hoặc linear least square. Mục tiêu là tìm một hàm `f: R^d → R` để **dự đoán một giá trị số liên tục** đầu ra dựa trên vector đặc trưng đầu vào.

**Phù hợp với loại dữ liệu gì:** Phù hợp với các bài toán **hồi quy (regression)**, **nhãn** đầu ra là các giá trị thực (có thể vô hạn).

**Toán học:** Mối quan hệ giữa đầu ra `y` và đầu vào `x` được mô hình bởi `y ≈ ŷ = f(x) = w^T x` hoặc `y ≈ w1 x1 + w2 x2 + w3 x3`. Trong đó `w` là vector hệ số (hoặc trọng số) cần tìm.

**Hàm mất mát (Loss Function):** Thường sử dụng **sai số bình phương trung bình (Mean Squared Error - MSE)**.

**Phương pháp tối ưu:** gradient descent, pseudo inverse (giả nghịch đảo).

**Bias trick:** Kỹ thuật thêm một đặc trưng bằng 1 vào vector đặc trưng để gộp bias `b` vào vector hệ số `w`, giúp đơn giản hóa biểu thức toán học.

**Ưu điểm:**
- Đơn giản, dễ hình dung và tính toán
- Overfitting có thể giảm bằng regularization.
- Hiệu suất tốt khi bộ dữ liệu có thể tách rời tuyến tính.

**Nhược điểm:**
- Dữ liệu độc lập, điều hiếm thấy trong cuộc sống thực.
- Dễ bị noise and overfitting.
- Nhạy cảm với các ngoại lệ.

**Cải tiến:**
- **Tiền xử lý (pre-processing) để loại bỏ nhiễu** trước khi thực hiện.
- Sử dụng **Huber loss** thay cho MSE để mô hình ít bị ảnh hưởng bởi nhiễu (Huber regression).
- **Hồi quy đa thức (Polynomial regression):** Áp dụng linear regression cho các quan hệ phi tuyến bằng cách tạo ra các vector đặc trưng mới có dạng `[1, x1, x1^2, ...]`.
- **Ridge regression:** Bổ sung thêm một số hạng regularization `λ||w||^2_2` vào hàm mất mát. Kỹ thuật này giúp phương trình đạo hàm bằng 0 có nghiệm duy nhất khi `X X^T` không khả nghịch, và còn giúp **tránh overfitting**.
- **Gradient descent:** Sử dụng để tối ưu hàm mất mát khi kích thước ma trận `X X^T` lớn, tránh việc tính ma trận nghịch đảo tốn kém.
