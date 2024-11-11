## 1. DNS là gì
Domain Name System (DNS) là một hệ thống phân giải tên miền dùng để tìm kiếm địa chỉ IP của một trang web hoặc một tài nguyên trên mạng Internet.

Khi nhập vào một địa chỉ web vào trình duyệt, trình duyệt sẽ sử dụng DNS để tìm kiếm địa chỉ IP của máy chủ chứa trang web đó.

DNS còn có thể được sử dụng để phân giải tên miền của các dịch vụ khác nhau, chẳng hạn như địa chỉ email, máy chủ FTP hoặc các dịch vụ mạng khác.

DNS cũng hỗ trợ các tính năng bảo mật như chữ ký số và mã hoá để đảm bảo tính bảo mật của thông tin truyền tải qua mạng.

## 2. Chức năng của DNS server

DNS server có chức năng quan trọng trong việc phân giải tên miền thành địa chỉ IP và giúp trình duyệt tìm kiếm và kết nối đến các trang web hoặc tài nguyên trên mạng Internet. Một số chức năng của DNS server:
- **Phân giải tên miền**: DNS server lưu trữ thông tin về các tên miền và địa chỉ IP tương ứng. Khi trình duyệt yêu cầu tìm kiếm một tên miền, DNS server sẽ truy vấn trong cơ sở dữ liệu để tìm kiếm thông tin tương ứng với tên miền đó.
- **Cập nhật thông tin DNS**: DNS server có thể được cấu hình để cập nhật thông tin về tên miền và địa chỉ IP tương ứng. Các thay đổi này có thể được thực hiện bởi quản trị viên mạng hoặc tự động thông qua các công cụ quản lý DNS.
- **Tăng tốc độ truy cập**: DNS server cũng có thể được sử dụng để tăng tốc độ truy cập cho người dùng bằng cách lưu trữ thông tin DNS trong bộ nhớ đệm. VD: khi truy vấn DNS là gì được thực hiện, DNS server sẽ truy cập thông tin từ bộ nhớ đệm trước, nếu có, thay vì thực hiện truy vấn đến các máy chủ DNS khác.
- **Bảo mật thông tin**: DNS server có thể được cấu hình để đảm bảo tính bảo mật của thông tin DNS. Các tính năng bảo mật bao gồm chữ ký số, mã hoá và xác thực người dùng để đảm bảo rằng thông tin DNS là gì được truyền tải an toàn và không bị đánh cắp.

## 3. Cách thức hoạt động của DNS

Mỗi nhà cung cấp dịch vụ Internet (ISPs) sẽ hoạt động và duy trì từng **DNS server riêng**. Khi người dùng muốn tìm kiếm địa chỉ website thì máy chủ DNS sẽ phân giải tên miền và trả về địa chỉ IP tương ứng với nhu cầu tìm kiếm.

Trong đó **INTERNIC** sẽ làm nhiệm vụ tổ chức, quản lý tên miền và các máy chủ DNS trên không gian mạng. INTERNIC sẽ thực hiện nhiệm vụ cụ thể là quản lý các tên miền đã đăng ký và tên miền đăng ký mới trên Internet.

Tuy nhiên, INTERNIC sẽ không tham gia vào quá trình phân giải tên miền.

DNS server có khả năng truy vấn nhiều DNS server khác nhau để có thể hoàn thành nhiệm vụ phân giải tên miền trên hệ thống. Đồng thời cũng có thể được dùng để lưu trữ các tên miền đã được phân giải thành địa chỉ IP để xử lý tốc độ cho những yêu cầu phân giải sau này.

>(Số lượng tên miền được lưu trữ trên DNS server sẽ tuỳ thuộc vào quy mộ của từng máy chủ)

Trong mỗi DNS server có hai nhiệm vụ chính:
- Phân giải tên miền thành địa chỉ IP cho các máy tính trong miền mà nó đang quản lý.
- Trả lời và phản hồi các yêu cầu phân giải tên miền từ hệ thống máy chủ bên ngoài cho tên miền mà DNS server đang quản lý.

## 4. Một số loại bản ghi (record) trên DNS server
**A Record**: 
- A record (Address record) được sử dụng để lưu trữ thông tin về địa chỉ IP của một tên miền cụ thể. Đây được xem là một bản ghi đơn giản, được dùng phổ biến trên thị trường và thực hiện nhiệm vụ trỏ tên về website để tới một địa chỉ IP cụ thể.
- Mỗi tên miền có thể có nhiều bản ghi A khác nhau, nhằm hỗ trợ tính sẵn sàng và chia sẻ tài nguyên trên máy chủ. Ngoài ra, khi sử dụng bản ghi A, ta có thể đổi tên mới dễ dàng hơn hay thêm **Time to live** (thời gian tự động tải lại bản ghi) và Points to để chỉ tới IP mong muốn.

