# SMS-Man: Số điện thoại ảo, nhận SMS trực tuyến và hướng dẫn API

**Languages:** [English](README.md) · [简体中文](README.zh-CN.md) · Tiếng Việt

[SMS-Man](https://sms-man.com/) là nền tảng trực tuyến cung cấp số điện thoại ảo, dịch vụ nhận tin nhắn SMS và thuê số điện thoại trong các trường hợp được hỗ trợ. Repository này là **tài liệu hướng dẫn độc lập do cộng đồng biên soạn**, không phải mã nguồn hay tài liệu chính thức của SMS-Man.

Tài liệu giúp bạn tìm hiểu SMS-Man là gì, cách nhận SMS trực tuyến, sự khác nhau giữa kích hoạt SMS một lần và thuê số, các tài liệu API chính thức cũng như những lưu ý về quyền riêng tư và bảo mật.

- **Trang web chính thức:** https://sms-man.com/
- **Trung tâm trợ giúp:** https://sms-man.com/help
- **Tài liệu API:** https://sms-man.com/api
- **Tài liệu Compatible API:** https://sms-man.com/api/compatible

> **Lưu ý:** SMS-Man là dịch vụ thương mại của bên thứ ba. Quốc gia, ứng dụng được hỗ trợ, số lượng số điện thoại, giá, phương thức thanh toán, quy định sản phẩm và API có thể thay đổi. Hãy kiểm tra thông tin mới nhất trên trang web và tài liệu chính thức trước khi mua hoặc tích hợp.

## Mục lục

- [SMS-Man là gì?](#sms-man-là-gì)
- [SMS-Man hoạt động như thế nào?](#sms-man-hoạt-động-như-thế-nào)
- [Các tính năng chính](#các-tính-năng-chính)
- [SMS một lần và thuê số điện thoại](#sms-một-lần-và-thuê-số-điện-thoại)
- [Quốc gia và dịch vụ được hỗ trợ](#quốc-gia-và-dịch-vụ-được-hỗ-trợ)
- [Cách nhận SMS bằng SMS-Man](#cách-nhận-sms-bằng-sms-man)
- [SMS-Man API dành cho nhà phát triển](#sms-man-api-dành-cho-nhà-phát-triển)
- [Giá, tình trạng số và hoàn tiền](#giá-tình-trạng-số-và-hoàn-tiền)
- [Quyền riêng tư và bảo mật](#quyền-riêng-tư-và-bảo-mật)
- [Khắc phục sự cố](#khắc-phục-sự-cố)
- [Câu hỏi thường gặp](#câu-hỏi-thường-gặp)
- [Tài nguyên chính thức](#tài-nguyên-chính-thức)
- [Tuyên bố miễn trừ trách nhiệm](#tuyên-bố-miễn-trừ-trách-nhiệm)

## SMS-Man là gì?

SMS-Man là nền tảng cung cấp số điện thoại ảo và khả năng nhận SMS trực tuyến. Tùy thuộc vào số lượng hiện có và quy định của dịch vụ, người dùng có thể chọn quốc gia, ứng dụng hoặc dịch vụ, mua số để nhận tin nhắn xác minh và xem SMS trong tài khoản SMS-Man. Nền tảng cũng có tùy chọn thuê số dành cho nhu cầu nhận nhiều tin nhắn trong thời gian thuê.

Số điện thoại ảo không giống một thuê bao di động cá nhân. Số có thể mang tính tạm thời, được chia sẻ, tái sử dụng hoặc chịu các giới hạn từ website, ứng dụng đích hay nhà mạng. Việc một số điện thoại xuất hiện trên SMS-Man không đảm bảo nền tảng bên thứ ba sẽ chấp nhận số đó.

## SMS-Man hoạt động như thế nào?

Quy trình tổng quát:

1. Đăng ký hoặc đăng nhập trên website SMS-Man chính thức.
2. Kiểm tra quốc gia, dịch vụ, loại số và giá đang hiển thị.
3. Chọn sản phẩm phù hợp với mục đích sử dụng hợp pháp.
4. Làm theo hướng dẫn trong tài khoản SMS-Man.
5. Nếu tin nhắn được gửi thành công, xem SMS trong trang quản lý tài khoản.
6. Hủy hoặc quản lý lượt kích hoạt và thời gian thuê theo quy định hiện hành.

Xem quy trình cập nhật tại [trung tâm trợ giúp SMS-Man](https://sms-man.com/help).

## Các tính năng chính

Theo tài liệu chính thức, SMS-Man có các tính năng được mô tả dưới đây:

- **Nhận SMS trực tuyến:** xem tin nhắn gửi đến số đã mua thông qua tài khoản trực tuyến.
- **Chọn quốc gia:** duyệt số theo quốc gia hoặc khu vực, tùy thuộc vào số lượng hiện có.
- **Chọn dịch vụ:** chọn ứng dụng hoặc dịch vụ đang được liệt kê trên nền tảng.
- **Kích hoạt SMS một lần:** mua số để nhận một SMS trong những trường hợp được hỗ trợ.
- **Thuê số điện thoại:** chọn dịch vụ thuê số nếu cần nhận nhiều tin nhắn trong thời gian thuê.
- **API cho nhà phát triển:** tự động hóa các thao tác được hỗ trợ như kiểm tra số dư, giá hoặc số lượng, yêu cầu số, nhận SMS và thay đổi trạng thái kích hoạt.
- **Compatible API:** cung cấp một giao diện API khác với định dạng yêu cầu tương thích.

Đây là phần tóm tắt tính năng, không phải cam kết rằng mọi quốc gia, ứng dụng hoặc loại số đều luôn có sẵn.

## SMS một lần và thuê số điện thoại

| Tiêu chí | Kích hoạt SMS một lần | Thuê số điện thoại |
|---|---|---|
| Mục đích thường gặp | Nhận một tin nhắn xác minh | Nhận nhiều tin nhắn trong thời gian thuê |
| Thời hạn | Theo lượt kích hoạt | Theo thời hạn thuê đã chọn |
| Nhiều tin nhắn | Không nên mặc định là được hỗ trợ | Tùy thuộc sản phẩm và quy định thuê |
| Tình trạng | Phụ thuộc quốc gia, dịch vụ và kho số | Phụ thuộc quốc gia, thời hạn và kho số |
| Phù hợp với | Nhu cầu một lần, ít rủi ro và được phép | Quy trình hợp pháp cần nhận SMS liên tục |

Theo trung tâm trợ giúp chính thức, số trong mục **Receive SMS** chỉ dùng để nhận một SMS; nếu cần nhận nhiều tin nhắn, hãy xem sản phẩm thuê số. Luôn kiểm tra mô tả sản phẩm hiện tại trước khi mua: [SMS-Man Help](https://sms-man.com/help).

## Quốc gia và dịch vụ được hỗ trợ

SMS-Man cho phép chọn quốc gia và dịch vụ thông qua website và API. Kho số có thể thay đổi, vì vậy việc duy trì một danh sách quốc gia cố định trong README GitHub có thể nhanh chóng trở nên lỗi thời.

Để kiểm tra tình trạng hiện tại:

1. Truy cập [website SMS-Man](https://sms-man.com/).
2. Chọn quốc gia hoặc khu vực.
3. Chọn ứng dụng hoặc dịch vụ cần dùng nếu có trong danh sách.
4. Kiểm tra giá, số lượng và giới hạn trước khi đặt mua.

Không nên xem ảnh chụp màn hình cũ hoặc danh sách của bên thứ ba là bằng chứng về số lượng hiện có theo thời gian thực.

## Cách nhận SMS bằng SMS-Man

Giao diện có thể thay đổi, nhưng quy trình được mô tả trong tài liệu trợ giúp thường gồm:

1. **Đăng ký hoặc đăng nhập** tại [sms-man.com](https://sms-man.com/).
2. **Kiểm tra thông tin sản phẩm:** quốc gia, dịch vụ, loại số, giá và các giới hạn.
3. **Chọn số còn khả dụng** thông qua giao diện chính thức.
4. **Chỉ sử dụng cho mục đích được phép.** Chỉ nhập số vào dịch vụ đích nếu dịch vụ đó cho phép số ảo và việc sử dụng tuân thủ điều khoản.
5. **Kiểm tra tài khoản SMS-Man** để xem tin nhắn đến.
6. **Hoàn tất xác minh** nếu dịch vụ đích chấp nhận số và tin nhắn được gửi thành công.
7. **Quản lý lượt kích hoạt hoặc thời gian thuê** theo hướng dẫn chính thức.

Nếu không nhận được SMS, hãy làm theo hướng dẫn chờ, hủy, thử lại hoặc liên hệ hỗ trợ trong trung tâm trợ giúp. Điều kiện hoàn tiền phụ thuộc chính sách hiện hành; không nên mặc định mọi lần thử không thành công đều được hoàn tiền.

## SMS-Man API dành cho nhà phát triển

SMS-Man công bố tài liệu API để tích hợp phần mềm. Tài liệu chính thức mô tả API v2.0 và Compatible API. Trước khi phát triển, hãy đọc tài liệu tương ứng:

- [Tài liệu API v2.0](https://sms-man.com/api)
- [Tài liệu Compatible API](https://sms-man.com/api/compatible)

### API v2.0

Tài liệu API v2.0 chỉ định endpoint:

`https://api.sms-man.com/control/`

Các thao tác được mô tả gồm:

| Thao tác | Mục đích |
|---|---|
| Balance request | Lấy số dư tài khoản |
| Get limits | Kiểm tra số lượng theo quốc gia và dịch vụ |
| Request a phone number | Yêu cầu số cho ứng dụng đã chọn |
| Get SMS | Lấy SMS gắn với yêu cầu |
| Change request status | Thay đổi trạng thái kích hoạt |
| Get current prices | Lấy dữ liệu giá và số lượng |
| List countries | Lấy danh sách quốc gia |
| List services | Lấy danh sách dịch vụ |

Yêu cầu API cần token của tài khoản. Tham số, phương thức HTTP, cấu trúc phản hồi và giá trị trạng thái phải tuân theo [tài liệu API chính thức](https://sms-man.com/api).

### Compatible API

Tài liệu Compatible API chỉ định endpoint:

`https://api.sms-man.com/stubs/handler_api.php`

Giao diện này sử dụng tham số `api_key` và mô tả các thao tác như kiểm tra số dư, giá, yêu cầu số, lấy danh sách quốc gia và dịch vụ, cũng như cập nhật trạng thái kích hoạt. Xem [tài liệu Compatible API](https://sms-man.com/api/compatible) để biết định dạng yêu cầu và phản hồi chính xác.

### Lưu ý bảo mật API

- Lưu API token trong biến môi trường hoặc dịch vụ quản lý bí mật.
- Không commit API key, cookie phiên, mật khẩu hoặc dữ liệu cá nhân vào GitHub công khai.
- Không để lộ thông tin xác thực trong JavaScript chạy trên trình duyệt.
- Thay token ngay nếu vô tình công khai.
- Thiết lập timeout, xử lý lỗi và chú ý giới hạn yêu cầu.
- Chỉ ghi log ID yêu cầu và thông tin chẩn đoán không nhạy cảm; không ghi nội dung SMS hoặc thông tin xác thực.
- Chỉ sử dụng API trong quy trình hợp pháp, được ủy quyền và tuân thủ điều khoản của SMS-Man cũng như dịch vụ đích.

Repository này không chứa API client, không chuyển tiếp tin nhắn SMS và không thu thập thông tin đăng nhập.

## Giá, tình trạng số và hoàn tiền

Giá và số lượng số điện thoại trên SMS-Man có thể thay đổi theo quốc gia, dịch vụ, loại số, thời hạn thuê và kho số hiện tại. Repository không duy trì bảng giá cố định vì dữ liệu tĩnh có thể gây hiểu nhầm khi đã lỗi thời.

Trước khi thanh toán, hãy xác nhận:

- quốc gia và dịch vụ đã chọn;
- sản phẩm là kích hoạt một lần hay thuê số;
- giá và đơn vị tiền tệ hiển thị;
- số điện thoại còn khả dụng;
- điều kiện hủy và hoàn tiền;
- giới hạn số ảo của dịch vụ đích.

Với câu hỏi về thanh toán hoặc hoàn tiền, hãy tham khảo [trung tâm trợ giúp SMS-Man](https://sms-man.com/help) và chính sách hiện hành trên website. Bài viết cũ hoặc README cộng đồng không thay thế chính sách ràng buộc của nhà cung cấp.

## Quyền riêng tư và bảo mật

Số điện thoại ảo có thể hữu ích cho kiểm thử và các quy trình được phép, nhưng cũng có rủi ro:

- **Khôi phục tài khoản:** bạn có thể không kiểm soát được số trong tương lai, nên số tạm thời không phù hợp với tài khoản cần khôi phục qua SMS.
- **Tái sử dụng số:** số tạm thời hoặc số được tái cấp có thể được giao cho người khác sau này.
- **Quyền truy cập dùng chung:** không nên xem số ảo là đường dây riêng tư và vĩnh viễn.
- **Giới hạn của bên thứ ba:** một số dịch vụ có thể chặn số ảo hoặc cấm cách sử dụng này trong điều khoản.
- **Tài khoản nhạy cảm:** tránh dùng số tạm thời cho ngân hàng, tài chính, y tế, dịch vụ chính phủ hoặc tài khoản chứa dữ liệu cá nhân nhạy cảm.
- **Tuân thủ pháp luật:** tuân thủ luật áp dụng, điều khoản SMS-Man và quy định của dịch vụ đích.

Không sử dụng số ảo để giả mạo người khác, né tránh biện pháp bảo vệ nền tảng, tạo tài khoản lừa đảo, vượt quyền truy cập hoặc thực hiện spam, gian lận, quấy rối hay hành vi lạm dụng khác.

## Khắc phục sự cố

| Vấn đề | Cần kiểm tra |
|---|---|
| Không có số khả dụng | Kiểm tra lại sau hoặc xem quốc gia/dịch vụ khác được hỗ trợ; kho số thay đổi theo thời gian. |
| Chưa nhận được SMS | Làm theo hướng dẫn chờ, hủy và thử lại trong trung tâm trợ giúp. |
| Dịch vụ đích từ chối số | Dịch vụ có thể không chấp nhận số ảo hoặc số đã từng được sử dụng. Không có gì đảm bảo đổi số sẽ thành công. |
| API xác thực thất bại | Kiểm tra API key, endpoint, tham số bắt buộc và phiên bản API. Không đăng key trong issue công khai. |
| API trả về lỗi | Đối chiếu danh sách lỗi chính thức, kiểm tra request ID và trạng thái kích hoạt. |
| Câu hỏi về thanh toán/hoàn tiền | Liên hệ hỗ trợ SMS-Man và xem chính sách hiện hành. |

## Câu hỏi thường gặp

### SMS-Man có miễn phí không?

SMS-Man là dịch vụ thương mại. Hãy kiểm tra website chính thức để biết giá, phương thức thanh toán và chương trình khuyến mãi hiện tại.

### Có thể nhận SMS trực tuyến bằng SMS-Man không?

SMS-Man được thiết kế để người dùng xem tin nhắn gửi đến các số được cung cấp thông qua tài khoản trực tuyến. Khả năng nhận thành công phụ thuộc số đã chọn và quy định xác minh của dịch vụ đích.

### Một số SMS-Man có thể nhận nhiều tin nhắn không?

Theo trung tâm trợ giúp chính thức, số trong mục Receive SMS chỉ dành cho một SMS. Nếu cần nhận nhiều tin nhắn, hãy xem sản phẩm thuê số và quy định cụ thể.

### SMS-Man có hỗ trợ mọi website và ứng dụng không?

Không. Danh sách dịch vụ có thể thay đổi và nền tảng bên thứ ba có thể từ chối số ảo. Không có đảm bảo rằng mọi số đều xác minh thành công.

### SMS-Man có API không?

Có. SMS-Man công bố tài liệu API v2.0 và Compatible API tại [trang API chính thức](https://sms-man.com/api).

### Lấy API key SMS-Man ở đâu?

Trung tâm trợ giúp chính thức cho biết API key có thể xem trong hồ sơ người dùng. Hãy giữ bí mật key và không đưa vào mã nguồn công khai.

### Số ảo SMS-Man có phù hợp với tài khoản quan trọng không?

Số tạm thời hoặc số thuê có thể không nằm trong quyền kiểm soát lâu dài của bạn. Với tài khoản quan trọng, hãy dùng số điện thoại hoặc phương thức xác minh mà bạn kiểm soát và dịch vụ đích chính thức hỗ trợ.

### Liên hệ hỗ trợ SMS-Man ở đâu?

Sử dụng các kênh liên hệ được cung cấp trên [website SMS-Man](https://sms-man.com/) và [trung tâm trợ giúp](https://sms-man.com/help).

## Tài nguyên chính thức

| Tài nguyên | Liên kết |
|---|---|
| Website chính thức | https://sms-man.com/ |
| Trung tâm trợ giúp | https://sms-man.com/help |
| API v2.0 | https://sms-man.com/api |
| Compatible API | https://sms-man.com/api/compatible |
| Trung tâm trợ giúp tiếng Trung | https://sms-man.com/cn/help |
| API tiếng Trung | https://sms-man.com/cn/api |

## Tuyên bố miễn trừ trách nhiệm

Repository này là tài liệu thông tin độc lập, không liên kết, không được ủy quyền và không được SMS-Man chứng thực. “SMS-Man” và các nhãn hiệu liên quan thuộc về chủ sở hữu tương ứng. Nội dung mô tả và liên kết chỉ nhằm mục đích tham khảo; điều khoản, giá và quy định sản phẩm hiện hành của nhà cung cấp chính thức được ưu tiên áp dụng.

Repository không khuyến khích vi phạm điều khoản của bên thứ ba, né tránh cơ chế bảo vệ xác minh hoặc sử dụng số ảo cho hoạt động bất hợp pháp hay lạm dụng. Người dùng tự chịu trách nhiệm đảm bảo việc sử dụng tuân thủ luật áp dụng và quy định của các dịch vụ liên quan.

---

Nếu hướng dẫn này hữu ích, hãy cân nhắc Star repository và kiểm tra tài liệu SMS-Man chính thức để cập nhật thông tin mới nhất.
