<div>
    <h1>
        <a align="left"><img src="https://i.ibb.co/SQWy8xC/logo-big.png" alt="DONGNAITRRAVEL-Logo" style="width: 80px; float: left; margin-right: 1rem" border="0"></a>
        DONG NAI TRAVEL PROJECT
        <br>
        Cẩm nang du lịch cho mọi người
    </h1>
</div>

## Giới thiệu tổng quan
DONG NAI TRAVEL là ứng dụng được xây dựng cho mục đích tham gia **cuộc thi Sáng tạo Khoa học Kĩ thuật** tỉnh Đồng Nai - 2023 và là đồ án tốt nghiệp 2024.

Giải pháp đạt được giải **Khuyến khích** chung cuộc. Xem thêm thông tin [tại đây](https://drive.google.com/file/d/1rtrAE14D4_O47xg_cKyicr1dSMoTsqJe/view?usp=sharing).

### Mục tiêu dự án
Hỗ trợ khám phá các địa điểm du lịch ở Đồng Nai, đồng thời người dùng có thể chia sẻ được các trải nghiệm thông qua bài viết và quản lý hồ sơ cá nhân. Người dùng còn có thể dùng Travel Bot để tham khảo lộ trình, kế hoạch đi du lịch; xem thông tin về thời tiết; xem lộ trình đường đi với Map tích hợp.

### Demo
Xem video demo dự án [tại đây](https://www.youtube.com/watch?v=6lMZkIQiZ68)

### Đội ngũ phát triển

**Thời gian phát triển**: từ tháng 02 - tới tháng 07 năm 2023.

**Thành viên tham gia**:
- Thái Anh Đức, [xem thêm](https://github.com/ThaiAnhDuc02)
- Lương Văn Pháp, [xem thêm](https://github.com/phapdev)
- Từ Nhật Phương, [xem thêm](https://github.com/FromSunNews)
- Nguyễn Anh Tuấn, [xem thêm](https://github.com/NguyenAnhTuan1912)
- Lê Nhật Tùng (giảng viên hướng dẫn)

### Công nghệ sử dụng
- **Frontend (Mobile)**: `React-Native`, `Expo`, `React-Navigation`
- **Frontend (Admin)**: `React`, `Tailwind CSS`
- **Backend**: `NodeJS`, `Express`
- **Database**: `MongoDB`
- **Services**: `GoogleAPI`, `Cloudinary`, `GPT`
- **DevOps**: `Docker`, `Podman`
- **Cloud**: `AWS`.

## Cấu trúc dự án
Dự án DONG NAI TRAVEL bao gồm 3 thành phần chính:

### 1. dongnai-travel (Mobile App)
Ứng dụng di động cho người dùng cuối, phát triển bằng React Native. Người dùng có thể khám phá các địa điểm du lịch, xem thông tin, chia sẻ trải nghiệm và sử dụng các tính năng đặc biệt như Travel Bot và bản đồ tích hợp.

```
├───animations
├───app
│   └───(app)
│       ├───(main)
│       │   ├───blogs
│       │   │   └───[id]
│       │   ├───explore
│       │   │   └───places
│       │   │       └───[id]
│       │   ├───home
│       │   ├───map
│       │   └───settings
│       │       └───profile
│       │           └───[id]
│       └───(sub)
│           └───chatbot
├───assets
│   ├───fonts
│   ├───images
│   │   ├───background_weather
│   │   ├───map_type
│   │   ├───step
│   │   ├───weather
│   │   └───weather_forcast
│   ├───json
│   └───mock-data
│       ├───blog
│       └───place
├───classes
├───components
│   ├───app-flat-list
│   ├───app_chart
│   │   └───app_bar_chart
│   ├───app_header
│   ├───app_list
│   ├───app_tab_slider
│   ├───app_text
│   ├───blog-comment
│   ├───blog_comment
│   ├───bottom_sheet
│   ├───bottom_tab_bar
│   ├───buttons
│   ├───...
│   ├───vertical_place_card
│   └───__tests__
│       └───__snapshots__
├───constants
├───hocs
│   ├───create-result-list
│   ├───with-blog-actions
│   └───with-place-actions
├───hooks
├───libs
│   ├───mark-format
│   │   ├───react-native
│   │   │   ├───config
│   │   │   └───render
│   │   └───src
│   │       ├───assets
│   │       ├───configs
│   │       ├───creator
│   │       ├───types
│   │       └───utils
│   ├───react-native-maps-line-arrow
│   └───react-native-weather-chart
│       └───src
│           ├───iconset
│           └───WeatherChart
├───objects
│   ├───banner
│   ├───blog
│   ├───chatbot
│   ├───map
│   ├───others
│   ├───place
│   ├───report
│   ├───text
│   ├───user
│   └───weather
├───screens
│   ├───blog-comments
│   ├───blog-detail
│   │   └───components
│   ├───...
│   ├───signin
│   ├───signup
│   └───weather
├───scripts
├───src
│   ├───apis
│   └───redux
│       ├───manifold
│       └───user
├───states
│   └───redux
│       ├───blogs
│       ├───language
│       ├───manifold
│       ├───map
│       ├───places
│       ├───profile
│       ├───reports
│       ├───settings
│       ├───theme
│       └───user
├───store
│   └───slices
├───styles
├───types
└───utils
```

### 2. dongnai-travel-admin (Admin Dashboard)
Giao diện quản trị cho các quản trị viên để quản lý nội dung của ứng dụng, bao gồm địa điểm, bài viết, người dùng, báo cáo và banner quảng cáo.

```
├───public
│   └───images
└───src
    ├───api
    ├───assets
    ├───components
    │   ├───markdown
    │   ├───table
    │   └───ui
    ├───hooks
    ├───layouts
    ├───lib
    ├───mock-data
    ├───objects
    │   ├───assignment
    │   ├───auth
    │   ├───banner
    │   ├───blog
    │   ├───place
    │   ├───report
    │   └───user
    ├───pages
    │   ├───auth
    │   │   └───components
    │   ├───banners
    │   │   └───components
    │   ├───blogs
    │   │   └───components
    │   ├───home
    │   ├───places
    │   │   └───components
    │   ├───reports
    │   │   └───components
    │   └───users
    │       └───components
    ├───routes
    ├───states
    │   └───dialogs
    ├───types
    └───utils
        ├───boolean
        ├───browser_storage
        ├───constant
        ├───cookies
        ├───datetime
        ├───element
        ├───number
        ├───object
        ├───other
        └───string
```

### 3. dongnai-travel-api (Backend)
API backend cung cấp dữ liệu và dịch vụ cho cả ứng dụng di động và trang quản trị. Xây dựng trên nền tảng NodeJS với Express và MongoDB.

```
├───database
│   └───scripts
├───server
│   ├───secrets
│   └───src
│       ├───classes
│       ├───databases
│       │   ├───dongnaitravel
│       │   │   ├───banner
│       │   │   ├───blog
│       │   │   ├───blog-comment
│       │   │   ├───blog-type
│       │   │   ├───business-status
│       │   │   ├───follow
│       │   │   ├───otp
│       │   │   ├───place
│       │   │   ├───place-review
│       │   │   ├───place-type
│       │   │   ├───report
│       │   │   ├───report-reason
│       │   │   ├───report-status
│       │   │   ├───user
│       │   │   ├───user-favorited-blog
│       │   │   ├───user-favorited-place
│       │   │   ├───user-role
│       │   │   └───user-visited-place
│       │   └───helper
│       ├───endpoints
│       │   ├───auth
│       │   ├───banner
│       │   ├───banners
│       │   ├───blog
│       │   ├───blogs
│       │   ├───chatbot
│       │   ├───place
│       │   ├───places
│       │   ├───reports
│       │   ├───user
│       │   ├───users
│       │   └───weather
│       ├───helpers
│       │   ├───auth
│       │   │   └───endpoints
│       │   ├───banners
│       │   │   └───endpoints
│       │   ├───blogs
│       │   │   ├───endpoints
│       │   │   └───middlewares
│       │   ├───other
│       │   ├───places
│       │   │   └───endpoints
│       │   ├───regex
│       │   ├───reports
│       │   │   └───endpoints
│       │   ├───users
│       │   │   └───endpoints
│       │   └───weather
│       │       └───endpoints
│       ├───services
│       │   ├───auth
│       │   ├───aws
│       │   │   └───s3
│       │   ├───chat-bot
│       │   ├───chat-gpt
│       │   ├───direction
│       │   ├───email
│       │   ├───google-map
│       │   ├───google-route
│       │   ├───redis
│       │   ├───text-to-speech
│       │   ├───upload-file
│       │   ├───validators
│       │   └───weather
│       ├───types
│       │   └───express
│       └───utils
├───_docker-compose-env
├───_scripts
├───_setup
└───_templates
```

# Các chức năng chính
- **Khám phá địa điểm**: Xem các thông tin mới nhất về địa điểm, bài viết, sự kiện. Người dùng có thể lưu thông tin địa điểm, bài viết.
- **Điều hướng và lộ trình**: Tìm lộ trình đi tới điểm đến, xem các thông tin chi tiết về địa điểm.
- **Đa phương tiện**: Đọc, nghe thông tin về địa điểm, bài viết.
- **Travel Bot**: Sử dụng AI để tham khảo, tạo lộ trình, kế hoạch đi du lịch.
- **Quản lý nội dung**: Quản trị viên có thể quản lý các địa điểm, bài viết, người dùng và báo cáo.

# Hướng dẫn cài đặt và triển khai

### 1. Thiết lập Backend (dongnai-travel-api)

Phần hướng dẫn này tập trung vào môi trường phát triển. Trong môi trường phát triển, Server và Database sẽ là các containers trong một network.

#### Yêu cầu cài đặt trước
- Docker/Docker Desktop hoặc Podman
- Node.js và npm/yarn

#### Các file cấu hình quan trọng
- `database/scripts/init.js`: Dùng để khởi tạo dữ liệu mặc định cho MongoDB.
- `server/secrets`: Thư mục chứa thông tin bảo mật (cần liên hệ nhóm tác giả để được cung cấp).
- `server/src/db.config.json`: Chứa cấu hình kết nối với cơ sở dữ liệu.

#### Các bước cài đặt
1. **Với Docker trong Linux**:
   - CD vào thư mục gốc của dự án
   - Chạy lệnh: `docker compose -f docker-compose.dev.yml up -d`

2. **Với Docker Desktop trong Linux hoặc Windows**:
   - Khởi động Docker Desktop
   - CD vào thư mục gốc của dự án
   - Chạy lệnh: `docker compose -f docker-compose.dev.yml up -d`

3. **Với Podman trong Linux hoặc WSL của Windows**:
   - CD vào thư mục gốc của dự án
   - Chạy lệnh: `podman compose -f docker-compose.dev.yml up -d`

4. **Với Podman trong Windows**:
   - CD vào thư mục gốc của dự án
   - Chạy lệnh: `podman compose -f docker-compose.dev.yml up -d`
   - Chạy lệnh `podman ps -a` để xem tất cả các containers
   - Start các containers theo thứ tự:
     - Database: `podman start <container-name>` (thường là **dongnai-travel-api_database_1**)
     - Server: `podman start -ia <container-name>` (thường là **dongnai-travel-api_server_1**)

> **Lưu ý**: Để sử dụng podman compose, cần cài đặt `podman-compose` qua pip với lệnh `pip install podman-compose`.

#### Port Forwarding (WSL)
Nếu ứng dụng không thể truy cập từ các thiết bị khác trong mạng, bạn cần thiết lập Port Forwarding:

```bash
wsl hostname -I
netsh interface portproxy set v4tov4 listenport=3000 listenaddress=0.0.0.0 connectport=3000 connectaddress=<WSL_IP_ADDRESS>
```

### 2. Thiết lập Mobile App (dongnai-travel)

1. CD vào thư mục `dongnai-travel`
2. Cài đặt các dependencies:
   ```
   npm install
   # hoặc
   yarn install
   ```
3. Thiết lập `.env`, đầu tiên là tạo file `.env` trước, sau đó lấy địa chỉ IP của máy
   ```
   # Lấy địa chỉ IP của máy
   ipconfig
   ```
   Vào trong **dongnai-travel**, lấy các biến mẫu trong `.env.example` bỏ vào trong `.env` và đổi giá trị của biến `EXPO_PUBLIC_DONGNAITRAVEL_API_URL` thành địa chỉ IP mới tìm thấy
   ```
   EXPO_PUBLIC_DONGNAITRAVEL_API_URL="ĐỊA CHỈ IP Ở ĐÂY"
   EXPO_PUBLIC_BUTTON_DEBOUNCE_TIME=500
   ```
3. Chạy ứng dụng:
   ```
   npm start
   ```

### 3. Thiết lập Admin Dashboard (dongnai-travel-admin)

1. CD vào thư mục `dongnai-travel-admin`
2. Cài đặt các dependencies:
   ```
   npm install
   # hoặc
   yarn install
   ```
3. Chạy ứng dụng:
   ```
   npm run dev
   # hoặc
   yarn run dev
   ```

## Tài liệu liên quan

- [Tài liệu chính](https://docs.google.com/document/d/1KdUV5ahihEOVYrn73MnY4GPgdbXIl4ou/edit?usp=sharing&ouid=102396661633118680496&rtpof=true&sd=true)
- [Các issues của dự án](https://github.com/FromSunNews/DongNaiTravelApp/issues)
- [Infographic](https://www.behance.net/gallery/177198847/DongNaiTravel-App)

## Tài liệu kỹ thuật tham khảo

- [Cloudinary Document for NodeJS (2023)](https://cloudinary.com/documentation/node_integration)
- [Expo Document (2023)](https://docs.expo.dev)
- [Google API Document (2023)](https://developers.google.com/workspace/products)
- [React Document (2023)](https://react.dev/)
- [React-Native Document (2023)](https://reactnative.dev)
- [React-Navigation Document (2023)](https://reactnavigation.org)
- [MongoDB Documentation](https://www.mongodb.com/docs/)
- [Express.js Documentation](https://expressjs.com/)
- [Docker Documentation](https://docs.docker.com/)
