 ## network basic.

> tài liệu tham khảo: [internet](https://google.com)

> Người thực hiện: Nguyễn Văn Hiệp 

> cập nhật lần cuối: 24/10/2017

>---

### Mục Lục:

> [1. Tìm hiểu về Mạng căn bản](#1)

>  - [1.1 Network là gì?](#1.1)

>  - [1.2 lợi ích?](#1.2)

>  - [1.3  Các đặc trưng?](#1.3)

>  - [1.4 Các loại Topology?](#1.4)


> [2. Mô hình OSI: Hoàn cảnh ra đời? Các lớp của mô hình? Chức năng của từng lớp mô hình?](#2)

>  - [2.1 hoàn cảnh ra đời?](#2.1)

>  - [2.2 các lớp của mô hình và chức năng của từng lớp?](#2.2)

> [3.  Mô hình TCP/IP: Các lớp? So sánh với mô hình OSI.](#3)

---------------


### 1. tìm hiểu về mạng căn bản <a name="1"></a>

 - Với sự phát triển của khoa học và kỹ thuật, hiện nay các mạng máy tính đã phát triển một cách nhanh chóng và đa dạng cả về quy mô,hệ điều hành và ứng dụng. Do vậy việc nghiên cứu chúng ngày càng trở nên phức tạp.

 - Để có thể thiết kế,quản trị một mạng máy tính,trước hết phải hiểu mạng máy tính đó hoạt động như thế nào. Thông thường,khi nghiên cứu về một mảng kiến thức mới,việc đầu tiên phải làm là nắm chắc các khái niệm tổng quát,căn bản ban đầu. Bằng cách này,người học mới có thể tự đi sâu tìm hiểu các chi tiết bên trong.

#### 1.1 network là gì <a name ="1.1"></a>

 - Mạng máy tính là một nhóm các máy tính và thiết bị ngoại vi kết nối với nhau thông qua các phương tiện truyền dẫn như cáp xoắn,cáp quang, sóng điện từ,tia hồng ngoại… để chia sẻ dữ liệu cho nhau. Dữ liệu truyền từ máy này sang máy khác đều là các bit nhị phân 0 và 1, sau khi biến đổi thành điện thế hoặc sóng điện từ,sẽ được truyền qua môi trường truyền dẫn bên dưới.

 - Mạng máy tính có nhiều ích lợi :
 <ul>
 <li>Tiết kiệm được tài nguyên phần cứng</li>
 <li>Giúp trao đổi dữ liệu dễ dàng</li>
 <li>Chia sẻ ứng dụng</li>
 <li>Tập trung dữ liệu,dễ bảo mật,dễ sao lưu</li>
 <li>Sử dụng internet….</li>
 </ul>

##### CÁC LOẠI MẠNG MÁY TÍNH THÔNG DỤNG :

 - Mạng máy tính có nhiều loại,tùy thuộc vào vị trí địa lý,tốc độ đường truyền,tỉ lệ lỗi bit trên đường truyền, đường đi của dữ liệu trên mạng, dạng chuyển giao thông tin. Nhìn  chung,các mạng máy tính có thể được phân biệt làm các loại sau :

 1) Mạng cục bộ :

– Mạng LAN (Local Area Network – còn gọi là mạng cục bộ) là một nhóm các máy tính và thiết bị altalttruyền thông mạng được kết nối với nhau trong một khu vực nhỏ như  tòa nhà cao ốc, trường đại học, khu giải trí…
![](http://www.vnpro.vn/wp-content/uploads/2016/11/LAN_VnPro.jpg)

- Mạng LAN có các đặc điểm sau :

–       Băng thông lớn để có khả năng chạy các ứng dụng trực tuyến như xem phim,giải trí,hội thảo qua mạng.

–       Kích thước mạng bị giới hạn bởi thiết bị

–       Chi phí thiết kế,lắp đặt mạng LAN rẻ

–       Quản trị đơn giản

2) Mạng  đô thị :

Mạng đô thị MAN (Metropolitan Area Network) gần giống như mạng LAN nhưng giới hạn kích thước của nó là một thành phố hay một quốc gia. Mạng MAN kết nối các mạng LAN lại với nhau thông qua môi trường  truyền dẫn và các phương  thức truyền thông khác nhau.

Mạng MAN có các đặc điểm sau :

–       Băng thông ở mức trung bình,đủ để phục vụ các ứng dụng cấp thành phố hay quốc gia như chính phủ điện tử,thương mại điện tử,các ứng dụng của các ngân hàng…

–       Do MAN kết nối nhiều LAN nên việc quản trị sẽ gặp khó khăn hơn,đồng thời độ phức tạp cũng tăng theo.

–       Chi phí các thiết bị MAN tương đối đắt tiền

3) Mạng diện rộng :

Mạng diện rộng WAN (Wide Area Network) có phạm vi bao phủ một vùng rộng lớn,có thể là quốc gia,lục địa hay toàn cầu. Mạng WAN thường là mạng của các công ty đa quốc gia hay toàn cầu. Mạng WAN lớn nhất hiện nay là mạng Internet. Mạng WAN là tập hợp của nhiều mạng LAN và MAN được nối lại với nhau thông qua các phương tiện như vệ tinh ,sóng vi ba,cáp quang,điện thoại ….

![](http://www.vnpro.vn/wp-content/uploads/2016/11/WAN_VnPro.gif)

 - Mạng WAN có các đặc điểm sau :

–       Băng thông thấp,dễ mất kết nối,thường chỉ phù hợp với các ứng dụng online như e – mail ,ftp,web….

–       Phạm vi hoạt động không giới hạn

–       Do kết nối nhiều LAN và MAN với nhau nên mạng rất phức tạp và các tổ chức toàn cầu phải đứng ra quy định và quản lý

–       Chi phí cho các thiết bị và công nghệ WAN rất đắt

**Chú ý là việc phân biệt mạng thuộc loại LAN, MAN hay WAN chủ yếu dựa trên khoảng cách vật lý và chỉ máng tính chất ước lệ .**

##### các thành phần cơ bản của mạng. 

 - một hệ thống mạng cơ bản nhất có thể bao gồm một số thành phần như sau :
 <ul>
 <li> các pc đầu cuối : các máy tính cá nhân hoạt động như là các điểm truy nhập đầu cuối, gửi và nhận dữ liệu về cho người dùng.</li>
 <li> các kết nối : mỗi kết nối được tạo thành từ một số thành phần để cho phép truyền dữ liệu từ thiết bị này sang thiết bị kia. một số thành phần cơ bản của kết nối như **card mạng** , **phương tiện truyền dẫn** hay **các đầu nối** </li>
 <li> ngoài ra các thiết bị còn được kết nối với các thiết bị tập trung khác như switch và router để thực hiện các chức năng như chuyển mạch và định tuyến các gói tin </li>
 </ul>

#### 1.2 lợi ích <a name="1.2"></a>

##### chức năng chia sẽ tài nguyên mạng.

 - kết nối mạng cho phép người dùng chia sẽ rất hiệu quả dữ liệu và các tài nguyên mạng. một số hoạt động chia sẽ trên mạng thường gặp trong mạng doanh nghiệp :
 <ul>
 <li>dữ liệu và các ứng dụng : thông qua kết nối mạng người dùng có thể chia sẽ dữ liệu qua mạng (ví dụ share file) hoặc cùng tham gia các ứng dụng qua mạng như họp trực tuyến hay chơi game ...</li>
 <li>chia sẽ tài nguyên phần cứng: một ví dụ cụ thể của hoạt động này là chia sẽ máy in thông qua các server máy in , kỹ thuật này cho phép một máy in có thể được sử dụng chung bởi nhiều người dùng trong mạng doanh nghiệp.</li>
 <li>hệ thống lưu trữ và backup : gồm các server lưu trữ, các thiết bị lưu trữ dùng chung... cho phép doanh nghiệp có thể thực hiện các giải pháp lưu trữ hiêu quả, giúp quản trị tốt cơ sở dữ liệu </li>
 </ul>
 
##### các ứng dụng người dùng 

 - có rất nhiều ứng dụng người dùng được thực hiện thông qua mạng. có thể kể ra một số ứng dụng chính như thư điện tử (mail) , trình duyệt web , nhắn tin , hội họp và làm việc trực tuyên , chia sẽ file ..... 
 các ứng dụng đó chia làm 3 loại :

1) các ứng dụng truyền file : do người dùng khởi tạo nhưng sẽ được thực hiện và hoàn tất bởi sự tương tác giữa các thiết bị mà không cần cự tương tác nào thêm của người sử dụng. đây là loại ứng dụng tương tác giữa thiết bị với thiết bị 

2) các ứng dụng tương tác : ví dụ như các hoạt động truy cập cơ sở dữ liệu hay truy vấn dữ liệu. người dùng thực hiện yêu cầu dữ liệu trên một server dữ liệu và phải chờ hồi đáp từ server đó .đây là các ứng dụng mà người dùng tương tác trực tiếp với thiết bị

3) ứng dụng thời gian thực : bao gồm các ứng dụng truyền thoại hoặc video qua mạng ( voip hoặc video) với các ứng dụng này người dùng tương tác trực tiếp với nhau theo thời gian thực thông qua các cuộc gọi điện thoại IP hoặc hội nghị truyền hình qua kết nối mạng. 

#### 1.3 Các đặc trưng? <a name="1.3"></a> 

 - khi nói đến một mạng người ta thường xem xét các đặc trưng sau của mạng:
 <ul>
 <li> **speed** cho biết mạng nhanh đến đâu trong hoạt động truyền dữ liệu. tốc độ của mạng được đo bằng đơn vị bps(bit per second) là số bit dữ liệu được truyền qua trong 1s </li>
 <li> **cost** chi phí để xây dựng và vận hành mạng , chi phí này có thể bao gồm chi phí mua sắm trang thiết bị , chi phí nâng cấp hệ thống , chi phí cho hoạt động vận hành , quản trị hệ thống đó </li>
 <li> **security** tính bảo mật của hệ thống mạng </li>
 <li> **availability** tính sẵn sàng của hệ thống là tính liên tục trong hoạt động truy cập và truyền dữ liệu</li>
 <li> **reliability** độ tin cậy của hệ thống , là khả năng truyền dữ liệu gây ít lỗi nhất có thể đảm bảo sự tin cậy về mặt chất lượng khi truyền dữ liệu</li>
 <li> **topology** sơ đồ mạng : bản đồ cho biết cách thức đấu nối giữa các thiết bị và hướng di chuyển của các luồng dữ liệu qua mạng.</li>
 </ul>

#### 1.4 các loại topology <a name="1.4"></a>

 - có hai topology có thể có cho một sơ đồ mạng: sơ đồ vật lý và sơ đồ luận lý .
 <ul>
 <li>sơ đồ vật lý là cách thức đấu nối giữa các thiết bị mạng với nhau </li>
 <li>sơ đồ luận lý cho biết cách thức dòng dữ liệu di chuyển giữa các thiết bị . có những trường hợp sơ đồ vật lý trùng với sơ đồ luận lý nhưng cũng có những trường hợp sơ đồ vật lý khác sơ đồ luận lý </li>
 </ul>
 - có nhiều cách đấu nối giữa các thiết bị, trong đó phổ biến nhất là 3 loại đấu nối : dạng bus, dạng sao (star topology) và dạng vòng ( ring topology)
 ![](https://i.imgur.com/zFfRAV2.png)

 1) dạng bus 
 - Trong dạng đường thẳng các máy tính đều được nối vào một đường dây truyền chính (bus). Đường truyền chính này được giới hạn hai đầu bởi một loại đầu nối đặc biệt gọi là terminator (dùng để nhận biết là đầu cuối để kết thúc đường truyền tại đây). Mỗi trạm được nối vào bus qua một đầu nối chữ T (T_connector) hoặc một bộ thu phát (transceiver). Khi một trạm truyền dữ liệu, tín hiệu được truyền trên cả hai chiều của đường truyền theo từng gói một, mỗi gói đều phải mang địa chỉ trạm đích. Các trạm khi thấy dữ liệu đi qua nhận lấy, kiểm tra, nếu đúng với địa chỉ của mình thì nó nhận lấy còn nếu không phải thì bỏ qua. Sau đây là vài thông số kỹ thuật của topology bus. Theo chuẩn IEEE 802.3 (cho mạng cục bộ) với cách đặt tên qui ước theo thông số: tốc độ truyền tính hiệu (1,10 hoặc 100 Mb/s); BASE (nếu là Baseband) hoặc BROAD (nếu là Broadband).

 - 10BASE5: Dùng cáp đồng trục đường kính lớn (10mm) với trở kháng 50 Ohm, tốc độ 10 Mb/s, phạm vi tín hiệu 500m/segment, có tối đa 100 trạm, khoảng cách giữa 2 tranceiver tối thiểu 2,5m (Phương án này còn gọi là Thick Ethernet hay Thicknet)

 - 10BASE2: tương tự như Thicknet nhưng dùng cáp đồng trục nhỏ (RG 58A), có thể chạy với khoảng cách 185m, số trạm tối đa trong 1 segment là 30, khoảng cách giữa hai máy tối thiểu là 0,5m. Dạng kết nối này có ưu điểm là ít tốn dây cáp, tốc độ truyền dữ liệu cao tuy nhiên nếu lưu lượng truyền tăng cao thì dễ gây ách tắc và nếu có trục trặc trên hành lang chính thì khó phát hiện ra. Hiện nay các mạng sử dụng hình dạng đường thẳng là mạng Ethernet và G-net.

 2) dạng vòng 

 - Các máy tính được liên kết với nhau thành một vòng tròn theo phương thức "một điểm - một điểm ", qua đó mỗi một trạm có thể nhận và truyền dữ liệu theo vòng một chiều và dữ liệu được truyền theo từng gói một. Mỗi gói dữ liệu đều có mang địa chỉ trạm đích, mỗi trạm khi nhận được một gói dữ liệu nó kiểm tra nếu đúng với địa chỉ của mình thì nó nhận lấy còn nếu không phải thì nó sẽ phát lại cho trạm kế tiếp, cứ như vậy gói dữ liệu đi được đến đích. Với dạng kết nối này có ưu điểm là không tốn nhiều dây cáp, tốc độ truyền dữ liệu cao, không gây ách tắc tuy nhiên các giao thức để truyền dữ liệu phức tạp và nếu có trục trặc trên một trạm thì cũng ảnh hưởng đến toàn mạng. Hiện nay các mạng sử dụng hình dạng vòng tròn là mạng Tocken ring của IBM.

 3) dạng sao 
 - Ở dạng hình sao, tất cả các trạm được nối vào một thiết bị trung tâm có nhiệm vụ nhận tín hiệu từ các trạm và chuyển tín hiệu đến trạm đích với phương thức kết nối là phương thức "một điểm - một điểm ". Thiết bị trung tâm hoạt động giống như một tổng đài cho phép thực hiện việc nhận và truyền dữ liệu từ trạm này tới các trạm khác. Tùy theo yêu cầu truyền thông trong mạng , thiết bị trung tâm có thể là một bộ chuyển mạch (switch), một bộ chọn đường (router) hoặc đơn giản là một bộ phân kênh (Hub). Có nhiều cổng ra và mỗi cổng nối với một máy. Theo chuẩn IEEE 802.3 mô hình dạng Star thường dùng:

 - 10BASE-T: dùng cáp UTP, tốc độ 10 Mb/s, khoảng cách từ thiết bị trung tâm tới trạm tối đa là 100m. 

 - 100BASE-T tương tự như 10BASE-T nhưng tốc độ cao hơn 100 Mb/s

### 2. mô hình OSI. <a name="2"></a>

#### 2.1 hoàn cảnh ra đời <a name="2.1"></a>

- với mô hình kiểu cũ , các thiết bị đến từ các nhà sản xuất khác nhau không thể truyền thông được cho nhaumà chỉ có thể truyền thông được cho các thiết bị cùng nhà sản xuất ~ví dụ~ 1 máy tính của IBM chỉ có thể giao tiếp được với 1 máy của IBM mà không thể trao đồi với 1 máy của HP. 

 - bên cạnh đó với mô hình kiểu cũ, một host chỉ có thể sử dụng các giao thức hay các ứng dụng do chính hãng sản xuất ra, không thể sử dụng được giao thức của các hãng khác 

 - từ đó có thể thấy mô hình kiểu cũ này không có tính mở rộng và không có tính tương thích giữa các dòng sản phẩm khác nhau của các hãng khác nhau. mô hình kiểu cũ này củng thiếu tính chuẩn hóa . 

 - để khắc phục nhược điểm đó ngày nay các host truyền dữ liệu theo các mô hình có tính chuẩn hóa cao. các kỹ thuật truyền số liệu , các ứng dụng , các giao diện đều được chuẩn hóa để các nhà sản xuất tuân theo . từ đó các thiết bị của các hãng khác nhau có thể truyền thông cho nhau. 

 - bên cạnh việc chuẩn hóa các choạt động truyền dữ liệu củng được chia thành các tầng cụ thể chính điều đó đã thúc đẩy sự ra đời của 2 mô hình tiêu chuẩn là mô hình OSI và mô hình TCP/IP.

 - Mô hình OSI (Open Systems Interconnection Reference Model, viết ngắn là OSI Model hoặc OSI Reference Model) - tạm dịch là Mô hình tham chiếu kết nối các hệ thống mở - là một thiết kế dựa vào nguyên lý tầng cấp, lý giải một cách trừu tượng kỹ thuật kết nối truyền thông giữa các máy vi tính và thiết kế giao thức mạng giữa chúng. Mô hình này được phát triển thành một phần trong kế hoạch Kết nối các hệ thống mở (Open Systems Interconnection) do ISO và IUT-T khởi xướng. Nó còn được gọi là Mô hình bảy tầng của OSI.

 - Mô hình OSI phân chia chức năng của một giao thức ra thành một chuỗi các tầng cấp. Mỗi một tầng cấp có một đặc tính là nó chỉ sử dụng chức năng của tầng dưới nó, đồng thời chỉ cho phép tầng trên sử dụng các chức năng của mình. Một hệ thống cài đặt các giao thức bao gồm một chuỗi các tầng nói trên được gọi là "chồng giao thức" (protocol stack). Chồng giao thức có thể được cài đặt trên phần cứng, hoặc phần mềm, hoặc là tổ hợp của cả hai. Thông thường thì chỉ có những tầng thấp hơn là được cài đặt trong phần cứng, còn những tầng khác được cài đặt trong phần mềm.

 - Mô hình OSI này chỉ được ngành công nghiệp mạng và công nghệ thông tin tôn trọng một cách tương đối. Tính năng chính của nó là quy định về giao diện giữa các tầng cấp, tức quy định đặc tả về phương pháp các tầng liên lạc với nhau. Điều này có nghĩa là cho dù các tầng cấp được soạn thảo và thiết kế bởi các nhà sản xuất, hoặc công ty, khác nhau nhưng khi được lắp ráp lại, chúng sẽ làm việc một cách dung hòa (với giả thiết là các đặc tả được thấu đáo một cách đúng đắn). Trong cộng đồng TCP/IP, các đặc tả này thường được biết đến với cái tên RFC (Requests for Comments, dịch sát là "Đề nghị duyệt thảo và bình luận"). Trong cộng đồng OSI, chúng là các tiêu chuẩn ISO (ISO standards).

 - Thường thì những phần thực thi của giao thức sẽ được sắp xếp theo tầng cấp, tương tự như đặc tả của giao thức đề ra, song bên cạnh đó, có những trường hợp ngoại lệ, còn được gọi là "đường cắt ngắn" (fast path). Trong kiến tạo "đường cắt ngắn", các giao dịch thông dụng nhất, mà hệ thống cho phép, được cài đặt như một thành phần đơn, trong đó tính năng của nhiều tầng được gộp lại làm một.

 - Việc phân chia hợp lý các chức năng của giao thức khiến việc suy xét về chức năng và hoạt động của các chồng giao thức dễ dàng hơn, từ đó tạo điều kiện cho việc thiết kế các chồng giao thức tỉ mỉ, chi tiết, song có độ tin cậy cao. Mỗi tầng cấp thi hành và cung cấp các dịch vụ cho tầng ngay trên nó, đồng thời đòi hỏi dịch vụ của tầng ngay dưới nó. Như đã nói ở trên, một thực thi bao gồm nhiều tầng cấp trong mô hình OSI, thường được gọi là một "chồng giao thức" (ví dụ như chồng giao thức TCP/IP).

 - Mô hình tham chiếu OSI là một cấu trúc phả hệ có 7 tầng, nó xác định các yêu cầu cho sự giao tiếp giữa hai máy tính. Mô hình này đã được định nghĩa bởi Tổ chức tiêu chuẩn hoá quốc tế (International Organization for Standardization) trong tiêu chuẩn số 7498-1 (ISO standard 7498-1). Mục đích của mô hình là cho phép sự tương giao (interoperability) giữa các hệ máy (platform) đa dạng được cung cấp bởi các nhà sản xuất khác nhau. Mô hình cho phép tất cả các thành phần của mạng hoạt động hòa đồng, bất kể thành phần ấy do ai tạo dựng. Vào những năm cuối thập niên 1980, ISO đã tiến cử việc thực thi mô hình OSI như một tiêu chuẩn mạng.

 - Tại thời điểm đó, TCP/IP đã được sử dụng phổ biến trong nhiều năm. TCP/IP là nền tảng của ARPANET, và các mạng khác - là những cái được tiến hóa và trở thành Internet. (Xin xem thêm RFC 871 để biết được sự khác biệt chủ yếu giữa TCP/IP và ARPANET.)

 - Hiện nay chỉ có một phần của mô hình OSI được sử dụng. Nhiều người tin rằng đại bộ phận các đặc tả của OSI quá phức tạp và việc cài đặt đầy đủ các chức năng của nó sẽ đòi hỏi một lượng thời gian quá dài, cho dù có nhiều người nhiệt tình ủng hộ mô hình OSI đi chăng nữa.

 - Mặt khác, có nhiều người lại cho rằng, ưu điểm đáng kể nhất trong toàn bộ cố gắng của công trình mạng truyền thông của OSI là nó đã thất bại trước khi gây ra quá nhiều tổn thất.

#### 2.2  các lớp của mô hình và chức năng của từng lớp?<a name="2.2"></a>

mô hình OSI có dạng :
![](https://i.imgur.com/VbfsF73.png)

 - Tầng 1: Tầng vật lý (Physical Layer)
Tầng vật lý định nghĩa tất cả các đặc tả về điện và vật lý cho các thiết bị. Trong đó bao gồm bố trí của các chân cắm (pin), các hiệu điện thế, và các đặc tả về cáp nối (cable). Các thiết bị tầng vật lý bao gồm Hub, bộ lặp (repeater),thiết bị chuyển đổi tín hiệu(Converter), thiết bị tiếp hợp mạng (network adapter) và thiết bị tiếp hợp kênh máy chủ (Host Bus Adapter)- (HBA dùng trong mạng lưu trữ (Storage Area Network)). Chức năng và dịch vụ căn bản được thực hiện bởi tầng vật lý bao gồm:

Thiết lập hoặc ngắt mạch kết nối điện (electrical connection) với một môi trường truyền dẫn phương tiện truyền thông (transmission medium).
Tham gia vào quy trình mà trong đó các tài nguyên truyền thông được chia sẻ hiệu quả giữa nhiều người dùng. Chẳng hạn giải quyết tranh chấp tài nguyên (contention) và điều khiển lưu lượng.
Điều chế (modulation), hoặc biến đổi giữa biểu diễn dữ liệu số (digital data) của các thiết bị người dùng và các tín hiệu tương ứng được truyền qua kênh truyền thông (communication channel).
Cáp (bus) SCSI song song hoạt động ở tầng cấp này. Nhiều tiêu chuẩn khác nhau của Ethernet dành cho tầng vật lý cũng nằm trong tầng này; Ethernet nhập tầng vật lý với tầng liên kết dữ liệu vào làm một. Điều tương tự cũng xảy ra đối với các mạng cục bộ như Token ring, FDDI và IEEE 802.11.]]

Tầng 2: Tầng liên kết dữ liệu (Data-Link Layer)
Tầng liên kết dữ liệu cung cấp các phương tiện có tính chức năng và quy trình để truyền dữ liệu giữa các thực thể mạng (truy cập đường truyền, đưa dữ liệu vào mạng), phát hiện và có thể sửa chữa các lỗi trong tầng vật lý nếu có. Cách đánh địa chỉ mang tính vật lý, nghĩa là địa chỉ (địa chỉ MAC) được mã hóa cứng vào trong các thẻ mạng (network card) khi chúng được sản xuất. Hệ thống xác định địa chỉ này không có đẳng cấp (flat scheme). Chú ý: Ví dụ điển hình nhất là Ethernet. Những ví dụ khác về các giao thức liên kết dữ liệu (data link protocol) là các giao thức HDLC; ADCCP dành cho các mạng điểm-tới-điểm hoặc mạng chuyển mạch gói (packet-switched networks) và giao thức Aloha cho các mạng cục bộ. Trong các mạng cục bộ theo tiêu chuẩn IEEE 802, và một số mạng theo tiêu chuẩn khác, chẳng hạn FDDI, tầng liên kết dữ liệu có thể được chia ra thành 2 tầng con: tầng MAC (Media Access Control - Điều khiển Truy nhập Đường truyền) và tầng LLC (Logical Link Control - Điều khiển Liên kết Lôgic) theo tiêu chuẩn IEEE 802.2.

Tầng liên kết dữ liệu chính là nơi các thiết bị chuyển mạch (switches) hoạt động. Kết nối chỉ được cung cấp giữa các nút mạng được nối với nhau trong nội bộ mạng.

Tầng 3: Tầng mạng (Network Layer)
Tầng mạng cung cấp các chức năng và quy trình cho việc truyền các chuỗi dữ liệu có độ dài đa dạng, từ một nguồn tới một đích, thông qua một hoặc nhiều mạng, trong khi vẫn duy trì chất lượng dịch vụ (quality of service) mà tầng giao vận yêu cầu. Tầng mạng thực hiện chức năng định tuyến,.Các thiết bị định tuyến (router) hoạt động tại tầng này — gửi dữ liệu ra khắp mạng mở rộng, làm cho liên mạng trở nên khả thi (còn có thiết bị chuyển mạch (switch) tầng 3, còn gọi là chuyển mạch IP). Đây là một hệ thống định vị địa chỉ lôgic (logical addressing scheme) – các giá trị được chọn bởi kỹ sư mạng. Hệ thống này có cấu trúc phả hệ. Ví dụ điển hình của giao thức tầng 3 là giao thức IP.

Tầng 4: Tầng giao vận (Transport Layer)
Tầng giao vận cung cấp dịch vụ chuyên dụng chuyển dữ liệu giữa các người dùng tại đầu cuối, nhờ đó các tầng trên không phải quan tâm đến việc cung cấp dịch vụ truyền dữ liệu đáng tin cậy và hiệu quả. Tầng giao vận kiểm soát độ tin cậy của một kết nối được cho trước. Một số giao thức có định hướng trạng thái và kết nối (state and connection orientated). Có nghĩa là tầng giao vận có thể theo dõi các gói tin và truyền lại các gói bị thất bại. Một ví dụ điển hình của giao thức tầng 4 là TCP. Tầng này là nơi các thông điệp được chuyển sang thành các gói tin TCP hoặc UDP. Ở tầng 4 địa chỉ được đánh là address ports, thông qua address ports để phân biệt được ứng dụng trao đổi.

Tầng 5: Tầng phiên (Session layer)
Tầng phiên kiểm soát các (phiên) hội thoại giữa các máy tính. Tầng này thiết lập, quản lý và kết thúc các kết nối giữa trình ứng dụng địa phương và trình ứng dụng ở xa. Tầng này còn hỗ trợ hoạt động song công (duplex) hoặc bán song công (half-duplex) hoặc đơn công (Single) và thiết lập các quy trình đánh dấu điểm hoàn thành (checkpointing) - giúp việc phục hồi truyền thông nhanh hơn khi có lỗi xảy ra, vì điểm đã hoàn thành đã được đánh dấu - trì hoãn (adjournment), kết thúc (termination) và khởi động lại (restart). Mô hình OSI uỷ nhiệm cho tầng này trách nhiệm "ngắt mạch nhẹ nhàng" (graceful close) các phiên giao dịch (một tính chất của giao thức kiểm soát giao vận TCP) và trách nhiệm kiểm tra và phục hồi phiên, đây là phần thường không được dùng đến trong bộ giao thức TCP/IP.

Tầng 6: Tầng trình diễn (Presentation layer)
Lớp trình diễn hoạt động như tầng dữ liệu trên mạng. lớp này trên máy tính truyền dữ liệu làm nhiệm vụ dịch dữ liệu được gửi từ tầng Application sang dạng Fomat chung. Và tại máy tính nhận, lớp này lại chuyển từ Fomat chung sang định dạng của tầng Application. Lớp thể hiện thực hiện các chức năng sau: - Dịch các mã ký tự từ ASCII sang EBCDIC. - Chuyển đổi dữ liệu, ví dụ từ số interger sang số dấu phảy động. - Nén dữ liệu để giảm lượng dữ liệu truyền trên mạng. - Mã hoá và giải mã dữ liệu để đảm bảo sự bảo mật trên mạng.

Tầng 7: Tầng ứng dụng (Application layer)
Tầng ứng dụng là tầng gần với người sử dụng nhất. Nó cung cấp phương tiện cho người dùng truy nhập các thông tin và dữ liệu trên mạng thông qua chương trình ứng dụng. Tầng này là giao diện chính để người dùng tương tác với chương trình ứng dụng, và qua đó với mạng. Một số ví dụ về các ứng dụng trong tầng này bao gồm Telnet, Giao thức truyền tập tin FTP và Giao thức truyền thư điện tử SMTP, HTTP, X.400 Mail remote

### 3.  Mô hình TCP/IP: Các lớp? So sánh với mô hình OSI.<a name=3></a>

 - TCP/IP là bộ giao thức cho phép kết nối các hệ thống mạng không đồng nhất với nhau. Ngày nay TCP/IP được sử dụng rộng rãi trong mạng cục bộ cũng như mạng toàn cầu.

 ![](https://i.imgur.com/btok2ip.png)

- TCP/IP được xem như giản lược của mô hình tham chiếu OSI với 4 tầng như sau:

  o Tầng Liên Kết (Datalink Layer)

  o Tầng Mạng (Internet Layer)

  o Tầng Giao Vận (Transport Layer)

  o Tầng Ứng Dụng (Application Layer)

 - Tầng liên kết: Tầng liên kết (còn được gọi là tầng liên kết dữ liệu hay tầng giao tiếp mạng) là tầng thấp nhất trong mô hình TCP/IP, bao gồm các thiết bị giao tiếp mạng và các chương trình cung cấp các thông tin cần thiết để có thể hoạt động, truy nhập đường truyền vật lý qua các thiết bị giao tiếp mạng đó.

 - Tầng Internet: Tầng Internet ( hay còn gọi là tầng Mạng) xử lý quá trình truyền gói tin trên mạng, các giao thức của tầng này bao gồm : IP ( Internet Protocol) , ICMP ( Internet Control Message Protocol) , IGMP ( Internet Group Message Protocol )

 - Tầng giao vận: Tầng giao vận phụ trách luồng dữ liệu giữa 2 trạm thực hiện các ứng dụng của tầng trên, tầng này có 2 giao thức chính là TCP ( Transmisson Control Protocol) và UDP ( User Datagram Protocol )

 – TCP cung cấp luồng dữ liệu tin cậy giữa 2 trạm, nó sử dụng các cơ chế như chia nhỏ các gói tin ở tầng trên thành các gói tin có kích thước thích hợp cho tầng mạng bên dưới, báo nhận gói tin, đặt hạn chế thời gian timeout để đảm bảo bên nhân biết được các gói tin đã gửi đi. Do tầng này đảm bảo tính tin cậy nên tầng trên sẽ không cần quan tâm đến nữa

 – UDP cung cấp một dịch vụ rất đơn giản hơn cho tầng ứng dụng . Nó chỉ gửi dữ liệu từ trạm này tới trạm kia mà không đảm bảo các gói tin đến được tới đích. Các cơ chế đảm bảo độ tin cậy được thực hiện bởi tầng trên
Tầng ứng dụng

 - Tầng ứng dụng là tầng trên của mô hình TCP/IP bao gồm các tiến trình và các ứng dụng cung cấp cho người sử dụng để truy cập mạng. Có rất nhiều ứng dụng được cung cấp trong tầng này , mà phổ biến là Telnet: sử dụng trong việc truy cập mạng từ xa, FTP ( File Transport Protocol ) dịch vụ truyền tệp tin., EMAIL : dịch vụ truyền thư tín điện tử. WWW ( Word Wide Web )

##### . So sánh TCP/IP với OSI

 - Mỗi tầng trong TCP/IP có thể là một hay nhiều tầng của OSI . Bảng sau chỉ rõ mối tương quan giữa các tầng trong mô hình TCP/IP với OSI

 ![](http://www.vnpro.vn/wp-content/uploads/2015/11/sp-sanh.jpg)

 - Sự khác nhau giữa TCP/IP với OSI:

 o Tầng ứng dụng trong mô hình TCP/IP bao gồm luôn cả 3 tầng trên của mô hình OSI

 o Tầng giao vận trong mô hình TCP/IP không phải luôn đảm bảo độ tin cậy của việc truyền tin như ở trong tầng giao vận của OSI mà cho phép thêm một lựa chọn khác là UDP


##### các ứng dụng ở tầng applycation 

 - các ứng dụng truyền file 
 <ul>
 <li>FTP</li>
 <li>TFTP</li>
 <li>Network File System</li>
 <li>E-mail</li>
 </ul>
 – Simple Mail Transfer Protocol
 
 - Remote login

 –Telnet

 – rlogin
 
 - Network management
 
 – Simple Network Management Protocol
 
 - Name management
 
 – Domain Name System
