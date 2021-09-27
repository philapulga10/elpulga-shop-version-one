- 4. Làm quen với CSS
  - 15. Đơn vị trong CSS
    - 1. Absolute units?
    - 2. Relative units? => cần 1 nơi phụ thuộc vào
      - % phụ thuộc vào kích thước của thẻ chứa nó
      - rem phụ thuộc vào font-size của thẻ HTML
      - em phụ thuộc vào thẻ gần gần chứa nó có thuộc tính font-size
      - vw (witdh): 1vw => 1% chiều ngang của trình duyệt
      - vh (height): 1vh => 1% chiều ngang của trình duyệt
    - thường sử dụng rem
    - ví dụ tình huống áp dụng: có nhiều nơi hiển thị chữ => muốn toàn bộ chữ to lên => dùng rem => tăng font-size của thẻ HTML => còn em thì phải sửa nhiều nơi
    - viewport: là khung nhìn, độ rộng của trình duyệt
    *** chiều ngang của thẻ body phụ thuộc vào chiều ngang kích thước của trình duyệt
  - 17. Pseudo classes
    - :root => phần tử HTML
  - 18. Pseudo elements
    - sử dụng để tạo ra những phần tử trên website mà không cần phải viết mã HTML, chỉ cần viết CSS thui
    - content: ''; => giúp element có thể tồn tại được
    - mặc định thẻ div đã được trình duyệt gán cho display: block; rồi => còn đổi với Pseudo elements muốn có tính chất khối giống thẻ div => phải chủ động thêm display: block;
    - ::before
      ::after
      ::first-letter
      ::first-line
      ::selection
- 5. Đệm, viền và khoảng lề
  - 20. CSS Border
    - mặc định nếu không set width cho border thì border sẽ có kích thước là 2px
  - 21. CSS Margin
    - 
  - 22. CSS Box-sizing
    - một box khi thêm padding hay border sẽ làm cho kích thước box tăng lên => tốn công tính toán => sử dụng box-sizing: border-box => lúc này box-sizing sẽ hiểu chiều ngang element của ta sẽ bằng tổng kích thước border + padding + content
    - thường dùng trong base CSS
    - mặc định box-sizing: content-box
    - box-sizing: unset
- 6. Thuộc tính tạo nền
  - 23. CSS Background-clip
    - quyết định background được đổ từ ranh giới nào
    - background-clip: border-box => đổ từ border
    - background-clip: padding-box
    - background-clip: content-box
  - 24. CSS Background-image
    - nếu chỉ set background-size: 100px; => chiều cao sẽ được set auto đúng tỷ lệ của ảnh
    - mặc định background-image: no-repeat;
    - background-image: no-repeat;
    - nếu chỉ set background-size: 100%; => chiều cao sẽ được set auto => không bị méo ảnh
    - nếu set background-size: 100% 100px; => sẽ bị méo ảnh
    - nếu set background-size: auto auto; => như lúc đầu
    - background-image: linear-gradient(0, #333, #ccc);
    - #333 => mã màu thập lục phân => có thể lấy từ design của designer => hoặc lấy từ devtools khi ta làm website giống website khác
    - nếu muốn mã màu #333 ở dạng trong suốt => rgba();
  - 25. CSS Background-size keywords
    - background-size: contain;
    - background-size: cover;
  - 26. CSS Background-origin
    - đi kèm với background-image
    - mặc định là background-origin: padding-box;
    - background-origin: border-box;
    - background-origin: content-box;
  - 27. CSS Background-position
    - background-position: bottom center;
    - background-position: 50px 50px;
    - background-position: 10% center;
    - background-position: top 20px right 30px;
  - 29. CSS Position: Relative
    - không phụ thuộc vào đối tượng nào khác, nó sẽ lấy chính vị trí của nó đang đứng làm gốc tọa độ
  - 30. CSS Position: Absolute
    - phục thuộc vào thẻ cha gần nhất có thuộc tính position (không phân biệt giá trị, có thể là relative, absolute, fixed, sticky) để lấy thẻ cha đó làm gốc tọa độ
    - nhìn layout => có 1 đối tượng là con của đối tượng khác => cần di chuyển vị trí của đối tượng con xung quanh đối tượng cha => sử dụng position
  - 72. Reset CSS
    - mặc định trình duyệt sẽ có những thuộc tính mặc định cho một số thẻ HTML của chúng ta ==> khi không muốn sử dụng những giá trị mặc định này ==> reset nó
    - những giá trị mặc định này không phải trình duyệt nào cũng giống nhau
    ==> cần chủ động CSS cho những thẻ HTML 1 giá trị mặc định ngay từ đầu ==> để trên mọi trình duyệt ==> những giá trị này sẽ là quy chuẩn do ta đặt ra thay vì ta cứ sử dụng những quy chuẩn do trình duyệt áp đặt
    - *** normalize - cdnjs.com
  - 73. Dựng base CSS
    - *** selector *: apply tất cả các thuộc tính CSS lên tất cả các phần tử HTML được nhúng file này
  - 74. Dựng khung web
    - Nếu xem header là 1 block ==> con của header là element ==> tên class là header__navbar ==> nếu thêm class modified ==> header__navbar--modified
  - 75. Navbar CSS
    - nếu màu nên là màu chuyển ==> sử dụng background-image
    *** user agent stylesheet: là những thuộc tính CSS mà trình duyệt đang apply vào thẻ ta đang select
    *** display: block ==> giúp ta có thể đặt chiều ngang, chiều dọc cho element và nó có thể kế thừa chiều ngang của thẻ chứa nó
    *** thẻ html không có thẻ cha ==> nó có display: block ==> nó kế thừa chiều ngang của trình duyệt ==> body có display: block ==> nó kế thừa chiều ngang của thẻ HTML ==> nó kế thừa chiều ngang của trình duyệt ==> cứ như vậy header tag cũng được kế thừa chiều ngang của trình duyệt
    *** link trong video hướng dẫn: <link href="https://fonts.googleapis.com/css2?family=Roboto:300,400,500;700&display=swap&subset=vietnamese" rel="stylesheet">
    *** transform: translateY(-50%) ==> -50% kích thước chiều cao của chính nó
  - 76. Nhúng Font-Icons
    - fontawesome thực ra chỉ là 1 file css được viết sẵn (đã định nghĩa ra những class) ==> chỉ lấy ra dùng
  - 77. Icons CSS
    - thẻ span sinh ra chỉ với mục đích css cho 1 element
    *** khi hover chẻ cha ==> nếu thẻ con đã ghi đè thuộc tính của thẻ cha thì thẻ con sẽ không được ảnh hưởng bởi hover
  - 78. Header QR code CSS
    - khi phần tử con có top: x% ==> x% theo chiều cao của thành phần cha
    *** <i></i> mới apply được thuộc tính font-size, còn <img> thì apply được thuộc tính height
  - 92. Header cart - List products
    - tại sao margin của thẻ heading lại khác với trong bản của sơn đặng
  - 99. Danh mục CSS
    - khi bên trong 1 tag là 1 thẻ <i></i> và 1 text mà ta chỉnh font-size tag cha ==> 2 element bên trong sẽ bị ảnh hưởng font-size
  - 101. CSS: Sắp xếp sản phẩm
    - tìm hiểu về margin auto
  - 103. Sản phẩm CSS
    - theo tỷ lệ chuẩn khuyến cáo trên PC thì khoảng cách giữa các cột là 24px => chúng ta cũng có thể thay đổi => như shopee nhiều sản phẩm
    *** browser mặc định sẽ apply các thuộc tính margin của thẻ h
    *** mặc định trong HTML khi thẻ con có kích thước chòi ra khỏi thẻ cha thì nó vẫn nhìn thấy được ==> xử dụng overflow để giải quyết
  - 104. Sản phẩm CSS - Phần 2
    - 1 số trường hợp !important mạnh mẽ quá nên tránh => có thể dùng selector.class để thay thế (nếu bị thu viện xóa thuộc tính)
  - 105. Sản phẩm CSS - Phần 3
    - chú ý thuộc tính margin: auto
    - mặc định thẻ span không được apply thuộc tính CSS vào
    *** cần đặt độ cao cho các dòng chữ (line-height) trên website của ta, thường designer sẽ quy định nó ==> ta chỉ cần set nó vào thẻ HTML
    *** sans-serif là chủng chữ không chân (không phải font) => nếu Roboto chưa hoặc không tải được => sẽ dùng sans-serif
    *** box-sizing: inherit; ==> kế thừa lại những thẻ chứa nó có thuộc tính box-sizing ==> tại sao trong project lại ser box-sizing như vậy?
    *** chú ý lớp grid trong file base.CSS
