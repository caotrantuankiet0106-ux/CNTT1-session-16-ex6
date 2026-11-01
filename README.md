# BẢN ĐẶC TẢ & QUY TRÌNH KHÔI PHỤC DỰ ÁN GREEN-TECH

## 1. Bản đặc tả không gian cộng tác (README.md)
* **Cấu trúc Thư mục & Hybrid Workflow:**
  * Thư mục `src/` (mã nguồn cảm biến) và `docs/` (báo cáo). Code được viết cục bộ trên máy Dev, đồng bộ định kỳ lên Cloud Workspace để bảo mật.
  * File `.env` chứa mật khẩu cảm biến được đưa vào `.gitignore`, chỉ Leader/Dev cốt lõi có quyền đọc để tránh rò rỉ.
* **Cấu trúc Channel:**
  * `#dev-sensors`: Trao đổi kỹ thuật, fix lỗi cảm biến.
  * `#investor-reports`: Cung cấp báo cáo cho nhà đầu tư.
  * `#hardware-partners`: Thảo luận cùng đối tác cung cấp thiết bị.
* **Quy định Phân quyền:**
  * Nhà đầu tư: **Viewer (Chỉ xem)** báo cáo.
  * Đối tác thiết bị: **Commenter (Bình luận góp ý)** tại thư mục/kênh liên quan.
  * Đội Dev: **Editor (Toàn quyền chỉnh sửa)** code.

## 2. Quy trình khôi phục khi xóa nhầm Folder Sensors
1. **Khôi phục nhanh trên Cloud:** Truy cập **Trash / Recycle Bin** của Workspace $\rightarrow$ Tìm `folder sensors` $\rightarrow$ Chọn **Restore**.
2. **Khôi phục qua Git (nếu xóa vĩnh viễn trên Cloud):**
   ```bash
   git checkout HEAD -- sensors/
   git push origin main