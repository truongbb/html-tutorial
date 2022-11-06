# HTML Assignment 04 - Bài tập HTML 04

Cho các ảnh ở file [này](./archives/allpics.zip), danh sách của chúng được liệt kê như sau:

- acacia.jpg
- acacia_th.jpg (??? x ???)
- adm_records_th.jpg (200 x 150)
- bookstore_th.jpg (247 x 150)
- cafeteria_th.jpg (183 x 150)
- cedro.jpg
- cedro_th.jpg (??? x ???)
- chavez_grove_th.jpg (200 x 150)
- library_th.jpg (200 x 150)
- rg240_th.jpg (247 x 150)
- roble.jpg
- roble_th.jpg (??? x ???)
- sequoia.jpg
- sequoia_th.jpg (??? x ???)

Đối với các ảnh đã được ghi rõ kích thước, hãy sử dụng kích thước đó để xây dựng web của bạn, với các ảnh còn lại, hãy tự tìm ra kích thước phù hợp để xây dựng web.

***Chú ý***: Tất cả các thẻ `<img>` ở trong bài này thì đều phải sử dụng đúng chiều dài và chiều rộng của anh

## Yêu cầu chung

- Tất cả các đường dẫn (links) và ảnh (images) **bắt buộc** sử dụng đường dẫn tương đối (relative paths)
- Tất cả các thành phần là ký tự đều được bao bọc trong thẻ `<p>` hoặc `<div>`
- Không sử dụng thẻ `<center>`

## Yêu cầu chi tiết

### 1. File `register.html`

Đoạn văn bản dưới đây là nội dung của file `register.html`. Những hướng dẫn trong dấu ngoặc vuông là các yêu cầu cần được hoàn thiện
```
[Title of page is "EVC Registration"]

[ level 1 heading ] Registering at Evergreen Valley College

[insert image adm_records_th.jpg] The
Admissions and Records Building is the place where you can register
for classes online or in person. This is also
the place where you: [this should be a bulleted list]

   * pay your fees
   * get transcripts
   * check course availability

[insert image bookstore_th.jpg]
After you have registered, you need to go to the
bookstore on the upper level of the Gullo Student Center
to pick up the books for your courses.

[horizontal rule]

[insert image cafeteria_th.jpg]
When you need a break, go to cafeteria on the lower level
of the Gullo Student Center.
```

### 2. File `buildings.html`

Đoạn văn bản dưới đây là nội dung của file `buildings.html`. Những hướng dẫn trong dấu ngoặc vuông là các yêu cầu cần được hoàn thiện
```
[Title of page is "EVC Classroom Buildings"]

[ level 1 heading ] Evergreen Valley College Classroom Buildings


Click any picture on this page to see a larger version of it.

[insert images acacia_th.jpg and sequoia_th.jpg side by
side. The words "Acacia and Sequoia" should appear
beneath the two pictures.]

The Acacia and Sequoia buildings are on the northeast side of
the campus. The Sequoia building is the newest of the campus
classrooms, with the most modern facilities in its lecture rooms.

[insert images roble_th.jpg and cedro_th.jpg side by
side. The words "Roble and Cedro" should appear
beneath the two pictures.]

The Roble and Cedro buildings are located on the northwest
side of the campus.
```

Tất cả các ảnh của file `buildings.html` đều click vào được (clickable) - có hình bàn tay đi di chuột vào vùng ảnh, khi click vào ảnh sẽ xem được ảnh gốc. Bảng dưới đây sẽ nêu rõ khi click vào ảnh nào thì ảnh nào sẽ được hiển thị ra

| Khi click vào ảnh này |Thì ảnh này sẽ hiện ra |
|---	|---	|
| acacia_th.jpg | acacia.jpg |
| cedro_th.jpg | cedro.jpg |
| roble_th.jpg | roble.jpg |
| sequoia_th.jpg | sequoia.jpg |


### 2. File `miscellaneous.html`

Đoạn văn bản dưới đây là nội dung của file `miscellaneous.html`. Những hướng dẫn trong dấu ngoặc vuông là các yêu cầu cần được hoàn thiện

```
[Title of page is "EVC Miscellanea"]

[ level 1 heading ] Evergreen Valley College Miscellanea

[ level 2 heading ] Computing Facilities

[insert image rg240_th.jpg]
Evergreen Valley College has several computer labs where
students can do their work for their Business Information Systems
or Computer Information Technology courses. At the right you see
the Windows computer lab in room RG-240.

[horizontal rule]

[insert image chavez_grove_th.jpg] One of
the places that you can go to relax and enjoy the weather is Cesar E.
Chavez Grove, near the lower level of the old Learning Resource Center.

[horizontal rule]

[image library_th.jpg]
The Library and Educational Technology Center is one of the newest
buildings on campus.
```