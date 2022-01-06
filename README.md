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
-Từ đó nhận ra rằng ,việc thằng Serilizable tức là nó sẽ tuần tự hóa đối tượng object đó .với lại dù đang ở nền tảng nào thì việc truy cập vào cái luồng byte đó vẫn oke.Trên mạng object bắn tới là nền tảng khác .trên android là nền tảng khác .Nên em nghĩ cứ qua mạng là chơi ngay thằng serrilizable.
## Serilzable vs Paracelable:
-Serilizable là thằng interface được các đối tượng object để tuần tự hóa hóa nó
-Trong khi đó Paracelable:
