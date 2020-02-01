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
   * Value
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
   * [DEMO](https://jsfiddle.net/HuyAnh_123doc_IT/v3crbosg/3/)

7. **align-self**
   * Thuộc tính CSS ```align-self``` ghi đè giá trị ```align-items``` của ```grid``` or ```flex```. Trong ```grid```, nó căn chỉnh item(phần tử) trong diện tích grid(```grid area```). Trong ```Flexbox```, nó căn chỉnh item(phần tử) trong trục chéo.
   * Value
      1. ```auto```: Tự động tính toán theo giá trị của ```align-items```
      2. ```normal```: Tùy theo kiểu bố trí mà có hiệu lực khác nhau
         * Trong layout vị trí cố định(absolute), nó cư xử như ```start``` với khối cố định, và như ```stretch``` với tất cả các boxes khác
         * Vị trí tĩnh(static position) của layout absolute-position, nó cư xử như ```stretch```
         * Đối với ```flex items```, nó cư xử như ```stretch```
         * Đối với ```grid items```, nó cư xử như ```stretch```, ngoại trừ boxes có tỷ lệ khung hình or có kích thước nội tại thì nó cư xử như ```start```
         * Thuộc tính không áp dụng với ```block-level```boxes, and ```table cells```
      3. ```self-start```: Căn chỉnh items ra đầu cạnh của căn chỉnh container tương ứng với cạnh bắt đầu của trục chéo.
      4. ```self-end```: Căn chỉnh items xuống cuối cạnh của căn chỉnh container
      5. ```flex-start```: dùng cho ```flex``` căn chỉnh phần tử lên đầu cạnh của container
      6. ```center```: căn lề box ra giữa trong trục chéo. Nếu trục chéo của item lớn hơn flex container , nó sẽ tràn đều cả 2 hướng.
      7. ```baseline```: dựa vào items có height lớn nhất mà căn chỉnh sao cho thẳng hàng 
      8. ```stretch```: Nếu kích thước item dọc theo trục chéo nhỏ hơn căn chỉnh container, item sẽ tự động tăng kích thước bằng với căn chỉnh container dọc theo trục chéo, trong khi nó vẫn tôn trọng những hạn chế áp đặt bởi ```max-height/max-width```
         
   * [Explain detail](https://developer.mozilla.org/en-US/docs/Web/CSS/align-self)
 
 8. **animation-fill-mode**
    * Syntax: ```animation-fill-mode: value```
    * Value:
    
      |Value|Explain|
      |-----|-------|
      |none|Animation sẽ không áp dụng bất kỳ style nào lên đối tượng không thực hiện.Phần tử sẽ thay thế hiển thị sử dụng bất kỳ quy tắ CSS áp dụng lên nó. Đây là giá trị mặc định|
      |forwards| Đối tượng sẽ được giữ lại vị trí cuối cùng của ```animation```|
      |backwards| Đối tượng sẽ được quay lại vị trí ban đầu sau khi hết ```animation```|
      |both| Nó sẽ theo quy tắc của ```forwards``` và ```backwards```|
      
9. **animation-iteration-count**
   * Syntax: ```animation-iteration-count: <number> | infinite```
   * Định nghĩa số lần ```animation``` được thực hiện. Nếu giá trị là ```infinite``` thì ```animation``` sẽ thực hiện mãi mãi.
   
10. **animation-name**
    * Thuộc tính thiết lập một hoặc nhiều ```animation``` cung cấp cho ```element```.Mỗi tên là quy tắc ```@keyframes``` thiết lập giá trị thuộc tính cho một chuỗi animation
    * Syntax: ```animation-name: slide``` và ```@keyframes slide {}```
    
11. **animation-play-state**
     * Thuộc tính thiết lập liệu ```animation``` đang chạy hoặc dừng lại
     * Syntax: ```animation-play-state: running | paused```
     
     |Value|Explain|
     |-----|-------|
     |running| ```animation``` đang ở trạng thái ```running```
     |paused| ```animation``` đăng ở trạng thái ```paused```|
    
12. **animation-timing-function**
     * Thuộc tính thiết lập làm thế nào ```animation``` chuyển động trong suốt thời gian của 1 chu kỳ
     * Value
     
     |Value|Explain|
     |-----|-------|
     |ease|Đây là giá trị mặc định. Vận tốc tăng dần đến giữa ```animation``` và giảm dần về cuối|
     |linear| Tại mọi thời điểm của animation đề có vận tốc đều nhau|
     |ease-in|Ban đầu chậm, tăng dần tốc độ cho tới khi kết thúc ```animation```|
     |ease-out| Ban đầu nhanh, giảm dần tốc độ cho tới khi kết thúc ```animation```|
     |ease-in-out| Ban đầu chậm , xong rồi nhanh rồi lại chậm|
     
13. **animation**
    * Syntax: ```animation: animation-name | animation-duration | animation-timming-function | animation-delay | animation-iteration-count | animation-direction | animation-fill-mode | animation-play-state```
    
14. **attr()**
    * function CSS ```attr``` sử dụng để lấy lại giá trị của thuộc tính(attribute) của phần tử được chọn, và sử dụng nó trong stylesheet.Nó cũng có thế sử vói phần tử giả(pseudo-element: after và before), giá trị của thuộc tính trong phần tử giả chính là giá trị của phần tử nguyên gốc.
    * Syntax: ```property: attr(attribute-name)```
    * Example:
      1. HTML: ```<p data-foo="hello">world</p>```
      2. CSS: ```[data-foo]::before {
              content: attr(data-foo) " ";
              }
              ```
15. **background-attachment**
    * Là thuộc tính thiết lập liệu vị trí ảnh nền sẽ ```fixed``` với màn hình ```viewport``` hoặc ```scrolls``` với khối chứa nó.
    * Value
    
    |Value|Explain|
    |-----|-------|
    |fixed|Ảnh nền sẽ được fixed với ```viewport```. Thậm chí nếu phần tử có cơ chế ```scroll```, thì ảnh nền không di chuyển cùng với phần tử. Nó không tương thích với ```background-clip: text```|
    |scroll|Ảnh nền sẽ ```fixed``` với phần tử chính nó và không cuộn với nội dung của nó. Nó chỉ có hiệu lực trói buộc với border element(nghĩa là nếu border của phần tử đó di chuyển thì ảnh nền cũng di chuyển theo).|
    |local|Ảnh nền sẽ ```fixed``` với nội dung của nó(element's contents).Nếu phần tử có cơ chế cuộn(```scroll```) thì ảnh nền sẽ cuộn theo nội dung của phần tử và diện tích ảnh nền và vị trí ảnh nền liên quan với diện tích ```scroll``` thay vì đóng khung chúng|
    
    * [DEMO](https://mdn.github.io/learning-area/css/styling-boxes/backgrounds/background-attachment.html)
    * [Explain detail](https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment)
         
16. **background-blend-mode**
    * Thuộc tính định nghĩa làm thế nào ```background-image``` nên trộn với ```background-color``` của nó.
    * Values
    
    |Value|Explain|
    |-----|-------|
    |initial|Giá trị mặc định không trộn với ```background-color``` mà chồng chéo lên|
    |inherit|Kế thừa kiểu trộn ```blend-mode``` của phần tử cha|
    |normal|```background-color``` sẽ không chảy qua ```background-image```.Hay mặc định ```background-image``` chồng chéo lên|
    |multiply|```background-color``` và ```background-image``` sẽ được nhân lên và dẫn đến ảnh ```image``` sẽ tối hơn trước|
    |screen|Cả ```image``` và ```color``` bị đảo ngược, nhân lên và sau đó đảo ngược lại lần nữa|
    |overlay|```background-color``` sẽ trộn với ```background-image``` để phản chiếu độ sáng hoặc tối của phông nền|
    |lighten|Nếu ```background-image``` sáng hơn ```background-color``` thì image sẽ thay thế, ngược lại nó vẫn như cũ|
    |color-dodge|```background-color``` sẽ chia cho đảo ngược của ```background-image```|
    |color-burn|```background-color``` sẽ được đảo ngược, chia cho ```background-image``` và đảo ngược lại lần nữa|
    |hard-light|Nếu ```background-image``` sáng hơn ```background-color``` thì kết quả là ```mulipy``` hoặc nếu sáng hơn thì kết quả là ```screen```|
    |soft-light|kết quả cuối cùng tương tự như ```hard-light``` nhưng mềm hơn ở chỗ ánh sáng khuếch tán đặt trong image|
    |difference|Kết quả trừ đi màu tối của ```background-image``` và ```background-color```.Thường image sẽ có độ tương phản cao|
    |exclusion| Kết quả tương tự như ```difference``` với độ tương phản thấp|
    |hue|Kết quả màu sắc của ```background-image``` kết hợp với độ sáng và độ bão hòa của ```background-color```|
    |saturation|Giữ độ bão hòa của ```background-image``` trong khi trộn màu sắc và độ sáng của ```background-color```|
    |color|Giữ màu sắc và bão hòa của ```background-image``` và độ sáng của ```background-color```|
    |luminosity| Độ sáng của màu sắc trên cùng được giữ trong khi sử dụng bão hòa và màu sắc của ```background-color```|
    
    * [Explain Detail](https://css-tricks.com/almanac/properties/b/background-blend-mode/)
    
17. **background-clip**
    * Thuộc tính CSS thiết lập liệu element's background mở rộng dưới ```border-box```, ```padding-box```, hoặc ```content-box```
    * Values
    
    |Value|Explain|
    |-----|-------|
    |border-box|```background``` mở rộng ra rìa ngoài của border, nhưng nằm bên dưới border. Hay có ```z-index``` nhỏ hơn|
    |border-box|```background``` mở rộng ra rìa ngoài của padding.Không có ```background``` được vẽ bên dưới ```border```|
    |content-box|```background``` được vẽ trong khối nội dung(content box)|
   
18. **background-color**
    * Thuộc tính CSS thiết lập background-color của phần tử
    * Syntax
    
    |Syntax|Description|
    |------|-----------|
    |Keyword values| ```background-color: red```|
    |hex value| ```background-color: #bbff00```|
    |RGB value| ```background-color: rgb(1,1,1)```|
    |HSL value| ```background-color: hsl(50, 33%, 25%)```|

19. **background-position**
    * Thuộc tính CSS thiết lập vị trí ban đầu cho từng ```background-image```.Vị trí có liên quan đến vị trí layer được thiết lập bởi ```background-origin```
    * Position: Được định nghĩa tạo độ X/Y. X đại diện cho vị trí liên quan theo chiều ngang và Y đại diện cho vị trí liên quan theo chiều dọc. Giá trị đầu khai bao X và giá trị sau khai báo Y
    * Values
        1. 1-value syntax(cú pháp một giá trị):
           * Giá trị là ```center``` , thì image nằm ở chính giữa
           * Một trong giá trị từ khóa là ```top```,```left```,```bottom```,```right```.Thì được hiểu là 0% và trục còn lại mặc đinh là 50%.VD: ```top``` thì image nằm ở vị trí top 0% và trục X là 50%
           * Nếu khai báo 1 giá trị là phần trăm thì có nghĩa là X% và mặc định Y là 50%
        2. 2-value syntax(cú pháp hai giá trị):
           * Một trong giá trị từ khóa ```top```,```left```,```bottom```,```right```.Nếu có ```left``` hoặc ```right``` thì nó định nghĩa giá trị theo trục X là 0%. Nếu ```top``` hoặc ```bottom``` nó định nghĩa theo trục Y là 0%
           * Không thể khai báo 2 giá trị cùng một trục được. VD: ```background-position: top bottom```
        3. 3-value syntax(cú pháp ba giá trị)
           * Giá trị đầu tiên là một giá trị từ khóa ```top```,```left```,```bottom```,```right``` hoặc ```center```.
           * Có 2 trường hợp với kiểu khai báo này
               * ```background-position: Keyword-Value1 p% Keyword-Value2```: nghĩa là vị trí Keyword-Value1 p% và Keyword-value2 0%
               * ```background-position: Keyword-Value1 Keyword-Value2 p%```: nghĩa là vị trí Keyword-Value1 0% và Keyword-value2 mặc định p%
               
         4. 4-value syntax(cú pháp bốn giá trị):
            * ```background-position: keyword-value1 a% keyword-value2 b%```: nghĩa là vị trí Keyword-Value1 a% và Keyword-value2 b%
            
20. **background-repeat**
    * Thuộc tính thiết lập làm thế nào ```background-image``` được lặp lại.```Background-image``` có thể lặp lại theo trục ngang và trục dọc, hoặc không lặp cả hai hướng.
    * Syntax: ```background-repeat: value1 value2```. Value1 đại diện cho trục ngang và value2 đại diện cho trục dọc
    * Values
    
    |Value|Explain|
    |-----|-------|
    |repeat|```image``` sẽ được lặp nhiều nhất có thể để bao phủ diện tích của phần tử.```image``` cuối cùng sẽ bị cắt nếu nó không phù hợp|
    |space|```image``` sẽ được lặp nhiều nhất có thể mà không bị cắt xén.Ảnh đầu và cuối được ghim ở 2 bên của phần tử, và khoảng không gian được phân phối đều giữa các ảnh.Thuộc tính ```background-position``` được bỏ qua trừ khi chỉ có duy nhất một ảnh được hiển thị mà không bị cắt xén.Trường hợp duy nhất xảy ra cắt xén là không đủ diện tích để hiển thị một ảnh|
    |round|Các ```image``` sẽ lặp lại nhiều nhất có thể. Nếu không gian còn thừa lại lớn hơn hoặc bằng 1/2 của ```width origin image``` thì sẽ tự động add thêm một ```image``` và các ```image``` sẽ được co giãn lại ```width``` sao cho phù hợp với ```width element```|
    
    
21. **background-size**
    * Thuộc tính CSS thiết lập kích thước ```background-image``` của phần tử.Image có thế là kích thước tự nhiên, co giãn, hoặc hạn chế để phù hợp với không gian có sẵn.
    * Values:
         1. contain
             * Mở rộng image lớn nhất có thể mà không cắt hoặc co giãn image
             * Nó phụ thuộc vào ```min = Math.min(width, height)``` của phần tử để có thể lặp lại image
             * Nếu ```width``` hoặc ```height``` của phân tử lớn hơn ```min``` thì sẽ tự động lặp thêm image theo chiều đó.
             * Có thể sử dụng thuộc tính ```background-repeat``` nếu không muốn lặp thêm image
         2. cover
             * Mở rộng image lớn nhất có thể mà không co giãn image.
             * Nó phụ thuộc vào ```max = Math.min(width, height)```. Điểm khác biệt của thuộc tính ```cover``` so với ```contain``` là nó sẽ không bao giờ lặp lại image, thay vào đó nó thể dịch chuyển vị trí ```background-position: center``` tương đương với thẻ có kích thước ```max x max```
             * Ví dụ: nếu có 1 div có các giá trị là ```width = 200px``` và ```height = 300px```.Nó sẽ dịch chuyển image với vị trí ```background-position: center``` tương đương như thẻ có kích thước ```300x300```
         3. Percentage
             * Syntax: ```background-size: a%```
             * Định nghĩa image có kích thước là ```width * a%``` và ```height * a%``` trong đó ```width``` và ```height``` là kích thước của phần tử.
             
22. **blur()**
    * Hàm CSS ```blur()``` áp dụng ```Gaussian blur``` cho image. Nó sẽ làm nhòe image
    * Syntax: ```filter: blur(Xpx)```
    
23. **border**
    * Thuộc tính CSS ```border``` thiết lập đường viền của phần tử.Nó thiết lập giá trị của ```border-width```,```border-style``` và ```border-color```
    * Syntax: ```border: width | style | color|```
    * Example: ```border: 1px solid #ccc```
    
24. **border-style**
    * Thuộc tính thiết lập kiểu đường cho bốn bên của border element.
    * Syntax: ```border-style``` là thuộc tính có thể chỉ định một, hai, ba, hoặc bốn giá trị
    
      |Syntax|Explain|
      |------|-------|
      |Một giá trị| Nó sẽ áp dụng cho tất cả bốn cạnh của border|
      |Hai giá trị| Giá trị đầu tiên sẽ áp dụng cho ```top and bottom```, giá trị thứ hai cho ```left and right```|
      |Ba giá trị| Giá trị đầu tiên áp dụng cho ```top```, giá trị thứ hai cho ```left and right```, giá trị thứ ba cho ```bottom```|
      |Bốn giá trị| Áp dụng cho ```top, right, bottom, left``` theo đúng thứ tự kim đồng hồ|
      
