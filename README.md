# SLL---Segment-Linked-List (Danh sách liên kết phân đoạn)
The combination of Segment Tree and Linked List  
Sự kết hợp giữa Segment Tree (cây phân đoạn) và Linked List (danh sách liên kết)


# Danh sách liên kết
Danh sách liên kết là một cấu trúc dữ liệu được sử dụng rất phổ biến trong lập trình.  
Danh sách liên kết là một tập hợp các phần tử dữ liệu, tuy nhiên các phần tử này không liền kề nhau trên địa chỉ vật lý. Thay vào đó, mỗi phần tử trỏ đến địa chỉ của phần tử kế tiếp nó.

![Ví dụ danh sách liên kết](https://res.cloudinary.com/practicaldev/image/fetch/s--y3j6aJXJ--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://res.cloudinary.com/practicaldev/image/fetch/s--_PwtVEkJ--/c_limit%252Cf_auto%252Cfl_progressive%252Cq_auto%252Cw_880/https://www.educative.io/api/edpresso/shot/5077575695073280/image/5192456339456000)
*<center> Minh họa danh sách liên kết </center>*

Ưu điểm của dánh sách liên kết so với mảng:  
1. Kích thước danh sách liên kết là động và không cần phải khai báo trước số lượng phần tử tối đa, đồng nghĩa với việc không cần tạo ra một vùng nhớ trống để giữ chỗ cho các phần tử khác khi cần được thêm vào  giống với mảng .
2. Thời gian thêm, chèn, xóa một phần tử là rất nhanh nếu biết địa chỉ ô nhớ của phần tử đó.

Nhược điểm của danh sách liên kết so với mảng:
1. Truy cập một phần tử tại một vị trí nhất định có độ phức tạp tuyến tính.
2. Mặc dù thêm, chèn hay xóa một phần tử trong danh sách liên kết nhanh hơn mảng, tuy nhiên đó là trường hợp biết trước địa chỉ ô nhớ của phần tử đó - một thao tác có độ phức tạp tuyến tính nếu thực hiện việc tìm kiếm thông thường.

# Cây phân đoạn
Segment Tree là một cây, cụ thể hơn, nó là một cây nhị phân đầy đủ (mỗi nút là lá hoặc có đúng 2 nút con), với mỗi nút quản lý một đoạn trên dãy số. Thông tin mà một nút quản lý trên một đoạn có thể là giá trị lớn nhất của đoạn, miền giá trị của đoạn,...

![Ví dụ về cây phân đoạn quản lý miền giá trị của đoạn](https://leetcode.com/articles/Figures/segtree_example_1.png)
*<center> Ví dụ về cây phân đoạn quản lý tổng của đoạn </center>*

Ưu điểm của cây phân đoạn là các thao tác truy cập có độ phức tạp O(log(N)), với N là số lượng các nút lá.

# Ý tưởng
Với mong muốn tận dụng tối đa khả năng tốc độ các thao tác thêm, chèn, xóa các phần tử trong danh sách liên kết, cây phân đoạn được ứng dụng vào quản lý danh sách liên kết để giảm độ phức tạp các thao tác trên xuống còn O(log(N)).

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