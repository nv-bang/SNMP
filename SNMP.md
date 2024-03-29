## Simple Network Management Protocol|(SNMP)

I. **SNMP là gì?**

  - SNMP là một giao thức tầng ứng dụng quy định bởi IAB trong RFC1157 để trao đổi thông tin quản lý giữa các thiết bị mạng.
  - SNMP là một giao thức tiêu chuẩn được sử dụng rộng rãi để quản lý và giám sát các thiết bị mạng

  - SNMP là một tập hợp các giao thức không chỉ cho phép kiểm tra tài nguyên và giám sát lưu lượng các thiết bị mạng như router,switch hay server đang vận hành mà còn hỗ trợ vận hành các thiết bị này một cách tối ưu. Ngoài ra SNMP còn cho phép quản lý các thiết bị mạng từ xa/

  - Giao thức SNMP được thiết kế để cung cấp một phương thức đơn giản để quản lý tập trung mạng TCP/IP. Nếu bạn muốn quản lý các thiết bị từ 1 vị trí tập trung, giao thức SNMP sẽ vận chuyển dữ liệu từ client (thiết bị mà bạn đang giám sát) đến server nơi mà dữ liệu được lưu trong log file nhằm phân tích dễ dàng hơn

  - SNMP dùng để quản lý tức là có thể theo dõi, có thể lấy thông tin, có thể được thông báo, và có thể tác động để hệ thống hoạt động như ý muốn.

  - Ví dụ một số khả năng của SNMP:

    - Theo dõi tốc độ đường truyền của một router/máy chủ, biết được tổng số byte đã truyền/nhận.

    - Lấy thông tin máy chủ đang có bao nhiêu ổ cứng, mỗi ổ cứng còn trống bao nhiêu

    - Tự động nhận cảnh báo khi switch có 1 port bị down

    - Điều khiển shutdown các port trên switch.

  - Có 2 nhân tố chính trong SNMP:  manager và agent. Các SNMP agent sẽ giữ một sơ sở dữ liệu, được gọi là Management Information Base (MIB), trong đó chứa các thông tin khác nhau về hoạt động của thiết bị mà agent đang giám sát. Phần mềm quản trị SNMP Manager sẽ thu thập thông tin này qua giao thức SNMP.

  <img src=https://i.imgur.com/GDrwXY8.jpg>

  - Ưu điểm khi thiết kế hệ thống quản trị với SNMP sẽ giúp đơn giản hóa các quá trình quản lý các thành phần trong mạng, giảm chi phí triển khai. SNMP được thiết kế có thể hoạt động độc lập với các kiến trúc và cơ chế của các thiết bị hỗ trợ SNMP. Các thiết bị khác nhau có hoạt động khác nhau nhưng đáp ứng SNMP là giống nhau.

  - SNMP bao gồm một bộ các tiêu chuẩn để quản lý mạng, bao gồm một giao thức lớp ứng dụng, một giản đồ cơ sở dữ liệu, và một tập các data objects

| Ứng dụng                             | Mô tả                                                         |
|-------------------------------------|----------------------------------------------------------------|
| Cisco Prime Infrastructure           | Hệ thống quản lý mạng toàn diện của Cisco                       |
| SolarWinds Network Performance Monitor | Giám sát và quản lý hiệu suất mạng                            |
| PRTG Network Monitor                 | Giám sát mạng và hệ thống tương thích với SNMP                   |
| Zabbix                              | Giám sát và quản lý mạng và hệ thống tương thích với SNMP       |
| Nagios                              | Giám sát hệ thống và mạng tương thích với SNMP                   |
| ManageEngine OpManager               | Phần mềm quản lý mạng và giám sát                                 |
| Paessler Router Traffic Grapher      | Giám sát lưu lượng mạng và thiết bị tương thích với SNMP          |
| IBM Tivoli Network Manager           | Hệ thống quản lý mạng của IBM                                    |
| HP OpenView Network Node Manager     | Hệ thống quản lý và giám sát mạng của HP                          |
| Juniper Networks Network Director    | Hệ thống quản lý mạng của Juniper Networks                        |


