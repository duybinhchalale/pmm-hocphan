# Bài 1.2 – Phân tích sự rẽ nhánh OpenOffice.org và LibreOffice

## 1. Giới thiệu

Một dự án mã nguồn mở không chỉ phụ thuộc vào chất lượng lập trình mà còn chịu ảnh hưởng lớn từ cách quản trị cộng đồng. Trường hợp OpenOffice.org và LibreOffice là ví dụ tiêu biểu về việc bất đồng giữa doanh nghiệp quản lý dự án và những người đóng góp dẫn đến một nhánh phát triển mới.

## 2. Bối cảnh hình thành

OpenOffice.org là bộ phần mềm văn phòng gồm công cụ soạn thảo văn bản, bảng tính và trình chiếu. Năm 2000, Sun Microsystems công bố mã nguồn StarOffice và tạo nền tảng cho dự án OpenOffice.org. Trong nhiều năm, dự án thu hút lập trình viên, tình nguyện viên dịch thuật và người dùng ở nhiều quốc gia. Tuy nhiên, Sun vẫn giữ vai trò lớn trong việc định hướng và tổ chức phát triển.

Năm 2010, Oracle hoàn tất việc mua lại Sun Microsystems. Sự thay đổi chủ sở hữu khiến nhiều thành viên lo ngại tương lai của OpenOffice.org sẽ phụ thuộc quá nhiều vào quyết định của một doanh nghiệp. Một bộ phận cộng đồng mong muốn dự án được quản trị độc lập, có tiếng nói rộng rãi hơn từ những người đóng góp.

## 3. Nguyên nhân và diễn biến rẽ nhánh

Tháng 9 năm 2010, các thành viên cộng đồng công bố The Document Foundation và giới thiệu LibreOffice, một nhánh phát triển dựa trên mã nguồn OpenOffice.org. Trong phát triển phần mềm, hành động tạo một hướng phát triển riêng từ mã nguồn sẵn có được gọi là fork. Việc này hợp pháp khi tuân thủ giấy phép của dự án gốc.

Theo tôi, mâu thuẫn ở đây không đơn thuần là tranh cãi về một tính năng. Vấn đề cốt lõi là quyền quyết định tương lai dự án, mức độ minh bạch và sự tin tưởng giữa doanh nghiệp với cộng đồng. Khi các thành viên cảm thấy khó tham gia quyết định, họ có động lực xây dựng một tổ chức độc lập để bảo vệ cách phát triển mà mình mong muốn.

Năm 2011, Oracle chấm dứt phát triển OpenOffice.org và chuyển mã nguồn cùng thương hiệu cho Apache Software Foundation. Từ đó, hai dự án tiếp tục tồn tại dưới những mô hình quản trị khác nhau: Apache OpenOffice thuộc hệ sinh thái Apache, còn LibreOffice gắn với The Document Foundation.

## 4. Hệ quả và đánh giá

Việc tách nhánh có cả lợi ích lẫn bất lợi. Về mặt tích cực, LibreOffice tạo điều kiện để cộng đồng chủ động hơn trong quản trị, tiếp nhận đóng góp và cải tiến sản phẩm. Người dùng có thêm lựa chọn thay vì chỉ phụ thuộc vào một bên điều hành. Sự tồn tại của một nhánh mới cũng chứng minh quyền sửa đổi và phân phối lại mã nguồn có ý nghĩa thực tế chứ không chỉ nằm trên giấy phép.

Mặt hạn chế là việc tách cộng đồng có thể làm phân tán nhân lực, tài liệu và nguồn lực kiểm thử. Hai nhóm cùng phát triển những chức năng tương tự có thể phải lặp lại công việc. Người dùng cũng dễ bối rối khi lựa chọn giữa hai phần mềm có chung nguồn gốc. Vì vậy, fork không phải giải pháp tối ưu cho mọi bất đồng; nó thường xuất hiện khi việc đối thoại và cải thiện quản trị không đạt kết quả mong muốn.

