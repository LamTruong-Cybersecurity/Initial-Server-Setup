# Thiết lập ban đầu đối với CentOS
![png-transparent-centos-installation-linux-virtual-private-server-tutorial-linux](https://user-images.githubusercontent.com/97789851/156534272-2211c8b4-4be6-49a5-b856-05e2f206f4c7.png)

**Bước 1 - Tạo người dùng mới**

Khi bạn đã đăng nhập **root**, chúng ta thiết lập một tài khoản người dùng mới với các đặc quyền giảm bớt để sử dụng hàng ngày.

Ví dụ này tạo một người dùng mới có tên là **admin**, nhưng bạn nên thay thế nó bằng một tên người dùng mà bạn thích:

        adduser admin
Tiếp theo, đặt mật khẩu cho người dùng mới mà bạn vừa tạo. Ở đây người dùng mới của mình là **admin** (bạn hãy thay thế **admin** bằng người dùng mà bạn vừa tạo):

        passwd admin
Nhập mật khẩu mạnh và lặp lại một lần nữa để xác minh.

**Bước 2 - Cấp đặc quyền quản trị**

Bây giờ mình đã có một tài khoản người dùng mới với các đặc quyền tài khoản thông thường. Tuy nhiên, nhiều lúc mình có thể cần thực hiện các công việc nâng cao của quản trị. Để thiết lập siêu người dùng hoặc đặc quyền root cho tài khoản bình thường, điều này sẽ cho phép người dùng bình thường chạy các lệnh có đặc quyền quản trị bằng cách đặt từ trước lệnh **sudo**.

Để thêm các đặc quyền này cho người dùng mới, mình sẽ thêm người dùng đó vào nhóm **wheel**. Theo mặc định, trên **CentOS** 7, người dùng là thành viên của nhóm **wheel** được phép sử dụng lệnh **sudo**.

        gpasswd -a admin wheel
**->** Giờ đây, khi đã đăng nhập với tư cách người dùng **admin**, bạn có thể nhập **sudo** trước các lệnh để chạy chúng với các đặc quyền của **người dùng siêu cấp**.

**=> Như vậy chúng ta đã hoàn thành các thiết lập ban đầu của máy chủ.**

**Bây giờ, các bạn cần đăng xuất khỏi hệ thống. Sau đó đăng nhập vào tài khoản siêu cấp admin**

        logout
**Sử dụng tài khoản siêu cấp để đăng nhập, sau đây là kết quả hiển thị:**

        [admin@CentOS7-Clean ~]$
## Chúc các bạn thành công :>