| Phiên bản | Ưu điểm                                                                           | Nhược điểm                                                                                      |
|-----------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| SNMPv1    | - Đơn giản và dễ triển khai | - Xác thực yếu (community string) |
|           | - Tiêu chuẩn hóa và tương thích rộng rãi                                           | - Không cung cấp tính năng mã hóa dữ liệu                                                       |
|           | - Quản lý và điều khiển thiết bị hạn chế                                                                            
| SNMPv2c   | - Cải tiến so với SNMPv1, bổ sung mô hình quản lý và phương thức mới                | - Xác thực yếu                                                                       |
|           | - Tiêu chuẩn hóa và tương thích rộng rãi                                           | - Không cung cấp tính năng mã hóa dữ liệu                                                       |
|           | - Quản lý và điều khiển thiết bị hạn chế                                            |
| SNMPv2u   | - Cải tiến liên quan đến quản lý nhóm và đối tượng                                | - Xác thực yếu                                                                       |
|           | - Quản lý và điều khiển thiết bị hạn chế                                            | - Không cung cấp tính năng mã hóa dữ liệu                                                       |
| SNMPv3    | - Cung cấp cải tiến đáng kể về bảo mật, hỗ trợ xác thực và mã hóa dữ liệu           | - Định dạng thông điệp phức tạp hơn                                                             |
|           | - Hỗ trợ xác thực mạnh hơn như HMAC và mã hóa dữ liệu bằng DES, AES                  | - Yêu cầu cấu hình và triển khai phức tạp hơn                                                    |
|           | - Quyền kiểm soát truy cập chi tiết và quản lý người dùng                           | - Yêu cầu hỗ trợ từ các thiết bị và ứng dụng SNMP                                                 |
|           |                                                                                   | - Cần có kiến thức về bảo mật để triển khai và quản lý SNMPv3                                      |

II. **SNMP hoạt động như thế nào**:

  - Có 2 phương pháp giám sát là poll và alert

    - Poll: Manager sẽ thường xuyên hỏi thông tin của agent. Nếu manager không hỏi thì agent không trả lời

    - Alert: Mỗi khi agent xảy ra event nào đó thì nó sẽ tự động gửi thông báo cho manager

  - SNMP sử dụng UDP (User Datagram Protocol) làm giao thức truyền tải thông tin giữa manager và các agent. Việc sử dụng UDP, thay vì TCP, bởi vì UDP là phương thức truyền mà trong đó hai đầu thông tin không cần thiết lập kết nối trứơc khi dữ liệu được trao đổi (connectionless), thuộc tính này phù hợp trong điều kiện mạng gặp trục trặc, hư hỏng... cần ưu tiên về mặt tốc độ.

  - Trong các ứng dụng của SNMP, một hoặc nhiều máy tính quản trị được gọi là các máy managers có nhiệm vụ giám sát hoặc quản lý một nhóm máy chủ hoặc thiết bị trên mạng máy tính. Mỗi hệ thống được quản lý được gọi là một agent báo cáo thông tin thông qua SNMP cho máy manager.

&ensp;&ensp;&ensp;&ensp;  <img src= https://i.imgur.com/IVTEvyT.png >

  - Hệ thống SNMP bao gồm 2 thành phần chính:

    - Manager

    - Agent

  - SMP Manager là máy được config để nhận và xử lý thông tin từ Agent gửi tới. Manager có thể  yêu cầu truy vấn đến các Agents với các thông tin chính xác.

  - Agent thu thập thông tin của client và lưu trữ chúng ở định dạng có thể query được

  - MIB (Management Information base) là một cấu trúc được định nghĩa theo thứ bậc, lưu trữ thông tin có thể được truy vấn hay thiết lập. Cấu trúc MIB được hiểu là cây phân cấp từ trên xuống dưới. Mỗi nhánh được fork ra được dán nhãn với cả 1 số nhận dạng(bắt đầu bằng 1) và 1 chuỗi xác định.

  <img src=https://i.imgur.com/AXhVG5I.png>

  - Các node có 1 Object ID duy nhất. ví dụ sysUPtime có OID là 1.3.6.1.2.1.1.3.0

