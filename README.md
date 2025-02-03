### 1. Xóa và thêm lại remote origin
- Kiểm tra remote hiện tại: git remote -v
- git remote remove origin
- git remote add origin https://github.com/DuongTrungQuoc/Face_Detection_with_MTCNN.git

### 2. .gitignore
- touch .gitignore
- git rm -r --cached .
- git add .
- git commit -m "Cập nhật .gitignore"
#### Node modules
node_modules/

#### Logs
logs
*.log

#### Operating system files
.DS_Store

#### Environment files
.env

#### IDE specific files
.vscode/


<h2>Thao tác trên nhánh (branch)</h2> 

### 1. Liệt kê các branch
- git branch: Liệt kê tất cả các branch cục bộ.
- git branch -r: Liệt kê tất cả các branch trên remote.
- git branch -a: Liệt kê tất cả các branch, bao gồm cả branch cục bộ và branch trên remote.
### 2. Tạo branch mới
- git branch branch-name: Tạo một branch mới có tên branch-name, nhưng không chuyển sang branch đó.
- git checkout -b branch-name: Tạo một branch mới và chuyển ngay sang branch đó.
### 3. Đổi tên branch
- git branch -m new-branch-name: Đổi tên branch hiện tại thành <new-branch-name>.
- git branch -m old-branch-name new-branch-name: Đổi tên branch old-branch-name --> new-branch-name.
### 4. Xóa branch
- git branch -d branch-name: Xóa branch branch-name nếu branch đã được merge.
- git branch -D branch-name: Xóa branch branch-name bất kể branch đó đã được merge hay chưa (cẩn thận khi dùng lệnh này vì dữ liệu có thể bị mất).
### 5. Kiểm tra thông tin về branch
- git branch -v: Hiển thị branch hiện tại và commit cuối cùng của mỗi branch.
- git branch --merged: Liệt kê các branch đã được merge vào branch hiện tại.
- git branch --no-merged: Liệt kê các branch chưa được merge vào branch hiện tại.
### 6. Thiết lập branch tracking (theo dõi branch)
- git branch -u remote/branch-name: Thiết lập branch cục bộ để theo dõi một branch trên remote.
- git branch -u origin/main: Thiết lập branch hiện tại để theo dõi branch main trên remote origin.
### 7. Xóa branch trên remote
- Để xóa branch trên remote, bạn dùng lệnh git push:
- #### Code: git push origin --delete branch-name
### 8. Hiển thị thông tin chi tiết về tất cả branch
- git branch -vv: Hiển thị chi tiết về tất cả các branch, bao gồm branch nào đang được theo dõi, commit cuối cùng, và trạng thái tracking.
### 9. Tạo một branch từ một commit cụ thể
- git branch branch-name commit-hash: Tạo một branch mới từ một commit cụ thể (dùng commit hash).
### 10. Xóa các branch cục bộ không còn tồn tại trên remote
- git fetch -p: Xóa các branch cục bộ đã bị xóa trên remote. Tùy chọn -p sẽ “prune” (dọn dẹp) những branch không còn tồn tại trên remote.
- ### Ví dụ sử dụng:
- #### Tạo một branch mới và chuyển sang branch đó:
  #### Code: git checkout -b feature/new-feature
- #### Xóa một branch không còn dùng nữa:
  #### Code: git branch -D old-feature
- #### Thiết lập branch hiện tại để theo dõi main từ remote origin:
  #### Code: git branch -u origin/main
  
### 11. Cấu hình git config

- git config --global user.name "Your Name"

- git config --global user.email "your-email@example.com"

<h2>Git Workflow Diagram</h2> 
<p>Thư mục đang làm việc ───[git add _file]───> StagingArea ───[git commit]───> Committed ───[git push]───> Repo</p>
<p> Thư mục đang làm việc<──[git restore --staged]──Staging Area</p>
  
<h2>Commit Tree</h2>
<img src="images/commit-tree.jpg"/>

<h2>Resolve Conflict:</h2><p>Xung đột thường xảy ra khi có nhiều người cùng chỉnh sửa một file và các thay đổi đó không thể tự động hợp nhất (merge) lại được.</p>

<img src="images/conflict.png"/>


