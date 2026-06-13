# **BÁO CÁO TIẾN ĐỘ KHÓA GIT FOUNDATIONS**
## **1. Thông tin học viên & Dự án**
* Khóa học: Git Foundations (Microsoft Learn - GitHub Foundations)
* Học viên: Nguyễn Đắc Nhật Quang
* Tên kho lưu trữ (Repository): github-practice
## **2. Quá trình học tập**
Được chia làm 2 giai đoạn chính dựa theo tài liệu Microsoft Learn:
* Giai đoạn 1 (Cơ bản): Tiếp cận các khái niệm cốt lõi của Git bao gồm quản lý mã nguồn cục bộ, làm việc với hệ thống lưu trữ đám mây GitHub, tìm hiểu cách hoạt động của mô hình GitHub Flow (Branching, Committing, Pull Request).
* Giai đoạn 2 (Cộng tác nâng cao): Học cách quản lý, phân quyền và bảo mật dự án. Thực hành các tình huống thực tế phức tạp như giải quyết xung đột mã nguồn (Conflict), quản lý lịch sử commit và thực hiện hoàn tác an toàn (Revert/Rollback).
## **3. Nhật ký thực hành**
### **3.2. Quản lý Branches**
Hệ thống ghi nhận em đã khởi tạo và điều phối công việc thành công trên 3 nhánh:
* nhánh main: Nhánh phân phối chính thức lưu trữ sản phẩm cuối cùng.
* nhánh feature 1: Nhánh phụ tạo ra nhằm phục vụ việc làm các yêu cầu: pull request, conflict, revert/rollback.
* nhánh feature 2: tương tự nhánh feature 2, tạo ra nhằm phục vụ việc làm các yêu cầu: pull request, conflict, revert/rollback.
### **3.1. Số lượng Commits**
Dự án đã tích lũy và ghi nhận thành công 29 commits gắn liền với tiến độ cập nhật nội dung qua từng giai đoạn.
### **3.3. Yêu cầu Pull Requests**
Pull Request #1: Hợp nhất nhánh 'feature-1' và 'feature-2' thành công.
Pull Request #2 (Conflict): Minh chứng tình huống xung đột mã nguồn giữa nhánh 'main' và nhánh 'conflict-branch'. Em đã tự Resolve conflicts thủ công trong tệp code bằng text editor và commit merge thành công thông qua Terminal.
Pull Request #3 (Rollback/Revert): Minh chứng thực hiện Revert bằng mã hash trên Terminal để hoàn tác một commit lỗi một cách an toàn mà không làm mất lịch sử.
### **3.4. Xử lý Conflict**
* Tình huống mô tả: Khi gộp nhánh phụ vào nhánh chính tại Pull Request #2, hệ thống phát hiện cả 2 nhánh đã chỉnh sửa với nội dung mâu thuẫn, dẫn đến việc không thể tự động gộp.
* Cách xử lý: Em đã kích hoạt trình chỉnh sửa ngay trên file code python, tiến hành xóa bỏ các thẻ đánh dấu xung đột (<<<<<<<, =======, >>>>>>>), giữ lại nội dung đồng nhất và tiến hành commit để hoàn thành việc gộp.
### **3.5. Xử lý Revert / Rollback**
Sau khi gộp Pull Request #2, em đã sử dụng tính năng Revert trực tiếp trên terminal trong VSCode, hoàn tác toàn bộ những thay đổi đã gộp một cách an toàn nhất mà không làm ảnh hưởng đến lịch sử kho chứa.
# **4. Trả lời câu hỏi: "Tôi sẽ dùng Git như thế nào khi Vibe Code với AI?"**
Khi bước vào giai đoạn Vibe Code với AI (sử dụng GitHub Copilot, Cursor, Codex, ...), AI hỗ trợ viết code rất nhanh, nhưng chính vì tốc độ đó nên Git sẽ giúp kiểm soát dự án dựa trên 3 nguyên tắc:
1. Chuẩn bị (Setup) Tạo Repo: Khởi tạo kho lưu trữ trên GitHub. Kết nối: Dùng tính năng GitHub Integration để nạp dự án vào Vibe Code giúp AI hiểu toàn bộ ngữ cảnh.
2. Quy trình: Prompt => Review => Commit.
* Bước 1 (Prompt): Yêu cầu AI viết hoặc sửa code trên VSCode. Đi từng tính năng nhỏ, tránh gom cụm quá lớn.
* Bước 2 (Review): Dùng các tính năng cơ bản để kiểm tra các file AI đã thay đổi.
* Bước 3 (Commit về máy): Tải hoặc sao chép code từ VSCode về máy local. Chạy git diff để kiểm tra lại. Commit rõ ràng: git commit -m "Feat: Add Google Auth (via Vibe Code)".
3. Quy tắc an toàn khi Chia nhánh (Branching): Luôn bắt AI làm việc trên nhánh tính năng (feature), không code thẳng vào nhánh chính (main). Kiểm thử (Test): Chạy thử code dưới máy local thấy ổn định rồi mới Merge vào nhánh chính.
# **5. Danh sách các lệnh Git đã sử dụng**
git init: Khởi tạo một kho lưu trữ Git cục bộ mới.
git clone <url>: Sao chép toàn bộ mã nguồn và lịch sử của kho lưu trữ từ GitHub về máy cá nhân.
git status: Kiểm tra trạng thái hiện tại của các file.
git add <tên_file>: Đưa các thay đổi của tệp tin vào vùng đệm (Staging Area).
git commit -m "Thông điệp": Ghi lại trạng thái mã nguồn vào lịch sử Git kèm mô tả chi tiết.
git push origin <tennhanh>: Đẩy các commit mới từ máy cục bộ lên GitHub.
git pull origin <tennhanh>: Kéo và cập nhật thay đổi mới nhất từ GitHub về máy.
git log: Xem lại toàn bộ lịch sử danh sách các commit đã thực hiện trong quá khứ.
git revert <ma>: Tạo commit mới mang nội dung ngược lại so với commit cũ nhằm hủy bỏ code lỗi một cách an toàn.
