# Xchange PWA

## PWA?
PWA mang lại trải nghiệm giống Native app nhưng bản chất là Web app. Tốc độ load nhanh hơn, có thể dùng khi không có Internet, dung lượng nhẹ hơn và cài đặt tiện hơn so với Native app.

Lựa chọn giải pháp PWA vì nó phù hợp với năng lực của đội: hầu hết chỉ cần tập trung vào front-end, back-end có thể setup rất đơn giản.

## Đặt vấn đề
1. Bình thường khi nói đến web app, chúng ta sẽ làm việc với JavaScript, càng nhiều JavaScript thì load càng lâu. Vì vậy chúng ta sẽ tối ưu phần JavaScript là chính.
2. Ngoài ra, chúng ta cũng muốn thể hiện được một ưu điểm của Native app - người dùng không phải tải đi tải lại các file liên quan (assets) mỗi lần khởi động chương trình.

## Front-end
### npm 
Node's package manager

### Yarn
Để khắc phục các nhược điểm của npm như: load lâu, không dùng được offline, dễ xảy ra conflict... thì dùng Yarn hỗ trợ.

### React
React là một thư viện phổ biến, với đặc điểm nổi trội nhất là có thể chia nhỏ mã nguồn giao diện người dùng thành nhiều module (component) nhỏ hơn.

### ReactDOM (render)
Vì React chỉ tạo ra UI chứ không render được UI :)))) nên sử dụng ReactDOM kèm để render được code React.

### Webpack
Tool giúp đóng gói code JavaScript

### Webpack dev server
Package giúp tự động rerun command Webpack sau mỗi thay đổi (không phải build lại từ đầu sau mỗi lần)

### Babel
Tool dịch chuẩn Javascript mới (ES6) sang Javascript cũ (ES5) để tương thích được với các browser cũ hơn

## Back-end
### Firebase
Chọn Firebase là vì nó vừa có database, vừa có hosting free, vừa có built-in authentication.
