# CSS Property

1. **-webkit-line-clamp**
   * Cho phép hạn chế nội dung của 1 block(khối) bằng số dòng được chỉ định
   * Nó chỉ hoạt động khi kết hợp thuộc tính ```display``` thiết lập là ```-webkit-box``` or ```-webkit-inline-box``` và thuộc tính ```-webkit-box-orient``` thiết lập là ```vertical```
   * Trong hầu hết các trường hợp bạn sẽ muốn thiết lập ```overflow``` là ```hidden```, ngược lại nội dung sẽ không bị cắt xén nhưng dấu ba chấm vẫn sẽ hiển thị sau khi số dòng được chỉ định
   * *Áp dụng khi muốn cho đoạn text hiển thị tối đa số dòng được chỉ định, còn lại dùng dấu ba chấm*
   * [DEMO](https://jsfiddle.net/HuyAnh_123doc_IT/d9xg2v4j/1/)

2. **:active**
   * ```:active``` là class giả đại diện cho phần tử đang được kích hoạt bởi người dùng.Khi sử dụng chuột, ki*kích hoạt* điển hình khi người dùng nhấn chuột trái xuống
   * class giả ```:active``` thường được dùng cho thẻ ```a``` và ```button```
   * Thứ tự của class giả là ```:link```--```:visited```--```:hover```--```:active```
   * [DEMO](https://jsfiddle.net/HuyAnh_123doc_IT/1rmuq0c4/2/)

3. **::after**
   * tạo phần tử giả ```::after``` sẽ là phần tử con cuối cùng của phần tử được chọn.Nó thường được dùng để thêm một nội dung tô điểm phần tử đó với thuộc tính ```content```.Nó mặc định là ```display: inline```.
   * Syntax CSS3 ```::after```
   * Syntax CSS2 ```:after```
   * [DEMO](https://developer.mozilla.org/en-US/docs/Web/CSS/::after)
