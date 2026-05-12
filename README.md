# bi-public
> Cấu trúc và tư duy hệ thống của ứng dụng ôn luyện từ vựng
#
## 2 hoạt động chính trên site
1. Nhập từ mới
2. Ôn luyện từ đã học
#
### 2.1 - Nhập từ mới
Gõ từ cần thêm vào ô tìm kiếm. Nếu từ chưa tồn tại trong từ điển cá nhân, sẽ có nút "Thêm mới" để click vào.  
API sẽ tự động tạo các trường: IPA, loại từ (danh từ, tính từ, động từ...), nghĩa tiếng Việt.  
Người dùng có thể sửa bất kỳ trường nào cho vừa ý.  
Nếu từ đã tồn tại, click vào sẽ tới trang edit từ như trên.
#
### 2.2 - Ôn luyện
Có 2 loại từ cần ôn chính:  
1. Ôn từ vừa mới học (vừa nhập)
2. Ôn từ đã học
#
#### 2.2.1 - Ôn từ vừa học
Làm đúng 5 lần thì từ đó sẽ được chuyển sang phần ôn luyện.  
Sử dụng nút bấm "Gợi ý" hay "Ví dụ", để sử dụng API hiển thị các câu ví dụ liên quan, chứa từ cần học
#### 2.2.2 - Ôn từ cũ
Danh sách hiển thị, là sự pha trộn random các loại sau:  
1. Từ mới học, ôn ít
2. Từ sai: Sai nhiều, vừa sai.

Ở phần ôn luyện, kết quả khi ôn luyện 1 từ sẽ được lưu vào database, làm cơ sở để hiển thị danh sách cần ôn sau này: ('write_prac' ++ )
1. Nhập sai > 'learn_more' = 1 && 'write_false' ++ ('learn_more' để xác định từ vừa học bị sai; 'write_false' để sau này tính tỉ lệ sai / số lần học ('write_prac').
2. Nhập đúng > 'learn_more' = 0

---
# 📋 Changelog
## 2026/5/11 Cách set danh sách ôn luyện
1. (All)learn_more = 1 - Làm sai (ở lần trước)
2. (30)write_prac ASC - Luyện ít nhất
3. (40)write_rate DESC - Sai nhiều nhất  
## 2025/12/25 Cách set danh sách ôn luyện
1. (30)created_at DESC - Mới học
2. (30)created_at ASC - Cũ nhất
3. (40)write_rate DESC - Sai nhiều nhất