**CNAME Record**:
- CNAME record (Canonical Name record) được sử dụng để tạo ra một tên miền thay thế (alias) cho một tên miền khác.
- CNAME record cung cấp cách thức để liên kết một tên miền với một tên miền khác mà có cùng địa chỉ IP, giúp tăng tính sẵn sàng và dễ dàng quản lý các tên miền.

**MX Record**:
- MX Record là bản ghi dùng để lưu trữ thông tin về server thư điện tử (mail server), được sử dụng để nhận và gửi email cho một tên miền cụ thể.
- Khi một email được gửi đến một địa chỉ email thuộc tên miền cụ thể, server thư điện tử của người gửi sẽ sử dụng MX record để phân giải tên miền và xác định địa chỉ IP của server thư điện tử tương ứng. Sau đó, email sẽ được gửi đến server thư điện tử này để tiếp tục xử lý và chuyển tiếp đến người nhận.
- Mỗi tên miền có thể có nhiều bản ghi MX khác nhau, nhằm hỗ trợ tính sẵn sàng cao hơn (thậm chí là TTL) và chi sẻ tải trên nhiều server thư điện tử.

**TXT Record**:
- TXT record đảm nhiệm vai trò chứa các thông tin định dạng văn bản của tên miền. Bản ghi này có thể thêm được host mới, thêm giá trị **TXT**, **TTL** và **Points to**.

**AAA Record**:
- AAA record (IPv6 Address record) được sử đụng để lưu trữ thông tin về địa chỉ IPv6 của một tên miền cụ thể.
- Địa chỉ IPv6 là phiên bản mới hơn của địa chỉ IP và được sử dụng để định danh cho các thiết bị trên mạng Internet.
- Mỗi tên miền có thể có nhiều bản ghi AAAA khác nhau nhằm hỗ trợ tính sẵn sàng và chia sẻ tải trên nhiều máy chủ.

**NS Record**:
- NS record (Name server record) là bản ghi dùng để lưu trữ thông tin về tên miền của DNS server chịu trách nhiệm cho một tên miền cụ thể nào đó.
- Mỗi tên miền có thể có nhiều máy chủ DNS khác nhau, nhằm hỗ trợ tính sẵn sàng cao hơn và chia sẻ tải trên nhiều máy chủ. Sử dụng bản ghi NS có thể tạo Name Server, TTL và cả host mới.
- Khi một trình duyệt hoặc ứng dụng yêu cầu truy cập đến một tên miền cụ thể, DNS server sẽ sử dụng bản ghi NS để tìm máy chủ DNS chịu trách nhiệm cho tên miền này. Sau đó DNS server sẽ tiếp tục sử dụng các bản ghi DNS khác để phân giải tên miền thành địa chị IP tương ứng.

**SRV Record**:
- SRV record được biết đến như một bản ghi đặc biệt dùng để chỉ định chính xác về thông tin của các dịch vụ mạng được cung cấp bởi một tên miền nào đó.
- SRV record được sử dụng chủ yếu trong các ứng dụng dịch vụ mạng như VoIP (Voice over Internet Protocol), LDAP (Lightweight Directory Access Protocol) và XMPP (Extension Message and Presence Protocol) để tìm kiếm các máy chủ cung cấp dịch vụ cụ thể cho một tên miền.

## 5. Phân loại DNS server
**Root Name Server**
Root Name Server (máy chủ gốc DNS) là một tập hợc các máy chủ DNS trên toàn cầu, chịu trách nhiệm cho việc phân giải tên miền trên mạng internet.

Các máy chủ này được duy trì bởi các tổ chức quản lý tên miền quốc tế, bao gồm ICANN (Internet Corporation for Assigned Names and Numbers) và Verisign.

Root Name Server cung cấp danh sách các tên miền cấp cao nhất trên internet (top-level domain), như .com, .org, .net, .edu, .gov, .mil và các tên miền quốc gia như .us, .uk, .vn,..

Root Name Server không chứa thông tên về các tên miền cụ thể, mà chỉ cung cấp thông tin về các máy chủ DNS cấp cao hơn để tiếp tục phân giải tên miền.

