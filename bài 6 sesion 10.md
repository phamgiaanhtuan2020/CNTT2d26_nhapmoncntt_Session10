---


---

<p><strong>PHẦN 1: PHÂN TÍCH SAI LẦM CỦA NAM VÀ ƯU ĐIỂM MARKDOWN</strong></p>
<ul>
<li>
<p><strong>Hai sai lầm của Nam:</strong></p>
<ol>
<li>
<p><strong>Độ bền dữ liệu kém:</strong> File Rich Text (.docx/.rtf) chứa cấu trúc XML ẩn phức tạp. Nếu mất dù chỉ 1 byte do lỗi mạng, toàn bộ cấu trúc file sẽ hỏng và không thể mở được.</p>
</li>
<li>
<p><strong>Quản lý mã nguồn kém:</strong> File Rich Text nặng, chứa nhiều mã định dạng giao diện rườm rà, không hỗ trợ theo dõi lịch sử thay đổi (diff/merge) trên Git.</p>
</li>
</ol>
</li>
<li>
<p><strong>Tại sao Markdown an toàn và nhẹ hơn:</strong></p>
<ul>
<li>
<p>Markdown là định dạng văn bản thô (plain text). Nếu mất 1 byte dữ liệu, hệ thống chỉ mất đúng ký tự tại vị trí đó, các phần còn lại vẫn đọc và chỉnh sửa bình thường.</p>
</li>
<li>
<p>Dung lượng rất nhẹ, truyền tải nhanh và tương thích hoàn toàn với các công cụ quản lý mã nguồn.</p>
</li>
</ul>
</li>
</ul>
<p><strong>PHẦN 2: CHUYỂN ĐỔI SANG MARKDOWN (.MD)</strong></p>
<h1 id="giới-thiệu-hệ-thống-smart-farm-iot">GIỚI THIỆU HỆ THỐNG SMART-FARM IOT</h1>
<p>Hệ thống tự động hóa chăm sóc vườn lan dựa trên công nghệ IoT.</p>
<h2 id="mục-tiêu-cốt-lõi">Mục tiêu cốt lõi</h2>
<ul>
<li>Thu thập dữ liệu môi trường thời gian thực (nhiệt độ, độ ẩm đất, ánh sáng).</li>
<li>Xử lý logic tại SoC để điều khiển máy bơm tưới tự động.</li>
<li>Tối ưu hóa lượng nước và giảm thiểu thao tác thủ công.</li>
</ul>

