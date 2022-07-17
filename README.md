I. Setup project
1) Cài đặt xampp và composer để cài đặt laravel 9
2) composer create-project laravel/laravel (name-project)
- Lưu ý nên lưu ở folder xampp/htdocs
- Khởi chạy xampp
- Vào localhost/phpmyadmin -> Tạo database 
3) Khởi chạy laravel
- cd (name-project) -> php artisan serve
- php artisan migrate(kết nối với database)
* Vào folder .env đổi: DB_CONNECTION=sqlite sau đó comment các giá trị DB phía dưới
* Tạo file mới ở folder: name-project/database -> database.sqlite(file trống) -> php artisan migrate -> kiểm tra xem file database.sqlite đã có chứa dữ liệu chưa, nếu rồi thì là kết quả đúng
* Quay lại file .env =>
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel9vue3_table(name-database-project)
DB_USERNAME=root
DB_PASSWORD=
* Tiếp tục setup tại file .editorconfig
4) Khởi chạy vue
- cd name-project
- npm install vite vue
* framework: vue -> variant: vue -> cd vue: npm i + npm run dev(khởi chạy frontend)
* lưu ý ở phần app.vue -> <script setup> là chế độ mặc định lưu lại các import components
- dừng khởi động máy chủ frontend -> npm install -S vuex@next
- New folder: store -> /store/index.js
- update ReadME.md
5) Setup cài đặt css
- cd/name-project/vue -> npm install -D tailwindcss postcss autoprefixer -> npx tailwindcss init -p
- setup tại trang vue/vite 
- npm install @headlessui/vue @heroicons/vue @tailwindcss/forms(lưu ý file tailwind.config.cjs)
6) Setup vue-router
- cd/name-project/vue -> npm install -S vue-router@next