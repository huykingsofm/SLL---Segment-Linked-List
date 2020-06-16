# Hướng dẫn đóng góp
### Bước 1: Chọn issue cần hỗ trợ và chưa có người đóng góp.
### Bước 2: Đăng ký đóng góp bằng cách tự assign issue này cho bản thân.
### Bước 3: Tạo pull request
*Lưu ý: Nếu đã thực hiện mục a và b thì có thể bỏ qua*  
a. Click vào fork để kéo repository về github của bạn, sau đó clone về máy local. 

b. Tạo upstream mới liên kết với repository gốc
> `$ git remote add upstream https://github.com/huykingsofm/SLL---Segment-Linked-List`

c. Đồng bộ repository ở github gốc về fork repository
> `$ git fetch upstream`  
> `$ git checkout master`  
> `$ git merge upstream/master`

d. Tạo một branch mới với tên branch là "branch_" + mã số của issue. Ví dụ issue có mã số là #123 thì tên branch là "branch_123"
> `$ git checkout -b branch_123`

e. Chỉnh sửa các file tương ứng với issue đã nhận

f.  Commit các thay đổi với comment là tiêu đề của issue.
> `$ git add .`  
> `$ git commit -m "issue title"`

g. Push branch đã tạo lên git
> `$ git push -u origin branch_123`

h. Vào trang github của repository gốc, đăng nhập với tài khoản của bạn, sẽ xuất hiện nút bấm **Compare & pull request**. Bấm vào nó, sau khi kiểm tra lại các thay đổi của bạn, đặt comment là tiêu đề của issue và nhấn **Create pull request**.

### Bước 4: Chờ phản hồi từ người bảo trì repository.