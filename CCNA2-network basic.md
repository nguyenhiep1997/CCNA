## network basic.

> tài liệu tham khảo: [internet](https://google.com)

> Người thực hiện: Nguyễn Văn Hiệp 

> cập nhật lần cuối: 26/10/2017

>---

### Mục Lục:

> [1. Chức năng của Tầng Transport.](#1)

> [2. Hai kiểu kết nối ở Tầng Transport. So sánh hai kiểu kết nối đó. Đặc điểm của các giao thức tương ứng với từng kiểu kết nối.](#2)

 - [2.1 UDP](#2.1)

 - [2.2 TCP](#2.2)

> [3. Quá trình three-ways handshake (Bắt tay 3 bước).](#3)

---------------

### 1. chức năng của tầng Transport <a name="1"></a>

 - lớp transport đảm nhận các nhiệm vụ :
 <ul>
 <li>truyền tải các session trao đổi dữ liệu của lớp applycation qua một kết nối end - to - end</li>
 <li>thực hiện phân mảnh dữ liệu, đóng gói các PDU của lớp applycation ở trên vào các đơn vị dữ liệu lớp 4</li>
 <li>việc truyền tải của cacs giao thức lớp transport có thể theo phương thức connecttion - oriented hoặc connectionles </li>
 </ul>

 - có hai giao thức nổi bật của chồng giao thức TCP/IP hoạt động ở tầng 4 của mô hình OSI là UDP và TCP. ta sẽ đi sâu vào tìm hiểu đặc điểm của 2 tầng này.

### 2. hai kiểu kết nối ở tầng transport. So sánh hai kiểu kết nối đó. Đặc điểm của các giao thức tương ứng với từng kiểu kết nối.<a name="2"></a>

#### 2.1 UDP <a name="2.1"></a>

 - UDP ( user datagram protocol) là một giao thức truyền tải connectionless điển hình . một giao thức connectionless sẽ không thực hiện thao tác xây dựng kết nối trước khi truyền dữ liệu mà thực hiện truyền ngay khi có dữ liệu cần truyền ( gọi là kiểu truyền best effort - truyền tổng lực) ngoài ra phương thức truyền connectionless cũng không sử dụng các phương pháp đảm bảo độ tin cậy như báo nhận hay điều khiển luồng (flow control). connectionless không thực hiện các biện pháp đánh số thứ tự cho các đơn vị được truyền. ... 

 - với đặc điểm này UDP sẽ thực hiện truyền tải rất nhanh cho dữ liệu của lớp ứng dụng tuy nhiên, hoạt động truyền tải này lại không có độ tin cậy cao và dễ bị lỗi 

 - đây là hình ảnh của 1 UDP datagram 

 ![](https://voer.edu.vn/file/2611)

 - có thể thấy cấu trúc của UDP header khá đơn giản, phù hợp cho phương thức truyền best - effort connectionless . trong đó :
 <ul>
 <li>các trường source port và destination port : cho phép định đanh 1 session của một ứng dụng nào đó chạy trên UDP. có thể coi port chính là địa chỉ của lớp 4.</li>
 <li>UDP length: cho biết độ dài của toàn bộ gói tin UDP datagram</li>
 <li>UDP checksum : thực hiện kiểm tra lỗi cho toàn bộ gói tin UDP </li>
 <li>data: dữ liệu lớp trên được đóng gói vào UDP datagram đang xét </li>
 </ul>

#### 2.2 TCP <a name="2.2"></a>

 - ngược lại với UDP , TCP ( transmisstion control protocol) . là giao thức truyền tải connection-oriented  điển hình . một giao thức connection-oriented mang những đặc điểm sau.
 <ul>
 <li>phải thực hiện thiết lập kết nối với đầu xa trước khi thực hiện truyền dữ liệu . tiến trình thiết lập kết nối ở TCP được gọi là tiến trình bắt tay 3 bước</li>
 <li> phải có cơ chế báo nhận khi truyền dữ liệu . mọi segment được gửi đi đều phải được bật báo nhận( acknowledge hay gọi tắt là ack) các segment gửi đi mà không báo nhận được xem như bị lỗi khi truyền đi và sẽ được thực hiện truyền lại </li>
 <li>phải thực hiện cơ chế đánh số thứ tự  (sequencing) cho các đơn vị dữ liệu được truyền </li>
 <li>phải thực hiện các cơ chế điều khiển luồng thích hợp để tránh nghẽn xảy ra</li>
 </ul>
 
 - ngoài ra, một kết nối TCP có thể xem là 1 cặp đương kết nối luận lý giữa hai host đầu cuối. mỗi đường phục vị cho một hướng truyền dữ liệu . ta nói TCP hỗ trợ kiểu truyền tải full duplex.

 - TCP củng cung cấp các dịch vụ sửa lỗi, trong đó phía nhận có thể yêu cầu phía gửi truyền lại một segment nào đó. 

 đây là một gói tin TCP thông thường ( được gọi là TCP segment).

 ![](http://intronetworks.cs.luc.edu/1/html/_images/tcp_header.png) 

 - trong đó các trường là :
 <ul>
 <li>Source port Số hiệu của cổng tại máy tính gửi.</li>
 <li>Destination port Số hiệu của cổng tại máy tính nhận</li>
 <li>Sequence number Trường này có 2 nhiệm vụ. Nếu cờ SYN bật thì nó là số thứ tự gói ban đầu và byte đầu tiên được gửi có số thứ tự này cộng thêm 1. Nếu
không có cờ SYN thì đây là số thứ tự của byte đầu tiên.</li>
 <li>Acknowledgement number Nếu cờ ACK bật thì giá trị của trường chính là số thứ tự gói tin tiếp theo mà bên nhận cần</li>
 <li>Data offset Trường có độ dài 4 bít qui định độ dài của phần header (tính theo đơn vị từ 32 bit). Phần header có độ dài tối thiểu là 5 từ (160 bit) và tối đa là 15 từ (480 bit)</li>
 <li>Reserved Dành cho tương lai và có giá trị là 0.</li>
 <li>Flags (hay Control bits) Bao gồm 6 cờ:
• URG Cờ cho trường Urgent pointer
• ACK Cờ cho trường Acknowledgement
• PSH Hàm Push
• RST Thiết lập lại đường truyền
• SYN Đồng bộ lại số thứ tự
• FIN Không gửi thêm số liệu
</li>
 <li>Window Số byte có thể nhận bắt đầu từ giá trị của trường báo nhận (ACK)</li>
 <li>Checksum16 bít kiểm tra cho cả phần header và dữ liệu. Phương pháp sử dụng được mô tả trong RFC 793</li>
 <li>16 bít kiểm tra cho cả phần header và dữ liệu. Phương pháp sử dụng được mô tả trong RFC 793</li>
 <li>16 bít của trường kiểm tra là bổ sung của tổng tất cả các từ 16 bít trong gói tin. Trong trường hợp số octet (khối 8 bít) của header và dữ liệu là lẻ thì octet cuối được bổ sung với các bít 0. Các bít này không được truyền. Khi tính tổng, giá trị của trường kiểm tra được thay thế bằng 0</li>
 <li>Các địa chỉ nguồn và đích là các địa chỉ IPv4. Giá trị của trường protocol là 6 (giá trị dành cho TCP, xem thêm: Danh sách số hiệu giao thức IPv4). Giá trị của trường TCP length field là độ dài của toàn bộ phần header và dữ liệu của gói TCP</li>
 <li>Urgent pointer Nếu cờ URG bật thì giá trị trường này chính là số từ 16 bít mà số thứ tự gói tin (sequence number) cần dịch trái.</li>
 <li>Options Đây là trường tùy chọn. Nếu có thì độ dài là bội số của 32 bít.</li>
 <li>data: dữ liệu lớp trên</li>
 </ul>

#### so sánh giữa TCP và UDP

 - Giống nhau : đều là các giao thức mạng TCP/IP, đều có chức năng kết nối các máy lại với nhau, và có thể gửi dữ liệu cho nhau…

 - Khác nhau (cơ bản): 
các header của TCP và UDP khác nhau ở kích thước (20 và 8 byte) nguyên nhân chủ yếu là do TCP phải hộ trợ nhiều chức năng hữu ích hơn(như khả năng khôi phục lỗi). UDP dùng ít byte hơn cho phần header và yêu cầu xử lý từ host ít hơn
TCP :
– Dùng cho mạng WAN
– Không cho phép mất gói tin
– Đảm bảo việc truyền dữ liệu
– Tốc độ truyền thấp hơn UDP
UDP:
– Dùng cho mạng LAN
– Cho phép mất dữ liệu
– Không đảm bảo.
– Tốc độ truyền cao, VolP truyền tốt qua UDP

 - TCP hoạt động theo hướng kết nối (connection-oriented), trước khi truyền dữ liệu giữa 2 máy, nó thiết lập một kết nối giữa 2 máy theo phương thức “bắt tay 3 bước (three-way-hand-shake)” bằng cách gửi gói tin ACK từ máy đích sang máy nhận, trong suốt quá trình truyền gói tin, máy gửi yêu cầu máy đích xác nhận đã nhận đủ các gói tin đã gửi, nếu có gói tin bị mất, máy đích sẽ yêu cầu máy gửi gửi lại, thường xuyên kiểm tra gói tin có bị lỗi hay ko, ngoài ra còn cho phép qui định số lượng gói tin được gửi trong một lần gửi (window-sizing), điều này đảm bảo máy nhận nhận được đầy đủ các gói tin mà máy gửi gửi đi –> truyền dữ liệu chậm hơn UDP nhưng đáng tin cậy hơn UDP

 - UDP hoạt động theo hướng ko kết nối (connectionless), ko y/c thiết lập kết nối giữa 2 máy gửi và nhận, ko có sự đảm bảo gói tin khi truyền đi cũng như ko thông báo về việc mất gói tin, ko kiểm tra lỗi của gói tin
–> truyền dữ liệu nhanh hơn UDP do cơ chế hoạt động có phần đơn giản hơn tuy nhiên lại ko đáng tin cậy bằng TCP

 - TCP và UDP là 02 Protocol hoạt động ở lớp thứ 04 (Transport Layer) của mô hình OSI và ở lớp thứ 02 (Transport Layer) mô hình TCP/IP (xin lưu ý: mô hình TCP/IP (TCP/IP Model ) khác hoàn toàn với chồng giao thức TCP/IP (TCP/IP Suite)

 - TCP là giao thức truyền tin cậy và phải bắt tay ba bước (three-way-hand-shake) nên khi Server không nhận được bất kỳ gói tin ACK từ Client gửi trả lời thì Server sẽ gửi lại gói tin đã thất lạc. Server sẽ gửi cho đến khi nhận được ACK của Client mới thôi => Điều này cũng là một nhân tố làm chậm và ngốn băng thông đường truyền.

 - Ý  muốn nói lên TCP dành cho các ứng dụng secure. đối với các ứng dụng không cần secure thì dùng UDP là được, lợi hơn về performance. finding DC thì không cần secure, LDAP tất nhiên cần secure.

 - Mặc dù tổng lượng lưu thông của UDP trên mạng thường chỉ vài phần trăm, nhưng có nhiều ứng dụng quan trọng dùng UDP, bao gồm DNS, SNMP, DHCP và RIP, dễ thấy hơn là điện thoại IP, xem truyền hình trực tiếp…Thực tế UDP dùng nhiều cho việc truyền tải Games Online. Như các bạn biết đó…việc nâng cấp sửa lỗi games các nhà quản trị Games và Bảo mật thường xuyên cập nhật bản vá lỗi của games, hoặc các thông tin dẫn truyền trong games đều dùng UDP rất nhiều. Nói TCP bảo mật hơn thì cũng đúng, nhưng UDP cũng rất bảo mật điều này phụ thuộc vào mức độ mã hóa của các Package trong liên kết truyền thông. Nghiên cứu thêm trong An Toàn Bảo Mật Thông Tin…

 - Để biết máy tính có dùng UDP hay TCP thi bạn có thể thao khảo Sys Tools…những công cụ kiểm tra hệ thống và xem trên Router, check Port Connection….(Tất cả nằm trên anh Google…)

 - “Tiền nào của nấy”. Sử dụng TCP có rất nhiều ưu điểm, nhưng ngược lại chi phí đắt.  Khi mà ứng dụng không yêu cầu quá cao về chất lượng, có thể chấp nhận việc mất thông tin và trễ về thời gian (như điện thoại internet, media…) thì việc sử dụng UDP thay vì TCP sẽ tiết kiệm được nhiều chi phí.

 – Ngoài ra:

 + UDP có độ trễ nhỏ, do không có giai đoạn thiết lập đường truyền

  + UDP nó đơn giản: Phía gửi và phía nhận không phải ghi nhớ trạng thái gửi/nhận.

 + small segment header

 + Không có cơ chế kiểm soát tắc nghẽn, do đó bên gửi có thể gửi dữ liệu với tốc độ tối đa

Các bạn có thể thấy UDP được sd nhiều trong : NTP, DNS, MDNS, BOOTP, DHCP, SysLog, NFS, ISAKMP, Cisco HSRP, Cisco MGCP,…

Hai ứng dụng phổ biến là Yahoo Messenger sử dụng TCP/IP và Skype sử dụng UDP.


### 3. quá trình bắt tay 3 bước <a name="3"></a>

 ![](https://i.imgur.com/Epemo86.png)

 - giả sử host A muốn truyền dữ liệu cho host B thông qua một kết nối TCP. trước khi thực hiện truyền host A phải thiết lập kết nối với host B. việc này được tiến hành thông qua tiến trình bắt tay 3 bước . 

 - 1. host A gửi cho host B segment đầu tiên, segment này có cờ SYN được bật lên 

 - giả sử rằng host A thiết lập cho segment này số thứ tự sequence là 100 segment đầu tiên này không chứa dữ liệu nên không có phần data , tuy nhiên số lượng byte dữ liệu vẫn được tính là 1 byte cho hoạt động gửi cờ SYN.

 - 2.  khi host B nhận được cờ SYN từ đầu bên kia , thực hiện hồi đáp lại môth TCP segment . segment này có cờ SYN và cờ ACK cùng được bật lên .

 - giả sử rằng host B thiết lập cho segment này số thứ tự là 300 .segment trà lời từ host B này củng không có dữ liệu nhưng vẫn tính là 1 byte cho data . khi hồi đáp, host B củng cần chỉ rõ trong trường ACK sequence số thứ tự củ byte tiếp theo mà nó muốn nhận từ host A như đã nói segment SYN do A gửi qua được tính byte là 1 nên B mong muốn nhận byte tiếp theo là byte thứ 101 từ A do đó ACK là 101 .

 - 3. khi host A nhận được segment hồi đáp từ host B nó gửi segment có bật cờ ACK về lại cho B

 - trường ACK sequence trong segment A gửi cho B sẽ chỉ rõ số thứ tự của byte tiếp theo mà nó muốn nhận từ B là byte 301 .

 - sau khi 3 bươc này được hoàn tất, kết nối TCP đã được thiết lập giữa host A và host B lúc này hai host có thể truyền dữ liệu cho nhau.

#### nhận diện giao thức applycation trên layer 4 header 

 - khi một thực thể lớp 4 đọc thông tin trên TCP hay UDP header , nó có thể xác định dữ liệu đang đóng gói bên trong TCP segment hay UDP datagram là của giao thức applycation nào mà không cần mở gói để xem nội dung bên trong. đê thực hiện điều này chồng giao thức TCP/IP sử dụng tham số port trong TCP/UDP header để nhận diện giao thức lớp trên đang được đóng gói trong phần data . ví dụ 
 - HTTP sử dụng port 80, 81
 - HTTPS sử dụng port 443
 - DNS sử dụng port 53
 - SSH sử dụng port 22
 - telnet sử dụng port 23
 - FTP sử dụng port 20,21
 - SMTP sử dụng port 25