## 5. Bài học rút ra

Qua trường hợp này, tôi hiểu rằng một dự án mã nguồn mở muốn bền vững cần có quy trình ra quyết định minh bạch, tôn trọng người đóng góp và cơ chế xử lý bất đồng. Bài học quan trọng nhất là giấy phép mở tạo ra quyền lựa chọn, còn văn hóa hợp tác và quản trị tốt quyết định dự án có phát triển lâu dài hay không.

## Tài liệu tham khảo

1. LibreOffice – LibreOffice Timeline: https://www.libreoffice.org/libreoffice-timeline/
2. The Document Foundation – Who are we?: https://www.libreoffice.org/who-are-we/
3. Apache Software Foundation – Board History: https://www.apache.org/foundation/board/minutes/OpenOffice.html

# Bài 1.3 – Tragedy of the Commons trong mã nguồn mở: Trường hợp OpenSSL và Heartbleed

## 1. Khái niệm và vấn đề đặt ra

Tragedy of the commons, thường được dịch là bi kịch tài nguyên chung, mô tả tình huống nhiều bên cùng hưởng lợi từ một nguồn lực nhưng không bên nào có đủ động lực tự nguyện gánh chi phí duy trì nguồn lực đó. Trong phần mềm mã nguồn mở, vấn đề xuất hiện khi doanh nghiệp và cá nhân cùng sử dụng một thư viện quan trọng, trong khi việc phát triển, kiểm thử và vá lỗi vẫn dựa vào một nhóm bảo trì nhỏ.

Mã nguồn mở cho phép mọi người sử dụng và đóng góp theo điều kiện giấy phép. Tuy nhiên, quyền sử dụng không tự động tạo ra nghĩa vụ đóng góp tài chính. Một công ty có thể kiếm doanh thu từ sản phẩm xây trên thư viện mở mà không phải trả phí duy trì thư viện. Điều này không nhất thiết sai về pháp lý, nhưng nếu quá nhiều bên chỉ nhận lợi ích và rất ít bên đầu tư trở lại, dự án chung có nguy cơ thiếu nhân lực, kinh phí và thời gian kiểm tra chất lượng.

## 2. Trường hợp OpenSSL trước năm 2014

OpenSSL là thư viện cung cấp các chức năng mật mã và hỗ trợ giao thức bảo mật như TLS. Nó được sử dụng rộng rãi trong máy chủ, ứng dụng và nhiều hệ thống kết nối Internet.

Trước năm 2014, OpenSSL có số lượng người sử dụng rất lớn, trong khi nhóm bảo trì thường xuyên lại tương đối nhỏ và nguồn lực tài chính hạn chế. Nhiều tổ chức xem thư viện này là một phần hạ tầng có sẵn, chỉ quan tâm đến tính năng và khả năng hoạt động của nó. Ít tổ chức trực tiếp đóng góp nhân lực rà soát mã, trả kinh phí kiểm toán bảo mật hoặc hỗ trợ công việc bảo trì lâu dài.

## 3. Sự cố Heartbleed và hậu quả

Tháng 4 năm 2014, lỗ hổng Heartbleed, mã CVE-2014-0160, được công bố trong OpenSSL. Lỗi nằm ở cách xử lý phần mở rộng Heartbeat của TLS và có thể khiến hệ thống tiết lộ một phần dữ liệu trong bộ nhớ. Thông tin bị lộ có khả năng chứa dữ liệu nhạy cảm như mật khẩu, phiên đăng nhập hoặc khóa bí mật, tùy vào nội dung bộ nhớ bị truy cập.

