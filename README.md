# Lab 1 - Nhập môn kiểm thử tự động & Thiết lập môi trường

- Sinh viên: Nguyễn Quốc Tuấn - Mã SV: TB02181
- Môn: SOF3091

## Cách chạy project
1. Cài .NET SDK và Google Chrome.
2. Clone repo:
   ```
   git clone https://github.com/darkgrial/Lab1-SOF3091-TB02181.git
   ```
3. Chạy test:
   ```
   cd Lab1-SOF3091-TB02181/FirstTest
   dotnet test --logger "console;verbosity=detailed"
   ```
4. Chrome sẽ tự mở trang example.com, test đọc tiêu đề và kiểm tra bằng Assert, kết quả hiển thị **Passed**.

## Minh chứng (thư mục screenshots/)
| Nội dung | Ảnh |
|---|---|
| dotnet --version | screenshots/01_dotnet_version.png |
| dotnet --info | screenshots/02_dotnet_info.png |
| File .csproj có Selenium.WebDriver | screenshots/03_csproj.png |
| Test Passed | screenshots/04_test_passed.png |
| Lịch sử commit | screenshots/05_git_log.png |
| Trang repo GitHub | screenshots/06_github_repo.png |
| Hỏi đáp với AI | screenshots/07_ai_prompt.png |

## Phần D - Trải nghiệm dùng AI
**Tình huống:** Sau khi dán code test vào Visual Studio, file bị 4 lỗi gạch đỏ ở `OpenQA`, `IWebDriver`, `ChromeDriver`.

**Prompt đã dùng:** "Khúc này sao lỗi nhiều vậy?" (kèm ảnh chụp màn hình code).

**Câu trả lời của AI:** Lỗi do project chưa có gói Selenium.WebDriver, hướng dẫn cài qua NuGet (Manage NuGet Packages) rồi Rebuild. Ảnh: `screenshots/07_ai_prompt.png`.

**Nhận xét:** AI giúp mình tìm ra nguyên nhân rất nhanh, chỉ cần gửi ảnh chụp màn hình là biết cả 4 lỗi cùng do thiếu một gói thư viện, và có các bước cài đặt cụ thể. Tuy nhiên, hướng dẫn của AI có vài chỗ không khớp với máy mình, ví dụ code mẫu dùng `namespace FirstTests` trong khi project của mình tên `FirstTest`, và Visual Studio của mình tạo file `.slnx` thay vì `.sln`. Vì vậy mình phải tự đối chiếu với màn hình thực tế trước khi làm theo. Sau khi cài gói Selenium, lỗi biến mất và test chạy Passed.