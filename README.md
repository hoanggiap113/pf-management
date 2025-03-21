# 📊 Personal Finance Data Warehouse  

## 📖 Giới thiệu  
Dự án này xây dựng một **Data Warehouse** hỗ trợ **quản lý tài chính cá nhân**, giúp theo dõi **thu nhập, chi tiêu, khoản vay, đầu tư** và phân tích dòng tiền hiệu quả.  

🚀 **Tính năng chính:**  
✅ Theo dõi **thu nhập & chi tiêu** theo danh mục.  
✅ Quản lý **các khoản vay, lãi suất, thời gian trả nợ**.  
✅ Giám sát **khoản đầu tư, lợi nhuận kỳ vọng**.  
✅ Phân tích dữ liệu tài chính theo **năm, quý, tháng, tuần**.  
✅ Hỗ trợ tích hợp với **Power BI, Tableau** để tạo báo cáo trực quan.  

---

## 📂 Cấu trúc Database  
Dự án sử dụng mô hình **Star Schema** để tối ưu hóa hiệu suất truy vấn.  

### 🔹 1. Bảng Dimension (Mô tả dữ liệu)  
| Bảng                  | Chức năng |
|----------------------|------------------------------------------------|
| `DIM_USERS` | Lưu thông tin người dùng |
| `DIM_ACCOUNTS` | Lưu thông tin tài khoản ngân hàng, ví, thẻ tín dụng |
| `DIM_TIME` | Quản lý thời gian (ngày, tháng, năm, quý, tuần) |
| `DIM_TRANSACTION_TYPES` | Phân loại giao dịch: Thu nhập, Chi tiêu, Vay, Đầu tư |
| `DIM_INCOME_CATEGORY` | Danh mục thu nhập (Lương, Kinh doanh, Đầu tư...) |
| `DIM_EXPENSE_CATEGORY` | Danh mục chi tiêu (Ăn uống, Giải trí, Mua sắm...) |
| `DIM_LOAN_TYPES` | Loại khoản vay (Vay tín dụng, Vay thế chấp...) |
| `DIM_INVESTMENT_TYPES` | Loại hình đầu tư (Cổ phiếu, Crypto, Bất động sản...) |

### 🔹 2. Bảng Fact (Dữ liệu chính)  
| Bảng                   | Chức năng |
|----------------------|------------------------------------------------|
| `FACT_TRANSACTIONS` | Lưu tất cả các giao dịch tài chính cá nhân |
| `FACT_INCOME` | Ghi nhận chi tiết các khoản thu nhập |
| `FACT_EXPENSES` | Ghi nhận chi tiết các khoản chi tiêu |
| `FACT_LOANS` | Quản lý khoản vay, lãi suất, ngày trả nợ |
| `FACT_INVESTMENTS` | Theo dõi các khoản đầu tư & lợi nhuận kỳ vọng |

---

## 🛠 Cách cài đặt  

### 📌 Yêu cầu hệ thống  
- **MySQL 8.0+**  
- **MySQL Workbench** hoặc **CLI MySQL**  

### 📌 Cài đặt Database  
1️⃣ **Clone repo hoặc tải file SQL**  
```sh
git clone https://github.com/your-repo/financial-dw.git
cd financial-dw