Heartbleed không phải là lỗi của bản thân giao thức TLS mà là sai sót trong cách triển khai thư viện. Không thể kết luận đơn giản rằng thiếu kinh phí trực tiếp tạo ra Heartbleed. Lập trình viên của cả dự án thương mại lẫn mã nguồn mở đều có thể mắc lỗi. Tuy vậy, sự cố phơi bày khoảng cách giữa mức độ quan trọng của OpenSSL và nguồn lực thực tế dành cho công việc kiểm thử, rà soát và bảo trì. Bài học là công khai mã nguồn chưa đủ bảo đảm an toàn nếu không có người thực sự đọc và kiểm tra mã.

## 4. Các giải pháp đề xuất

### Giải pháp thứ nhất: Tài trợ dài hạn cho dự án

Giải pháp thứ nhất là lập quỹ tài trợ dài hạn cho các thư viện hạ tầng. Doanh nghiệp đang sử dụng OpenSSL có thể đóng góp ngân sách định kỳ, phù hợp với quy mô và mức độ phụ thuộc. Tiền tài trợ nên chi cho nhân sự bảo trì, kiểm toán bảo mật và xử lý lỗ hổng chứ không chỉ dành cho việc phát triển tính năng mới. Sau Heartbleed, Core Infrastructure Initiative của Linux Foundation đã hỗ trợ hai người làm việc toàn thời gian cho OpenSSL trong ba năm và tài trợ kiểm toán bảo mật. Đây là ví dụ cho thấy đóng góp có tổ chức có thể giúp giảm áp lực lên nhóm duy trì.

### Giải pháp thứ hai: Đóng góp kỹ thuật

Giải pháp thứ hai là chia sẻ trách nhiệm bằng đóng góp kỹ thuật. Những doanh nghiệp sử dụng thư viện có thể cho kỹ sư tham gia sửa lỗi, viết bộ kiểm thử, xem xét pull request và cải thiện tài liệu.

### Giải pháp thứ ba: Minh bạch trong quản trị

Giải pháp thứ ba là tăng minh bạch trong quản trị và sử dụng kinh phí. Dự án nên công bố lộ trình, nhu cầu bảo trì, báo cáo tài trợ và quy trình quyết định ưu tiên.

### Giải pháp thứ tư: Quản lý rủi ro của bên sử dụng

Giải pháp thứ tư là chủ động quản lý rủi ro tại từng tổ chức sử dụng. Doanh nghiệp cần có danh sách các thư viện phụ thuộc, theo dõi bản vá, kiểm tra cập nhật và đánh giá những thành phần quan trọng. Không thể giao toàn bộ trách nhiệm bảo mật cho nhóm tác giả mã nguồn mở. Bên sử dụng phần mềm vẫn phải chịu trách nhiệm bảo vệ sản phẩm và dữ liệu của mình.

## 5. Đánh giá tính khả thi và kết luận

Theo tôi, các giải pháp chỉ hiệu quả khi được triển khai cùng nhau. Cơ chế tài trợ định kỳ, đóng góp kỹ thuật và quản trị minh bạch tạo ra sự cân bằng tốt hơn giữa quyền hưởng lợi và trách nhiệm bảo vệ hạ tầng chung.

Trường hợp OpenSSL cho thấy mã nguồn mở không đồng nghĩa với tài nguyên vô hạn. Phần mềm có thể sao chép với chi phí rất thấp, nhưng thời gian, kiến thức và sức lao động của người bảo trì vẫn hữu hạn. Để cộng đồng phát triển bền vững, người hưởng lợi cần tham gia nuôi dưỡng nguồn lực chung, thay vì mặc nhiên cho rằng sẽ luôn có người khác làm công việc khó khăn đó.

## Tài liệu tham khảo

1. OpenSSL Foundation – History: https://openssl.foundation/about/history
2. OpenSSL Corporation – OpenSSL Finances (2023): https://openssl-corporation.org/blog/2023-08-08-finances.html
3. CVE Program – CVE-2014-0160: https://www.cve.org/CVERecord?id=cve-2014-0160
4. OpenSSL Library – Sponsorship and Donations: https://openssl-library.org/donations/
