# 7. HTML Forms
## 7.1. Định nghĩa
- Các phần tử trong form có thể chứa các các kiểu phần tử khác nhau như các ô nhập dữ liệu (`textboxes`), các ô cho người dùng lựa chọn (`checkboxes` hoặc `radio buttons`), các nút cho người dùng kích gửi dữ liệu (`submit buttons`) và nhiều phần tử khác nữa.

- HTML Form là phương tiện cho người dùng nhập dữ liệu được gửi đến máy chủ để xử lý.
- Tại sao sử dụng HTML Form: HTML Form được sử dụng khi chúng ta muốn thu nhập một số dữ liệu của người truy cập trang web. VD như điền thông tin vào đơn đăng ký học online, địa chỉ để giao hàng...
- Khai báo HTML Form:
```html
<form action="server url" method="get|post">  
  //input controls ví dụ: textfield, textarea, radiobutton, button
</form>
```
## 7.2. Thẻ `<form>`
- Thẻ `<form>` được sử dụng để tạo một biểu mẫu HTML cho người dùng nhập dữ liệu vào.
- Bên trong thẻ `<form>` chứa các loại phần tử đầu vào  khác nhau như: `<textfields>`, `<checkboxes>`, `<radiobuttons>`, `submit buttons`, etc. 

## 7.3. Thuộc tính trong Form
### 7.3.1. Thuộc tính `action`
- Thuộc tính `action` định nghĩa hành động sẽ được thực hiện khi một biểu mẫu được gửi đi khi người dùng thực hiện click nút submit.
- Thông thường, dữ liệu biểu mẫu được gửi tới một tập tin trên máy chủ khi người dùng thực hiện click vào nút button.
- VD dưới đây, dữ liệu biểu mẫu được gửi tới một file gọi là "action_page.php" một script chạy ở phía server được xác định để xử lý biểu mẫu đã gửi: `<form action="/action_page.php">`

- *Nếu như thuộc tính `action` được bỏ qua, `action` sẽ được thiết lập tới trang hiện tại*

### 7.3.2. Thuộc tính `target`
- Thuộc tính `target` định nghĩa nơi hiển thị phản hồi sau khi thực hiện click nộp từ biểu mẫu.
- Thuộc tính `target` có thể có một trng những giá trị sau: (giống thẻ link).

    VD:
`<form action="/action_page.php" target="_blank">`

### 7.3.3. Thuộc tính `method`
- Thuộc tính `method` xác định kiểu phương thức HTTP (`GET hoặc POST`) được sử dụng gửi dữ liệu trên biểu mẫu.
- Phương thức HTTP `mặc định` khi gửi dữ liệu biểu mẫu là `GET`.
- VD: 
    - Sử dụng phương thức GET: `<form action="/action_page.php" method="get">` 
    - Sử dụng phương thức POST: `<form action="/action_page.php" method="post">` 

**Khi nào thì sử dụng phương thức POST và phương thức GET**
- Sử dụng `GET`:
    - Sử dụng GET nếu dữ liệu trong biểu mẫu gửi đi không cần mã hóa, không chứa các thông tin nhạy cảm như mật khẩu,...
    - Khi sử dụng GET, dữ liệu có trong biểu mẫu sẽ bị nhìn thấy trên thanh địa chỉ của trang, ví dụ:
    <p align="center">
    <img src="../images/lesson3/get.png" width=500>
    </p>

    <p align="center">
    <img src="../images/lesson3/url_get.png" width=500>
    </p>

    - Đặc điểm của GET: thêm dữ liệu vào thanh địa chỉ URL, theo cặp tên/giá trị như hình ảnh ví dụ bên trên.
    - Chiều dài của một URL bị giới hạn (2048 ký tự).

- Sử dụng `POST`: 
    - Nên sử dụng POST trong trường hợp nếu biểu mẫu cập nhật dữ liệu hoặc dữ liệu trên biểu mẫu gửi đi bao gồm các thông tin nhạy cảm như mật khẩu, mã thẻ ngân hàng,...
    - POST cung cấp cơ chế bảo mật hơn bởi vì dữ liệu được gửi đi không được hiển thị trên thanh địa chỉ của trang.
    - VD:
    <p align="center">
    <img src="../images/lesson3/post.png" width=500>
    </p>

    <p align="center">
    <img src="../images/lesson3/url_post.png" width=500>
    </p>

