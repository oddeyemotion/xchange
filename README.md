# Xchange PWA

## Technical questions
1. Để hiển thị gợi ý tìm kiếm có khó k?
2. Để hiển thị bộ lọc có khó k?
3. Có những chỗ đang "?? characters" thì nên làm ntn?

## Problems
1. Nếu list của bên A có nhiều hơn 1 sp phù hợp để exchange, thì nếu cho chọn nhiều sp thì sẽ hơi khó develop -> chỉ cho chọn 1 sp, bên A có thể message cho bên B để mời bên B vô profile xem thêm.
2. View 2.3 cần lấy API map để user pick location

## List views
### 0 - Splash screen
[](https://github.com/oddeyemotion/xchange/blob/55a601004bb03b9055c40887f677c74356df8ede/XCHANGE-(2)/XCHANGE%20(2)-01.png)
A static png image of the logo.
### 1 - Login
Have the user enter their email/username and password. (Int he prototype, we only let user use the username).
### 2 - Sign up
#### 2.1 - Enter email
Enter email
#### 2.2 - Enter your name
Enter the user's real name
#### 2.3 - Your location (!!!)
Have the user pick their approximate location on the map (get city, district and ward)
#### 2.4 - Phone number
Enter phone number
#### 2.5 - Pick username
Enter the user's username. This along with the password will be used to save the user's credentials. (login)
#### 2.6 - Choose password
Choose password & retype password to confirm
#### 2.7 - Pick 3 tags (!!!)
Have the user pick at least 3 product tags for the Home view to work (but for the sake of prototyping, we will let user pick one or two since we only have two tags)
#### 2.8 - All set!
Reuse Splash screen

### 3 - Home
#### 3.1 - Main home
Components: 
1. A search box (let user go to view 3.2)
2. A notification bell icon (let user go to Notification view, which we don't plan to develop)
3. A "New offer" button (let user go to view 3.4)
4. A gallery of items displayed based on the tags the user have chosen when they register their account (or after modifying in Profile view).
#### 3.2 - Search
When user type a keyword in the search box, a list of old searches [and suggestions] appears. (We will consider not developing the suggestions feature if there is not enough time.)
#### 3.3 - Search results
Resuing components from view 3.1. But the results are displayed in this priority:
1. Exact/near exact keyword
2. Nearest location
There is a button for filters, but we do not plan to develop it right now.
#### 3.4 - New offer
User can create new offers in this view.
1. Adding photos and videos (for prototyping, we let user upload maximum of 3)
2. Product name (required, maximum ?? characters)
3. Product type (required, drop-down list, user can choose more than one tag)
4. Product description (optional)
5. Wants to trade with (required, drop-down list, user can choose more than one tag)
6. Description of the product user wants to trade with (optional)
And then click on the "Post" button to upload.
#### 3.5 - Product detail
Components from top to bottom:
1. A caroussel of photos and videos
2. Product tags
3. Product name
4. Username of the owner and their approx. location and their approx. distance.
5. 2 columns: Condition of the product & Exchange with
6. Description (if available) of the shown product.
At the bottom, there are 3 buttons: 
1. Save (let user save this product detail for later. We do not plan to develop this feature right now.)
2. Message (send a message to the owner. We do not plan to develop this feature right now.)
3. Exchange (let user go to view 3.6)
#### 3.6 - Choose product to offer
Components:
1. A list of available items the this user can exchange with the owner (Theoretically, this list should be displayed based on their tags, which means the items with non-relevant tags will not be shown. But for prototyping, we decided not to implement this feature yet.) When the user click on an item, it changes color.
2. A box to send messages to the owner (optional)
When the user has done picking their items and click on the "Confirm" button, the owner should receive a notification.

### Other views besides Home
Only develop static front-end, no feature.
1. Profile
2. Chat
3. Settings

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
