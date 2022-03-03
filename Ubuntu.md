# Thiết lập ban đầu đối với Ubuntu
![Ubuntu](https://user-images.githubusercontent.com/97789851/156393979-9354be29-ae9e-4197-a939-c1532161e2bb.jpg)

**Bước 1 - Đăng nhập với quyền root**

Để đăng nhập vào tài khoản **root** bạn sử dụng lệnh sau:
        
        sudo su
Sau khi đăng nhập bằng quyền **root**. Chúng ta thiết lập một tài khoản người dùng mới với các đặc quyền giảm bớt để sử dụng hàng ngày.

**Bước 2 - Tạo người dùng mới**

Ví dụ này tạo một người dùng mới có tên là **admin**, nhưng bạn nên thay thế người dùng đó bằng một tên người dùng mà bạn thích:

        adduser admin
Bạn sẽ được hỏi một số câu hỏi, bắt đầu với mật khẩu của tài khoản mới. 

Nhập một mật khẩu mạnh và điền vào bất kỳ trường thông tin bổ sung nào nếu bạn muốn. Điều này không bắt buộc và bạn có thể nhấn "ENTER" bỏ qua.

**Bước 3 - Cấp đặc quyền quản trị**

Bây giờ mình đã có một tài khoản người dùng mới với các đặc quyền tài khoản thông thường. Tuy nhiên, nhiều lúc mình có thể cần thực hiện các công việc nâng cao của quản trị. Để thiết lập siêu người dùng hoặc đặc quyền root cho tài khoản bình thường, điều này sẽ cho phép người dùng bình thường chạy các lệnh có đặc quyền quản trị bằng cách đặt từ trước lệnh **sudo**.

Để thêm các đặc quyền này cho người dùng mới, mình sẽ thêm người dùng đó vào nhóm **sudo**. Theo mặc định, trên **Ubuntu** 20.04, người dùng là thành viên của nhóm **sudo** được phép sử dụng lệnh **sudo**.

        usermod -aG sudo admin
**->** Giờ đây, khi đã đăng nhập với tư cách người dùng **admin**, bạn có thể nhập **sudo** trước các lệnh để chạy chúng với các đặc quyền của **người dùng siêu cấp**.

**=> Như vậy chúng ta đã hoàn thành các thiết lập ban đầu của máy chủ.**

**Bây giờ, các bạn cần thoát khỏi tài khoản root, đăng xuất khỏi hệ thống. Sau đó đăng nhập vào tài khoản siêu cấp admin**

        exit
        logout
**Sử dụng tài khoản siêu cấp để đăng nhập, sau đây là kết quả hiển thị:**

        To run a command as administrator (user "root"), use "sudo <command>".
        See "man sudo_root" for details.
        admin@ubuntu:~$
## Chúc các bạn thành công :>