*Lưu ý:* Luôn sử dụng `POST` nếu dữ liệu trong biểu mẫu chưa những thông tin nhạy cảm và mang tính cá nhân
### 7.3.4. Thuộc tính `autocomplete`
- Thuộc tính tự động hoàn thành chỉ định xem biểu mẫu có nên bật hay tắt tính năng tự động hoàn thành hay không. 
- Khi bật tính năng tự động hoàn thành, trình duyệt sẽ tự động hoàn thành các giá trị dựa trên các giá trị mà người dùng đã nhập trước đó.
VD: `<form action="/action_page.php" autocomplete="on">`
    <p align="center">
    <img src="../images/lesson3/autocomplete.png" width=500>
    </p>

### 7.3.5. Thuộc tính `novalidate`
- Thuộc tính `novalidate` là một thuộc tính `boolean` 
- Khi xuất hiện, nó chỉ định rằng dữ liệu nhập vào  trong biểu mẫu không được xác thực khi nộp.
- VD: `<form action="/action_page.php" novalidate>`

## 7.4. Các phần tử của HTML form
- Bên trong phần tử `<form>` có thể chứa 1 hoặc nhiều phần tử biểu mẫu khác
### 7.4.1. Phần tử `<input>`
- Một trong những phần tử form quan trọng nhất là thẻ `<input>`
- Thẻ `<input>` có thể được hiển thị bằng một vài cách, phụ thuộc vào thuộc tính type.
### 7.4.1.1. `Input Type Text`
- `input type="text"`: định nghĩa một trường nhập dữ liệu trên 1 dòng.
    <p align = "center">
    <img width = 500 src="../images/lesson3/text_field.png">
    </p>
### 7.4.1.2. `Input Type password`
- `input type="password"`: định nghĩa một trường mật khẩu.
- Ký tự trong một trường mật khẩu được che dấu (mỗi ký tự khi hiển thị sẽ được thay bằng dấu hoa thị hoặc dấu tròn).
    <p align = "center">
    <img width = 500 src="../images/lesson3/password.png">
    </p>

### 7.4.1.3. `Input Type Submit`
- `input type="submit"`: định nghĩa một nút nhấn để gửi dữ liệu nhập trên biểu mẫu (`submiting`) tới một trang khác để xử lý dữ liệu của biểu mẫu này (`form_handler`). Form-handler thường là một trang chạy ở phía server cho phép xử lý dữ liệu nhập. 
- Form-handler được chỉ định trong thuộc tính `action` của form.
    <p align = "center">
    <img width = 500 src="../images/lesson3/submit.png">
    </p>
### 7.4.1.4. `Input Type Reset`
- `input type="reset"`: định nghĩa một nút nhấn reset để đặt lại tất cả những giá trị trên biểu mẫu về giá trị mặc định của chúng.
- VD: Khi chúng ta đã nhập dữ liệu vào biểu mẫu như ví dụ dưới đây. Sau đó chúng ta nhấn nút reset trên biểu mẫu thì các trường trên biểu mẫu sẽ được đặt lại thành các giá trị mặc định ban đầu
    - Dữ liệu đã nhập:
    <p align="center">
    <img src="../images/lesson3/reset1.png" width=500>
    </p>

    - Dữ liệu sau khi nhấn reset:
    <p align="center">
    <img src="../images/lesson3/reset2.png" width=500>
    </p>

### 7.4.1.5. `Input Radio Button`
- `input type="radio"`: định nghĩa một radio button. Các nút radio `chỉ cho phép người sử dụng chọn một` trong một danh sách giới hạn các lựa chọn
    <p align="center">
    <img src="../images/lesson3/radio.png" width=500>
    </p>
### 7.4.1.6. `Input Type Checkbox`
- `<input type="checkbox">`: định nghĩa một checkbox. Checkbox cho phép người dùng `không chọn hoặc chọn nhiều lựa chọn` trong một danh sách giới hạn các lựa chọn.

    <p align="center">
    <img src="../images/lesson3/checkbox.png" width=500>
    </p>

### 7.4.1.7. `Input Type Button`
- `<input type="button">`: định nghĩa một nút nhấn
    <p align="center">
    <img src="../images/lesson3/button.png" width=500>
    </p>

### 7.4.1.8. `Input Type Color`
- `<input type="color">`: được sử dụng cho trường đầu vào của biểu mẫu mà tại đó chứa một loại màu.
- Phụ thuộc vào sự hỗ trợ của các trình duyệt (không hỗ trợ cho trình duyệt Internet Explorer 11, Safari 9.1 hoặc các phiên bản trước đấy), một công cụ chọn màu có thể được hiển thị trong một trường đầu vào.

VD: <p align="center">
    <img src="../images/lesson3/type_color.png" width=500>
    </p>

