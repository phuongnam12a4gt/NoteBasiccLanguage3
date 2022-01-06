# NoteBasiccLanguage3
## Serilization vs Deserilization:
### Serilization:
#### Java:
-Đây chính là quá trình chuyển đổi 1 đối tượng java object thành các qua các byte stream.Và các cái đó sẽ được lưu trử trong ổ đĩa .bộ nhớ .sau đó các luồng khác củng có thể truy cập nó từ 1 luồn khác,củng có thể lấy được thông tin của nó.
-Nó được sử dụng chủ yếu truyền qua mạng.Để triển khai đó thì đối tượng đó phải cài đặt interface serrilizable.Còn về phần ngôn ngữ kotlin hiện tại thì củng triển khai thằng serrilizable của thằng java.
### Deserilization:
Đây củng chính là quá trình chuyển ngược từ thằng byte stream thành các đối tượng object.
## Vậy lợi ích của việc này là gì ?
-Theo em hiểu việc chuyển tiếp theo dạng này chắc chắn sẽ giảm thời gian hơn.
- Nếu mà nó ghi theo cơ chế từ trên mạng bắn về thì có thể là output stream ,dữ liệu sẽ bắn ngược vào file tệp.Còn nếu sử dụng luồng ByteArrayObjectOutPut thì bắn vô mảng bộ nhớ.
thực hiện theo cơ chế socket tới socket nhận thì sau đó sẽ được giải mã.
-Từ đó nhận ra rằng ,việc thằngSerilizable tức là nó sẽ tuần tự hóa đối tượng object đó .với lại dù đang ở nền tảng nào thì việc truy cập vào cái luồng byte đó vẫn oke.Trên mạng object bắn tới là nền tảng khác .trên android là nền tảng khác .Nên em nghĩ cứ qua mạng là chơi ngay thằng serrilizable.
## Serilzable vs Paracelable:
-Serilizable là thằng interface được các đối tượng object để tuần tự hóa hóa nó
###Paracelable:
Theo như em hiểu thằng này vì sao khi ta truyền giữa 2 activity nhanh hơn thằng serrilizable là vì thằng này nó thực hiện theo cơ chế tuàn tự hóa ,có nghĩa là lúc đầu có đối tượng nó sẽ thực hiện ghi vào trong 1 parcel nhưng nó để thông qua thằng  Creator thằng và thằng này có nhiệm vụ tạo ra đối tượng tĩnh ,để tạo ra 1 đối tượng mới kiêu dữ liệu đối tượng.Trong khi nếu ở activity khác thì thằng này củng có cái để lấy ra đối tượng đó thông qua thằng static của nó.Vậy nó chỉ đưa vô rồi ,rồi lấy ra .Nhưng 2 thứ này phải củng nền tảng mới lấy được.Còn thằng Serrilizable nó sẽ thực hiện việc ánh xa qua byte rồi ánh xạ ngược lại ,đồng thời tạo ra mấy đối tượng rác ,thì nó ko tốt bằng parcelable.Còn việc truyền dữ liệu mạng  dùng thăng Paracelable đi thì em nghĩ nó khác nền tảng rồi nên ko dùng.
