# TEST PLAN – PARABANK AUTOMATION

**Dự án:** Selenium Automation Testing với Parabank  
**Phạm vi:** Tuần 7 – Thiết kế test

---

## 1. Phạm vi test (Scope)

- **Ứng dụng:** Parabank – https://parabank.parasoft.com/parabank/index.htm  
- **Phạm vi chức năng:** Toàn bộ 9 module chính (Registration, Login/Logout, Account Overview, Open New Account, Transfer Funds, Bill Pay, Find Transactions, Update Contact Info, Request Loan).  
- **Loại test:** Functional, GUI, Smoke.  
- **Ngoài phạm vi:** Performance, Security, API (chỉ tập trung UI với Selenium).

---

## 2. Modules cần test

| Module | Ưu tiên | Ghi chú |
|--------|---------|--------|
| Login / Logout | Cao | Smoke test bắt buộc |
| User Registration | Cao | Dữ liệu test cần chuẩn bị |
| Account Overview | Cao | Kiểm tra hiển thị số dư, danh sách tài khoản |
| Transfer Funds | Cao | Smoke test |
| Open New Account | Trung bình | Checking/Savings |
| Bill Pay | Trung bình | Payee, amount, account |
| Find Transactions | Trung bình | Filter theo ngày, ID, loại |
| Update Contact Info | Trung bình | Address, phone |
| Request Loan | Trung bình | Amount, down payment |

---

## 3. Chiến lược test (Strategy)

- **Smoke Test:** Chạy trước mỗi lần test đầy đủ (Login thành công, Logout, Transfer funds thành công).  
- **GUI Test:** Kiểm tra nút bấm, ô nhập, link, thông báo lỗi, hiển thị/ẩn element.  
- **Functional Test:** Mỗi chức năng có test case positive và negative (dữ liệu hợp lệ/không hợp lệ).  
- **Test Data:** Lưu trong JSON/CSV (username, password, account number, transfer amount, payee).  
- **Công nghệ:** Selenium WebDriver, C#, NUnit, Page Object Model (POM).

---

## 4. Tiêu chí hoàn thành

- Tối thiểu **30–40 test scenarios** (theo yêu cầu nhóm 3–4 SV).  
- Mỗi SV xây dựng tối thiểu **5 automation tests**.  
- Test scenarios phủ đủ các chức năng quan trọng và có bảng Test Scenarios đính kèm.

---

*Tài liệu này có thể copy sang Word, giữ khoảng 1–2 trang khi nộp.*