- SNMP protocol Command

  - SNMP có các phương thức quản lý nhất định và các phương thức này được định dạng bởi các gói tin PDU (Protocol Data Unit). Các manager và agent sử dụng PDU để trao đổi với nhau.

  - Get : Get message gửi bởi manager tới agent để yêu cầu giá trị của 1 OID cụ thể. được trả lời với gói Response

  - GetNext: Manager yêu cầu object tiếp theo trong MIB.

  - Set: Manager gửi đến 1 agent để thay đổi giá trị được gửi bởi 1 biến trên agent.Điều này có thể sử dụng để kiểm soát thông tin cấu hình hoặc thay đổi trạng thái máy chủ từ xa.

  - Response: gửi bởi agent, dùng để gửi bất kỳ thông tin nào mà manager yêu cầu

  - Trap: Được gửi từ agent đến manager. Là các thông báo không đồng bộ ở chỗ chúng không được yêu cầu bởi manager. Chủ yếu sử dụng để truyền thông tin cần mornitor. Có 2 loại trap là generic trap và specific trap:

    - generic trap: được quy định trong các chuẩn SNMP

    - specific trap : được người dùng định nghĩa

  - SNMP chạy trên UDP. cấu trúc 1 bản tin SNMP bao gồm version,community và data(PDU).

  <img src=https://i.imgur.com/Kh6J4FN.jpg>


  III. **Cấu hình và cài đặt SNMP**

  - Môi trường cài đặt : VMware

  - Mô hình:

  <img src=https://i.imgur.com/839fvj5.png>

1. ** Config máy agent**

  - Cài đặt các package:

  ```
  apt-get -y install snmp snmpd snmp-mibs-downloader net-snmp net-snmp-utils
  ```

  - Config file /etc/snmp/snmpd.conf

  ```
  # line 15: comment out
  #agentAddress udp:127.0.0.1:161
  # line 17: uncomment
  agentAddress udp:161,udp6:[::1]:161
  # line 49: uncomment and change to any comunity name you like
  rocommunity public localhost
  # line 51: comment out
  #rocommunity public default -V systemonly
  # line 59: uncomment and change to any comunity name & change access permission
  rocommunity public 10.0.0.0/24

  ```
  - Restart service snmpd

  ```
  systemctl restart snmpd
  ```
2. Cấu hình SNMP cho thiết bị mạng Cisco
- ví dụ cấu hình SNMPv2c cho một thiết bị Cisco
  ```
     snmp-server community <community-string> RO
  ```
- Ví dụ cấu hình SNMP cho một thiết bị Cisco sử dụng giao thức SNMPv3
 ```
     snmp-server group <group-name> v3 priv
     snmp-server user <username> <group-name> v3 auth sha <auth-password> priv aes 128 <encryption-password>
```
 
3. Ví dụ truy vấn snmp đến thiết bị

```
snmpget -v2c -c@snmp 10.1.1.1 SNMPv2-MIB::sysLocation.0
```


- `snmpget`: Là câu lệnh SNMP để lấy giá trị của một biến SNMP từ một thiết bị.
- `-v2c`: Đặc tả phiên bản SNMP sử dụng, trong trường hợp này là SNMPv2c (Community-based SNMPv2).
- `-c@snmp`: Chuỗi xác thực cộng đồng (community string) được sử dụng để xác thực yêu cầu SNMP. Trong ví dụ này, chuỗi xác thực  là "@snmp".
- `10.1.1.1`: Địa chỉ IP của thiết bị mạng mà bạn muốn truy vấn thông tin SNMP.
- `SNMPv2-MIB::sysLocation.0` (1.3.6.1.2.1.1.6): Định danh của biến SNMP mà bạn muốn lấy giá trị. Trong ví dụ này, biến `sysLocation` trong MIB (Management Information Base) `SNMPv2-MIB` với chỉ số 0 (`sysLocation.0`).
