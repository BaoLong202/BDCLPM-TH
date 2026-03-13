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


# PHÂN TÍCH HỆ THỐNG PARABANK

**Website:** https://parabank.parasoft.com/parabank/index.htm  
**Tuần 7 – Tìm hiểu hệ thống**

---

## 1. Tổng quan hệ thống

Parabank là website demo ngân hàng trực tuyến, dùng để thực hành automation test. Hệ thống cung cấp các chức năng cơ bản của ngân hàng online: đăng ký, đăng nhập, xem tài khoản, chuyển tiền, thanh toán hóa đơn, v.v.

---

## 2. Các module chính

| STT | Module | Mô tả ngắn | URL/Trang |
|-----|--------|------------|-----------|
| 1 | **User Registration** | Đăng ký tài khoản mới (username, password, thông tin cá nhân) | Register |
| 2 | **Login / Logout** | Đăng nhập và đăng xuất vào hệ thống | Index (Home) |
| 3 | **Account Overview** | Xem tổng quan các tài khoản, số dư | Accounts Overview |
| 4 | **Open New Account** | Mở tài khoản mới (Checking/Savings) | Open New Account |
| 5 | **Transfer Funds** | Chuyển tiền giữa các tài khoản | Transfer Funds |
| 6 | **Bill Pay** | Thanh toán hóa đơn (payee, số tiền, tài khoản trừ) | Bill Pay |
| 7 | **Find Transactions** | Tìm kiếm giao dịch theo tiêu chí | Find Transactions |
| 8 | **Update Contact Info** | Cập nhật thông tin liên hệ (địa chỉ, SĐT) | Update Profile |
| 9 | **Request Loan** | Yêu cầu vay vốn (số tiền, khoản thanh toán) | Request Loan |

---

## 3. Luồng nghiệp vụ chính

1. **Đăng ký** → **Đăng nhập** → **Xem tài khoản**
2. **Mở tài khoản mới** (nếu cần)
3. **Chuyển tiền** / **Bill Pay** / **Request Loan**
4. **Find Transactions** để kiểm tra lịch sử
5. **Update Contact Info** khi cần thay đổi thông tin
6. **Logout** khi kết thúc

---

## 4. Đối tượng test (Elements thường gặp)

- **Links:** Đăng ký, Đăng xuất, các menu điều hướng
- **Textbox:** Username, Password, số tiền, thông tin payee, tìm kiếm
- **Buttons:** Login, Submit, Send Payment, v.v.
- **Dropdown:** Loại tài khoản, tài khoản nguồn/đích
- **Bảng:** Danh sách tài khoản, giao dịch
- **Thông báo:** Thành công (Welcome), lỗi (Invalid username/password)

---

# TIẾN ĐỘ TUẦN 7 – Tìm hiểu hệ thống + Thiết kế test

**Ngày thực hiện:** …………………  
**Nhóm:** …………………

---

## Công việc đã hoàn thành

### 1. Tìm hiểu hệ thống
- Phân tích website Parabank (https://parabank.parasoft.com/parabank/index.htm).
- Xác định **9 module chính:** User Registration, Login/Logout, Account Overview, Open New Account, Transfer Funds, Bill Pay, Find Transactions, Update Contact Info, Request Loan.
- Tài liệu: `01_Phan_tich_he_thong_Parabank.md`.

### 2. Thiết kế test
- **Test Plan:** Phạm vi test, danh sách modules, chiến lược test (Smoke, GUI, Functional).  
  → File: `02_Test_Plan.md`
- **Test Scenarios:** 40 test scenarios cho các chức năng quan trọng, bao gồm:
  - Smoke Test (Login, Logout, Transfer Funds).
  - GUI Test (button, textbox, link, thông báo lỗi, hiển thị element).
  - Functional Test (Register, Bill Pay, Open New Account, Find Transactions, Update Contact Info, Request Loan).
  - File: `03_Test_Scenarios.csv` (mở bằng Excel).

---

## Sản phẩm nộp (cuối tuần 7)

| File | Mô tả |
|------|--------|
| 01_Phan_tich_he_thong_Parabank.md | Phân tích hệ thống – các module |
| 02_Test_Plan.md | Test Plan (có thể copy sang Word 1–2 trang) |
| 03_Test_Scenarios.csv | 40 test scenarios (mở bằng Excel) |
| 04_Tien_do_Tuan_7.md | Báo cáo tiến độ tuần 7 |

---

## Ghi chú

- File `.md` có thể mở bằng Notepad/VSCode hoặc chuyển sang Word.
- File `03_Test_Scenarios.csv` mở bằng Excel để chỉnh sửa/nộp.
- Tuần 8: Xây dựng framework automation (Selenium, POM, C#, NUnit).

-Word: https://sthuflitedu-my.sharepoint.com/:w:/g/personal/23dh111935_st_huflit_edu_vn/IQB2MEQNi1I8TZPEjzHTRCnQAbR8g7Enibwdbolh0UbqK2w?e=scQdOd

-Excel: https://sthuflitedu-my.sharepoint.com/:x:/g/personal/23dh111935_st_huflit_edu_vn/IQDsXeaOpv5xQpTNCtQA_bF6AaDkB08FU40B3rWk3qdBgPs?e=iDBeho