### 7.4.1.9. `Input Type Date`
- `<input type="date">`: được sử dụng cho trường đầu vào mà ở đó chứa thông tin với định dạng tháng/ngày/năm (mm/dd/yyyy)
- Có thể sử dụng thuộc tính `max`, `min` để thêm giới hạn cho ngày nhập vào.
VD: <p align="center">
    <img src="../images/lesson3/dates.png" width=500>
    </p>
### 7.4.1.10. `Input Type Email`
- `<input type="email">`: được sử dụng cho trường đầu vào mà tại đó chứa một địa chỉ email.

```html
<form>
  <label for="email">Enter your email:</label>
  <input type="email" id="email" name="email">
</form>
```
- Một số loại điện thoại thông minh yêu cầu loại email phải có thêm đuôi `.com` để phù hợp với dữ liệu email nhập vào.

### 7.4.1.11. `Input Type Image`
- `<input type="image">` định nghĩa một hình ảnh như là một nút gửi (submit).
VD: 
```html
<form>
<input type="image" src="img_submit.gif" alt="Submit" width="48" height="48">
</form>
```
### 7.4.1.12. `Input Type File`
- `<input type="file">` định nghĩa một trường chọn tệp tin và một nút nhấn "Duyệt" để tải tập tin lên.
    <p align="center">
    <img src="../images/lesson3/type_file.png" width=500>
    </p>

### 7.4.1.13. `Input Type Hidden`
- `<input type="hidden">` định nghĩa một trường đầu vào bị ẩn đi (người dùng không xem được trường này).
- Một trường ẩn đi thường lưu trữ những gì mà cơ sở dữ liệu ghi lại để cập nhật dữ liệu khi biểu mẫu được gửi đi.  

*Lưu ý:* 
- Khi giá trị trong trường ẩn này không được hiển thị cho người dùng xem trên nội dung của trang web, nhưng nó có thể xem được (và có thể chỉnh sửa) bằng cách sử dụng bất kỳ công cụ phát triển web nào hoặc chức năng "Xem nguồn trang" trên trình duyệt
- Các trường `input hidden` thường được sử dụng để lưu trữ dữ liệu tạm thời trên web mà không cho người sử dụng nhìn thấy trực tiếp, các dữ liệu này thường sẽ vẫn xuất hiện trong cấu trúc html của web, vì vậy không nên lưu trữ các dữ liệu mang tính riêng tư, bảo mật hoặc bản quyền để tránh bị lộ khi người dùng biết một chút thủ thuật hoặc code về HTML.
    <p align="center">
    <img src="../images/lesson3/hidden.png" width=500>
    </p>

### 7.4.1.14. `Input Type Number`
- `<input type="number">` định nghĩa một trường nhập số học.
- Chúng ta cũng có thể đặt giới hạn cho những con số nào hợp lệ với thuộc tính `max` và `min`  
VD:
    ```html
    <form>
    <label for="quantity">Quantity (between 1 and 5):</label>
    <input type="number" id="quantity" name="quantity" min="1" max="5">
    </form>
    ```

### 7.4.1.15. `Input Type Range`
- `<input type="range">` định nghĩa 1 thanh trượt điều khiển cho việc nhập vào một con số. Giới hạn mặc định của thanh trượt là từ 0-100. Thuy nhiên, chúng ta có thể đặt giới hạn cho thanh trượt đó bằng thuộc tính `max`, `min` và `step`.  
VD:
    <p align="center">
    <img src="../images/lesson3/range.png" width=500>
    </p>

