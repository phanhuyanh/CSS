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
   
4. **align-content**
   * thuộc tính CSS ```align-content``` thiết lập phân bố giữa không gian và xung quanh nội dung phần tử dọc theo trục chéo ```flex-box``` hoặc trục khối của ```grid``` 
  
      | Property | Explain|
      |----------|--------|
      |```start``` | các phần từ được gói gọn lên đầu cạnh của khối container |
      |```end``` | các phần tử được gói gọi xuống cuối cạnh của khối container |
      |```flex-start``` |  thuộc tính chỉ áp dụng cho ```flex``` layout và các phần tử được gói gọn lên đầu của khối container theo trục chéo mà container quy định(ví dụ: ```flex-direction: row```) |
      |```flex-end``` | thuộc tính chỉ áp dụng cho ```flex``` layout và các phần tử được gói gọn xuống cuối của khối container theo trục chéo mà container quy định(ví dụ: ```flex-direction: row or column```) |
      |```center``` | các phần tử được gói gọn nằm chính giữa của khối container theo trục chéo |
      |```normal``` | các phần tử được đặt vị trí mặc định giống như thuộc tính ```align-content``` chưa được thiết lập |
      |```baseline``` | các phần tử được căn chỉnh có text ngang hàng nhau |
      |```space-between``` |  các phần tử được phân bố đều trong căn chỉnh container theo trục chéo.Khoảng không gian giữa các phần tử liền kề là bằng nhau.Phần tử đầu tiên sẽ nằm vị trí ```start``` và phần tử cuối cùng nằm vị trí ```end``` |
      |```space-around``` | các phần tử được phân bố đều trong căn chỉnh container theo trục chéo. Khoảng không gian giữa các phần tử liền kề là bằng nhau. Khoảng không gian bắt đầu cạnh container vs phần tử đầu tiên và khoảng không gian giữa phần tử cuối cùng với vị trí ```end``` của container là bằng nhau và bằng 1/2 khoảng các giữa các phần tử liền kề. |
      |```space-evenly```| các phần tử được phân bố đều trong căn chỉnh container theo trục chéo. Khoảng không gian giữa các phần tử liền kề là bằng nhau va bằng vị trí ```start``` của container đến phần tử đầu tiên và phần tử cuối cùng đến vị trí ```end``` của container |
      |```stretch``` | nếu kết hợp kích thước của các phần tử dọc theo trục chéo nhỏ hơn kích thước căn chỉnh của khối container, thì các phần tử tự động tăng kích thước như nhau, sao cho lấp đầy chính xác kích thước dọc theo trục chéo. |
   * [Explain detail](https://developer.mozilla.org/en-US/docs/Web/CSS/align-content)
  
5. **align-items**
   * Thuộc tính CSS ```align-items``` thiết lập giá trị ```align-self``` cho tất cả các thẻ con trực tiếp thành 1 nhóm.Trong FlexBox nó điều khiển căn chỉnh các phần tử trong trục chéo.(trục chéo là trục vuông góc với trục ```flex-direction```). Trong GridLayout nó điều khiển căn chỉnh các phần tử của trục khối.
   * Property
     1. ```normal```: Tùy theo kiểu bố trí mà có hiệu lực khác nhau
        * Với layout có vị trí cố định, nó sẽ cư xử các items tuyệt đối(absolute) như ```start``` và các tất cả các items cố định khác là ```stretch```
        * Với vị trí tĩnh(static) của layout tuyệt đối(absolute), nó sẽ cư xử như ```stretch```
        * Với Flex-items, nó sẽ cư xử như ```stretch```
        * Với Grid items, nó có hành vi tương tự như ```stretch```, ngoại trừ các items có tỷ lệ khung nhìn hoặc có kích thước bên trong thì sẽ cư xử như ```start```
        * Thuộc tính không ứng dụng với table cells và block-level box
      2. ```flex-start```: các phần tử(item) sẽ được căn chỉnh lên đầu cạnh của khối container
      3. ```flex-end```: các phần tử(item) sẽ được căn chỉnh xuống cuối cạnh của khối container
      4. ```center```: các phần tử(item) sẽ được chỉnh ra giữa cách đề đầu cạnh và cuối cạnh của khối container
      5. ```baseline```: dựa vào item có height lớn nhất và các item còn lại căn chỉnh sao cho thẳng hàng với nhau
      6. ```stretch```: các phần tử sẽ được tự động tùy chỉnh ```height``` sao cho lấp đầy khoảng không gian của khối container
   
6. **-webkit-box-reflect**
   * Tạo một thẻ div ảo phản chiếu với thẻ đó
   * Style: ```-webkit-box-reflect: below 1px linear-gradient(transparent, transparent, #0004)```
 