Cơ chế hoạt động của Root Name Server cụ thể như sau: Khi một trình duyệt hoặc ứng dụng truy cập một tên miền cụ thể, DNS resolver sẽ gửi yêu cầu đến một trong các Root Name Server để xác định các máy chủ DNS cấp cao hơn cho tên miền đó. Sau đó DNS resolver sẽ tiếp tục gửi yêu cầu đến các máy chủ DNS cấp cao hơn cho đến khi tìm thấy máy chủ chứa thông tin về tên miền cụ thể và trả về địa chỉ IP tương ứng.

**Local Name Server**
Local Name Server là một máy chủ DNS được cấu hình trên mạng nội bộ của một tổ chức hoặc doanh nghiệp, giúp hỗ trợ quản lý tên miền và phân giải tên miền cụ thể và trả về địa chỉ IP tương ứng.

Local Name Server hoạt động bằng cách lưu trữ các bản ghi DNS cho các tên miền được sử dụng thường xuyên trên mạng nội bộ, giúp giảm thiểu thời gian phản hồi và tăng cường tính sẵn sàng khi truy cập các tài nguyên trên mạng.

## 6. Cách thức hoạt động của DNS Server

Bước 1: Khi máy khách muốn truy cập và website của example.com, nó sẽ phải gửi yêu cầu tìm địa chỉ IP của tên miền example.com đến máy chủ tên miền cục bộ.

Bước 2: máy chủ miền cục bộ sẽ thực hiện rà soát các cơ sỏ dữ liệu để xem có những thông tin nào khác tương ứng IP với tên miền example.com không. Nếu không sẽ nhanh chóng tả IP của example.com cho máy khách.

Trường hợp nếu rà soát không phả hiện dữ liệu liên quan đến tên miền example.com, máy chủ miền cục bộ sẽ gửi yêu cầu đến Root Name server.

Bước 3: Root Name Server không chứa thông tin về địa chỉ IP của example.com, mà chỉ chứa thông tin về máy chủ quản lý tên miền .com

Khi đó, Root Name Server sẽ gửi thông tin về địa chỉ máy chủ quản lý tên miền .com cho Local Name Server.

Bước 4: Lúc này, máy chủ tên miền cục bộ sẽ gửi yêu cầu tìm kiếm đến máy chủ quản lý tên miền .com để tìm địa chỉ của example.com

Bước 5: Máy chủ quản lý tên miền .com có chứa thông tin về tất cả các tên miền .com, khi tìm được thông tin, máy chủ sẽ trả lại địa chỉ IP cho Local Name Server.

Bước 6: Local Name Server sẽ gửi thông tin về tên miền đến cho máy khách, sau đó máy khách khách sẽ sử dụng địa chỉ IP được cấp để truy cập tới server example.com

## 7. Nguyên tắc vận hành DNS server

DNS server sẽ có cơ chế hoạt động tương tự với hệ thống khách, nó cũng sẽ có những nguyên tắc hoạt đọng nhất định và muốn sử dụng, ta phải hiểu được nguyên lý hoạt động.

Sau đây là nội dung khái quát về nguyên tắc làm việc của DNS server:
- Mỗi nhà cung cấp dịch vụ sẽ có hệ thống DNS riêng để phân giải tên miền và đảm bảo cho người dùng có thể truy cập vào các trang web của doanh nghiệp nhanh chóng nhất.
- Khi người dùng truy cập vào một trang web, DNS server sẽ phân giải tên miền của website đó tại chính tổ chức quản lý website, không phải ở các tổ chức hay nhà cung cấp dịch vụ khác.
- INTERNIC là tổ chức được thành lập với mục đích đăng ký tên miền của internet và theo dõi các DNS server tương ứng. Tuy nhiên, INTERNIC không thực hiện phân giải tên miền mà chỉ quản lý tất cả các DNS trên server. DNS có khả năng truy vấn các DNS server khác để có được tên miền đã được phân giải, nó có hai chức năng chính là phân giải tên miền và trả lời các yêu cầu của các DNS server khác.
- Mỗi DNS server sẽ quản lý và chịu trách nhiệm phân giải tên miền từ các máy bên trong tên miền đến các địa chỉ internet mà nó quản lý. DNS server cũng có trách nhiệm trả lời các yêu cầu từ các DNS server khác đang cố gắng phân giẩi tên miền mà nó quản lý. Tất cả các nhà cung cấp dịch vụ đều có hệ thống DNS riêng để đảm bảo an toàn và hiệu quả cho người dùng, và INTERNIC là tổ chức quản lý các tên miền và DNS server trên toàn thế giới.