*Lưu ý:* Chúng ta có thể tham khảo thêm các loại input khác tại [HTML Input Types](https://www.w3schools.com/html/html_form_input_types.asp)
### 7.4.2. Thẻ `<label>`
- Thẻ `<label>` định nghĩa nhãn cho thành phần `<input>`.
- Thẻ `<label>` không hiển thị bất cứ gì đặc biệt cho người dùng, tuy nhiên nó cung cấp một cải thiện cho người sử dụng chuột, nếu click chuột vào nhãn, sẽ đưa con trỏ chuột vào vùng `<input>`.
- Muốn sử dụng hiệu quả `<label>`, cần thiết phải cho giá trị `id` của `<input>` trùng với giá trị `for` của `<label>`

VD: 
```html
<label for="male">Nam</label>: 
<input type="radio" id="male" name="gender" value="" /><br />
<label for="female">Nữ</label>:
<input type="radio" id="female" name="gender" value="" />
```
### 7.4.3. Phần tử `<select>`
- Phần tử `<select>` xác định một danh sách thả xuống
- Phần tử `<option>` được sử dụng để định nghĩa 1 lựa chọn có thể được chọn trong danh sách.
- Mặc định, lựa chọn đầu tiên trong danh sách là đã được chọn.
- Để định nghĩa một lựa chọn mặc định, thêm thuộc tính `selected` vào lựa chọn đấy  
VD:
    <p align="center">
    <img src="../images/lesson3/select.png" width=500>
    </p>

### 7.4.4. Phần tử `<textarea>`
- Phần tử `<textarea>` định nghĩa một trường nhập dữ liệu nhiều dòng (một vùng văn bản).
- Sử dụng thuộc tính rows và cols để chỉ định số lượng dòng và chiều dài của một vùng văn bản có thể nhìn thấy trên trình duyệt.  
VD:
    <p align="center">
    <img src="../images/lesson3/textarea.png" width=500>
    </p>
- Chúng ta cũng có thể định nghĩa kích thước của vùng văn bản bằng thuộc tính `style` CSS 
```html
<textarea name="message" style="width:200px; height:600px;">
The cat was playing in the garden.
</textarea>
```
### 7.4.5. Phần tử `<fieldset>` và `<legend>`

- Phần tử `<fieldset>` được sử dụng để nhóm các dữ liệu liên quan vào trong một biểu mẫu.
- Phần tử `<legend>` định nghĩa một tiêu đều cho phần tử `<fieldset>`

VD:
    <p align="center">
    <img src="../images/lesson3/fieldset.png" width=500>
    </p>
### 7.4.6. Phần tử `<datalist>`
- Phần tử `<datalist>` chỉ định danh sách các tùy chọn được xác định trước cho một phần tử `<input>`.

- Người dùng sẽ thấy danh sách thả xuống gồm các tùy chọn được xác định trước khi họ nhập dữ liệu.

- Thuộc tính `list` của phần tử `<input>`, phải tham chiếu đến thuộc tính `id` của phần tử `<datalist>`.

VD:
    <p align="center">
    <img src="../images/lesson3/datalist.png" width=500>
    </p>
 
 ***Lưu ý:* Sự khác biệt giữa `<select>` và `<datalist>`**
 - Với `<select>`, người dùng chỉ có thể chọn các giá trị đã được liệt kê ra trong danh sách bằng các thẻ `<option>`. Còn với `<datalist>`, người dùng có thể chọn 1 trong các giá trị trong danh sách hoặc có thể nhập 1 giá trị lựa chọn khác không có trong danh sách bằng trường input.
 - Điểm khác thứ 2: với `<select>` sẽ luôn có một giá trị được mặc định trước, còn `<datalist>` thì không có giá trị mặc định cho trường input.
### 7.4.7. Phần tử `<output>`
- Phần tử `<output>` đại diện cho kết quả của một phép tính (giống như một phép tính được thực hiện bởi tập lệnh).

VD:
    <p align="center">
    <img src="../images/lesson3/output.png" width=500>
    </p>

## 7.5. Thuộc tính trong HTML Input
### 7.5.1. Thuộc tính `value`
- Thuộc tính `value` định nghĩa một giá trị đầu tiên (mặc định) cho trường nhập dữ liệu đầu vào.
VD: <p align="center">
    <img src="../images/lesson3/get.png" width=500>
    </p>

### 7.5.2. Thuộc tính `readonly`
- Thuộc tính `readonly` định nghĩa một trường dữ liệu `chỉ đọc, không thể chỉnh sửa`
- Giá trị của trường này cũng sẽ được gửi khi thực hiện gửi biểu mẫu.
VD: `<input type="text" id="fname" name="fname" value="John" readonly>`
<input type="text" id="fname" name="fname" value="John" readonly><br>

### 7.5.3. Thuộc tính `disabled`
- Thuộc tính `disabled` định nghĩa một trường nhập dữ liệu bị vô hiệu hóa, tức là nó `không được sử dụng và không thể nhấp vào.`
- Giá trị của trường này cũng không được gửi đi.

VD: `<input type="text" id="fname" name="fname" value="John" disabled><br>`
<input type="text" id="fname" name="fname" value="John" disabled><br>

### 7.5.4. Thuộc tính `size`
- Thuộc tính `size` định nghĩa chiều dài có thể nhìn thấy trên trình duyệt của một trường dữ liệu. Giá trị mặc định của `size` là 20.
- Thuộc tính `size` chỉ hoạt động với những loại input sau: `text, search, email, password, tel, url`.

VD:
`<input type="text" id="fname" name="fname" value="John" size="4">`
<input type="text" id="fname" name="fname" value="John" size="4">

`<input type="text" id="fname" name="fname" value="John" size="10">`
<input type="text" id="fname" name="fname" value="John" size="10">

### 7.5.5. Thuộc tính `maxlength`
- Thuộc tính `maxlength` định nghĩa số lượng ký tự tối đa được nhập vào một trường dữ liệu nhập vào.
- Khi một thuộc tính `maxlength` được thiết lập, thì trường dữ liệu đó sẽ không được nhập quá số lượng ký tự đã quy định.

VD: `<input type="text" id="fname" name="fname" value="John" maxlength="4">`

### 7.5.6. Thuộc tính `max` và `min`
- Thuộc tính `max` và `min` chỉ định giá trị tối thiểu và tối đa có thể nhập vào trong một trường dữ liệu.
- Sử dụng đồng thời hai thuộc tính này sẽ tạo thành một phạm vi của giá trị hợp lệ.  
VD:
```html
<form>
  <label for="datemax">Enter a date before 1980-01-01:</label>
  <input type="date" id="datemax" name="datemax" max="1979-12-31"><br><br>

  <label for="datemin">Enter a date after 2000-01-01:</label>
  <input type="date" id="datemin" name="datemin" min="2000-01-02"><br><br>

  <label for="quantity">Quantity (between 1 and 5):</label>
  <input type="number" id="quantity" name="quantity" min="1" max="5">
</form>
```

### 7.5.7. Thuộc tính `multiple`
- Thuộc tính `multiple` định nghĩa rằng người dùng `có thể nhập vào nhiều hơn 1 giá trị` cho mỗi trường dữ liệu.
- Thuộc tính `multiple` hoạt động đối với loại input: `email` và `file`

VD: `<input type="file" id="files" name="files" multiple>`
    <p align="center">
    <img src="../images/lesson3/multiple.png" width=500>
    </p>
### 7.5.8. Thuộc tính `pattern`
- Thuộc tính `pattern` định nghĩa một biểu thức chính quy mà giá trị của trường nhập dữ liệu phải dựa vào biểu thức đó để kiểm tra khi biểu mẫu được gửi đi.
- Sử dụng thuộc tính `title` để mô tả một mẫu giúp người dùng hiểu.

VD: Nhập vào 1 số điện thoại có 10 chữ số (không có chữ cái và ký tự đặc biệt)

`<input type="text" id="phonenumber" pattern="[0-9]{10}" title="A Phone number has ten numbers">`

### 7.5.9. Thuộc tính `placeholder`
- Thuộc tính `placeholder` định nghĩa một gợi ý ngắn để định nghĩa những giá trị được mong đợi của một trường nhập dữ liệu.
- Một gợi ý ngắn sẽ được hiển thị trong trường nhập dữ liệu trước khi người dùng nhập một giá trị vào.
- Thuộc tính `placeholder` hoạt động với những loại input sau: `text, search, email, password`.

VD:
    <p align="center">
    <img src="../images/lesson3/placeholder.png" width=500>
    </p>

### 7.5.10. Thuộc tính `required` 
- Thuộc tính `required` định nghĩa một trường dữ liệu phải được nhập vào trước khi thực hiện việc gửi biểu mẫu đi.
- Thuộc tính `required` hoạt động với những loại input: `text, search, email, password, radio`...

VD: 
    <p align="center">
    <img src="../images/lesson3/required.png" width=500>
    </p>

### 7.5.11. Thuộc tính `autofocus`
- Thuộc tính `autofocus` định nghĩa rằng một trường dữ liệu sẽ `tự động được chỉ định` khi trang web được tải.  

VD:
```html
<label for="fname">First name:</label>

<input type="text" id="fname" name="fname" autofocus><br>
```

<label for="fname">First name:</label>
<input type="text" id="fname" name="fname" autofocus><br>

### 7.5.12. Thuộc tính `height` và `width`
- Thuộc tính `height` và `width` xác định chiều cao và độ rộng của một phần tử `<input type="image">`
- `Luôn chỉ định cả thuộc tính chiều cao và chiều rộng cho hình ảnh`. Nếu chiều cao và chiều rộng được thiết lập, không gian cần thiết cho hình ảnh sẽ được dành riêng khi trang được tải. Nếu không có các thuộc tính này, trình duyệt không biết kích thước của hình ảnh và không thể dành không gian thích hợp cho nó. Hiệu quả sẽ là bố cục trang sẽ thay đổi trong quá trình tải (trong khi tải hình ảnh).

VD: `<input type="image" src="img_submit.gif" alt="Submit" width="48" height="48">`

### 7.5.13. Thuộc tính `list`
- Thuộc tính `list` liên quan đến một phần tử `<datalist>` mà chứa những lựa chọn được xác định trước cho một phần tử `<input>`.
- Thuộc tính `list` của phần tử `<input>` và thuộc tính `id` của phần tử `<datalist>` `phải có giá trị trùng nhau`.

VD:
```html
<form>
  <input list="browsers">
  <datalist id="browsers">
    <option value="Internet Explorer">
    <option value="Firefox">
    <option value="Chrome">
    <option value="Opera">
    <option value="Safari">
  </datalist>
</form>
```

### 7.5.14. Thuộc tính `autocomplete`
- Thuộc tính `autocomplete` định nghĩa một biểu mẫu hay một trường dữ liệu có tự động được hoàn thành hay không.
- `Autocomplete` cho phép những trình duyệt dự đoán trước những giá trị. Khi người dùng bắt đầu nhập vào một trường, trình duyệt hiển thị ra những lựa chọn để điền vào trường dữ liệu đó, dựa trên những giá trị  đã được nhập trước đó.

- VD:
    - Trường Firstname sử dụng thuộc tính `autocomplete = "on"`
    <p align="center">
    <img src="../images/lesson3/auto.png" width=500>
    </p>
    - Trường Firstname sử dụng thuộc tính `autocomplete = "off"`
    <p align="center">
    <img src="../images/lesson3/auto_off.png" width=500>
    </p>

## 7.6. Thuộc tính `form*` cho phần tử `<input>`
### 7.6.1. Thuộc tính `form`
- Thuộc tính `form` định nghĩa biểu mẫu mà phần tử `<input>` phụ thuộc vào.
- Giá trị của thuộc tính này phải `trùng với` giá trị của `thuộc tính id `của thẻ `<form>` mà `nó phụ thuộc`.
VD:
 ```html
<form action="/action_page.php" id="form1">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <input type="submit" value="Submit">
</form>

<label for="lname">Last name:</label>
<input type="text" id="lname" name="lname" form="form1">
```
### 7.6.2. Thuộc tính `formaction`
- Thuộc tính `formaction` định nghĩa tệp tin URL mà sẽ xử lý dữ liệu của biểu mẫu khi nó được gửi đi.
- Thuộc tính này sẽ ghi đè thuộc tính `action` của phần tử <form>.
- Thuộc tính này hoạt động với loại input: submit và image.

VD:
```html
<form action="/action_page.php">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <input type="submit" value="Submit">
  <input type="submit" formaction="/action_page2.php" value="Submit as Admin">
</form>
```

### 7.6.3. Thuộc tính `formenctype`
- Thuộc tính `formenctype` định nghĩa cách mà dữ liệu biểu mẫu được mã hóa khi gửi đi (`chỉ xảy ra đối với biểu mẫu có method = "post"`)
- Thuộc tính này ghi đè thuộc tính `enctype` của phần tử <form>.
- Thuộc tính này hoạt động với loại input: submit và image.

VD: Một biểu mẫu có hai nút gửi. Đầu tiên gửi dữ liệu biểu mẫu với mã hóa mặc định, thứ hai gửi dữ liệu biểu mẫu được mã hóa dưới dạng "multipart/form-data":
```html
<form action="/action_page_binary.asp" method="post">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <input type="submit" value="Submit">
  <input type="submit" formenctype="multipart/form-data"
  value="Submit as Multipart/form-data">
</form>
```
- Ngoài ra còn có thuộc tính formenctype cho `<button>`
VD: Một biểu mẫu có hai nút gửi. Nút gửi đầu tiên gửi dữ liệu biểu mẫu với mã hóa ký tự mặc định và nút thứ hai gửi dữ liệu biểu mẫu không có mã hóa ký tự:

<p align="center">
<img src="../images/lesson3/button_formenctype.png" width=500>
</p>

### 7.6.4. Thuộc tính `formmethod`
- Thuộc tính `formmethod` định nghĩa giao thức HTTP cho việc gửi dữ liệu biểu mẫu tới URL xử lý.
- Thuộc tính này sẽ ghi đè thuộc tính `action` của phần tử <form>.
- Thuộc tính này hoạt động với loại input: submit và image.
- Dữ liệu biểu mẫu có thể được gửi như `các biến URL (method="get")` hoặc như `một giao dịch HTTP post (method = "post")
`
### 7.6.7. Thuộc tính `formtarget`
- Thuộc tính `formtarget` định nghĩa một tên hoặc một từ khóa mà chỉ định nơi mà hiển thị những phản hồi sau khi dữ liệu biểu mẫu được gửi đi.
- Thuộc tính này ghi đè thuộc tính `target` của phần tử `<form>`.
- Thuộc tính này hoạt động với loại input: submit và image.

VD: Kết quả khi nhấn hai nút nhấn submit sẽ hiện thị trên các cửa sổ khác nhau
```html
<form action="/action_page.php">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <input type="submit" value="Submit">
  <input type="submit" formtarget="_blank" value="Submit to a new window/tab">
</form>
```
### 7.6.8. Thuộc tính `formnovalidate`
- Thuộc tính `formnovalidate` định nghĩa một phần tử `<input>` không được xác thực khi gửi đi.
- Thuộc tính này ghi đè thuộc tính `novalidate` của phần tử `<form>`.
- Thuộc tính này hoạt động với loại input: submit

VD:
```html
<form action="/action_page.php">
  <label for="email">Enter your email:</label>
  <input type="email" id="email" name="email"><br><br>
  <input type="submit" value="Submit">
  <input type="submit" formnovalidate="formnovalidate"
  value="Submit without validation">
</form>
```
# 8. HTML Multimedia
## 8.1. Định nghĩa
- `Multimedia` (đa phương tiện) có rất nhiều định dạng khác nhau. Nó có thể là bất cứ cái gì mà bạn nghe hoặc nhìn được, ví dụ như hình ảnh, âm nhạc, âm thanh, video, bản ghi, phim, hình ảnh động,...
- Trên trang web thường chứa rất nhiều định dạng, kiểu loại khác nhau của những phần tử đa phương tiện.
- Định dạng đa phương tiện: các phần tử đa phương tiện (như audio, video) được lưu trữ trong tệp tin phương tiện (media file). Cách thông thường nhất để nhận biết loại tập tin là xem phần mở rộng của tệp tin. Tệp tin đa phương tiện thường có những phần mở rộng như: `.wav`, `.mp3`, `.mp4`, `.mpg`, `.wmv`, `.avi`

## 8.2. HTML Video
- Phần tử `<video>` được sử dụng để hiển thị một video trên HTML.

VD:
    <p align="center">
    <img src="../images/lesson3/video.png" width=500>
    </p>

- Trong ví dụ trên:
    - Thuộc tính `controls` được thêm vào trong phần tử `<video>` để điều khiển một video như: `play (chạy video)`, `pause (dừng video)` và `volume (điều chỉnh âm lượng)`.
    - Luôn khai báo thuộc tính `width` và `height`. Nếu như không thiết lập hai thuộc tính này, trang web có thể bị nhấp nháy khi tải video.
    - Phần tử `<source>` cho phép chỉ định tệp video thay thế mà trình duyệt có thể chọn. Trình duyệt sẽ sử dụng định dạng được phát hiện đầu tiên.
    - `Phần văn bản` ở giữa cặp thẻ `<video> </video>` sẽ `chỉ được hiển thị` lên trình duyệt khi mà `trình duyệt đó không hỗ trợ` phần tử HTML `<video>`.

- HTML `<video>` autoplay:
    - Để tự động phát một video, sử dụng thuộc tính `autoplay`

    VD: 
    ```html
    <video width="320" height="240" autoplay>
        <source src="movie.mp4" type="video/mp4">
        <source src="movie.ogg" type="video/ogg">
        Your browser does not support the video tag.
    </video>
    ```
    - Để `tắt tiếng` của video, ta thêm `muted` đằng sau của thuộc tính `autoplay`:  
    `<video width="320" height="240" autoplay muted>`
## 8.3. HTML audio
- Để phát một tệp tin âm thanh, ta sử dụng phần tử `<audio>`.

VD:
    <p align="center">
    <img src="../images/lesson3/audio.png" width=500>
    </p>
- Trong ví dụ trên:
    - Thuộc tính `controls` được thêm vào trong phần tử `<audio>` để điều khiển một video như: `play (chạy)`, `pause (dừng)` và `volume (điều chỉnh âm lượng)`.
    - Phần tử `<source>` cho phép chỉ định tệp âm thanh thay thế mà trình duyệt có thể chọn. Trình duyệt sẽ sử dụng định dạng được phát hiện đầu tiên.
    - `Phần văn bản` ở giữa cặp thẻ `<audio> </audio>` sẽ `chỉ được hiển thị` lên trình duyệt khi mà `trình duyệt đó không hỗ trợ` phần tử HTML `<audio>`.

- HTML `<audio>` autoplay:
    - Để tự động phát một âm thanh, sử dụng thuộc tính `autoplay`

    VD: 
    ```html
    <audio width="320" height="240" controls autoplay>
        <source src="movie.mp4" type="video/mp4">
        <source src="movie.ogg" type="video/ogg">
        Your browser does not support the video tag.
    </audio>
    ```
    - Để `tắt tiếng` của video, ta thêm `muted` đằng sau của thuộc tính `autoplay`:  
    `<video width="320" height="240" controls autoplay muted>`

## 8.4. HTML Plug-ins
- `Plug-ins` (`công cụ/chương trình cài cắm`) là những chương trình máy tính để mở rộng những chức năng tiêu chuẩn của trình duyệt.
- Plug-ins được thiết kế để sử dụng cho những mục đích khác nhau:
    - Để chạy những ứng dụng Java.
    - Để hiển thị phim Flash.
    - Để hiển thị bản đồ
    - Để quét vi-rút.
    - Để xác thực mã ngân hàng.

- Phần tử `<object>`
    - Phần tử `<object>` hỗ trợ cho tất cả các trình duyệt.
    - Phần tử `<object>` định nghĩa một đối tượng được nhúng vào trong một tài liệu HTML.
    - Nó được thiết kế để nhúng các bộ cài cắm (như ứng dụng Java, trình đọc PDF,...) vào trang web, nhưng cũng có thể sử dụng để bao gồm HTML trong HTML:  
    VD: `<object width="100%" height="500px" data="snippet.html"></object>`
- Phần tử `<embed>`
    - Phần tử `<embed>` được hỗ trợ cho tất cả các trình duyệt chính.
    - Phần tử `<embed>` định nghĩa một đối tượng được nhúng vào trong một tài liệu HTML. VD: `<embed src="audi.jpeg">`
    - Phần tử `<embed>` không có thẻ đóng và nó không chứa đoạn văn để thay thế
    - Phần tử `<embed>` cũng có thể bao gồm HTML trong HTML. VD: `<embed width="100%" height="500px" src="snippet.html">`

## 8.5. HTML Youtube Videos
- Cách dễ nhất để hiển thị video trên HTML là sử dụng `Youtube`.
- Chuyển videos sang những định dạng khác nhau có thể khó và tốn thời gian. Vì vậy, một giải pháp dễ hơn là để Youtube phát videos trên trang web.
- `Youtube video id`: youtube sẽ hiển thị một `id` (như tgbNymZ7vqY) khi chúng ta lưu (hoặc chạy) một video. Chúng ta có thể sử dụng `id` này để tham chiếu tới video của chúng ta trong đoạn mã HTML.
### 8.5.1. Phát một video Youtube trong HTML
- Để phát một video trên một trang web, thực hiện các bước sau:
    - Tải video lên Youtube.
    - Ghi lại id của video.
    - Định nghĩa một thẻ `<iframe>` trên trang web của chúng ta.
    - Đặt thuộc tính src chỉ tới địa chỉ URL của video
    - Sử dụng thuộc tính `width`, `height` để định nghĩa `kích thước` của trình phát video.
    - Thêm những thông số bất kỳ khác tới URL (*theo dõi phần 8.5.2*).  
    VD: 
    <p align="center">
    <img src="../images/lesson3/youtube.png" width=500>
    </p>

### 8.5.2 Một số thông số có thể thêm vào URL
- `Youtube Autoplay + Mute`
    - Chúng ta có thể `để video của mình phát một cách tự động` khi một người dùng ghé thăm trang web, bằng cách `thêm` `autoplay = 1` vào địa chỉ URL của youtube. Ngoài ra có thể thêm `mute = 1 sau autoplay=1 để phát video tự động nhưng tắt tiếng`

    VD: 
    <p align="center">
    <img src="../images/lesson3/auto_mute.png" width=500>
    </p>

- `Youtube Loop`
    - Thêm `loop=1` để video của chúng ta `lặp lại mãi mãi`. Mặc định, l`oop=0` video sẽ `chỉ chạy 1 lần`.

    VD:
    ```html
    <iframe width="420" height="315"
    src="https://www.youtube.com/embed/tgbNymZ7vqY?playlist=tgbNymZ7vqY&loop=1">
    </iframe>
    ```

- `Youtube Controls`
    - Thêm `controls=0` để `tắt phần điều khiển` trên trình phát video. Mặc định `controls=1` là `phần điều khiển sẽ được hiển thị`.  

    VD:
    ```html
    <iframe width="420" height="315"
    src="https://www.youtube.com/embed/tgbNymZ7vqY?controls=0">
    </iframe>
    ```