## 8. Hướng dẫn cách sử dụng DNS server:

Mỗi DNS server có tốc độ hoạt động khác nhau, vì vật người dùng có thể tự do lựa chọn DNS server phù hợp với thiết bị.

Tuy nhiên nếu người dùng sử dụng DNS của nhà cung cấp mạng thì không cần phải điền địa chỉ DNS là gì khi kết nối với Internet. Ngược lại, khi sử dụng máy chủ khác, người dùng sẽ phải điền địa chỉ cụ thể của máy chủ mà họ muốn sử dụng.

## 9. Tại sao DNS dễ bị tấn công

DNS là một trong những dịch vụ internet quan trọng và cũng không thể tránh khỏi các cuộc tấn công.

Mục đích của những cuộc tấn công là ngắt kết nối hoặc làm gián đoạn các trang web mà người dùng đang truy cập, đây là dạng tấn công từ chối dịch vụ (DoS). Hiện tại có hai dạng máy chủ tên miền là: máy chủ tên miền có thẩm quyền và máy chủ tên miền đệ quy.

Trong đó máy chủ đệ quy có vai trò trả lời các truy vấn DNS của người dùng khi sử dụng Internet, đây cũng là nơi lưu trữ các kết quả phản hồi của DNS trong thời gian dài vì vậy thường sẽ được hacker nhắm để tấn công nhằm đánh cắp cơ sở dữ liệu của người dùng.

Các hacker có thể mò ra các điểm yếu của DNS, sau đó có thể chiếm quyền điều khiển DNS để điều hướng người dùng đến các trang web độc hại hoặc đánh cắp thông tin quan trọng của người dùng hoặc doanh nghiệp bằng cách sử dụng kỹ thuật DNS tunneling.

Một dạng tấn công khác là man-in-the-middel (người trung gian). Hacker có thể can thiệp trực tiếp vào các dịch vụ như Voice Over IP (VoIP), đánh cắp email, chuyển hướng trang web, đánh cắp thông tin tài khoản thẻ, thông tin mật hay mật khẩu.

## 10. Rò rỉ DNS

### Khái niệm

Khi thông tin DNS bị rò ri, các bên thứ ba có thể thu thập và sử dụng thông tin đó để theo dõi và phân tích hành vi trực tuyến của khách hàng.

Rò rỉ DNS là hiện tượng khi thông tin truy vấn DNS của người dùng bị rò rỉ ra ngoài mạng Internet, thường là do thiết bị mạng hay phần mềm đang sử dụng không được cấu hình chính xác hoặc bị lỗ hổng bảo mật.

Cụ thể khi kết nối dịch vụ DNS để kết nối với Domain để nhập và giữ địa chỉ IP của máy chủ dùng để lưu trữ website. Nhờ nguyên lý hoạt động này mà trang web có thể được tìm kiếm trên trình duyệt.

### Nguyên nhân:

Có nhiều nguyên nhân dẫn đến rò rỉ DNS, tuy nhiên chủ yếu xuất phát từ vấn đề lỗi kết nối của VPN không được cấu hình đúng cách.

Những sự cố rò rỉ có thể xuất hiện ở tất cả các hệ điều hành,.. Chỉ cần là thiết bị có kết nối với VPN đều có thể bị rò rỉ DNS. Bên cạnh đó, nguyên nhân rò rỉ DNS là gì sẽ tuỳ thuộc vào nhà cung cấp VPN nhưng phổ biến nhất là liên quan đến cấu hình

Trường hợp cấu hình đúng thì máy tính sẽ kết nối với VPN bằng cách sử dụng IPS và các DNS server của IPS (Internet Service Provider) tương ứng.

Sau khi kết nối thành công nó sẽ sử dụng DNS của VPN và hệ thống máy chủ đó phải đảm bảo đang cùng truy cập chung một mạng với máy chủ VPN. Điều này sẽ đảm bảo mã hóa được lưu lượng của DNS. 

Tuy nhiên, nếu mô hình này không thể tuân theo do gặp sự cố bất kỳ nào đó. Thì lúc này lưu lượng DNS có thể sẽ thoát khỏi VPN Tunnel và bên ngoài có thể dễ dàng nhìn thấy được thông tin, dữ liệu ở bên trong. Hậu quả là các yêu cầu DNS sẽ không được mã hóa và có thể tất cả DNS sẽ không hỗ trợ cho việc mã hóa theo yêu cầu của DNS.

