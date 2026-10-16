---


---

<h1 id="hướng-dẫn-cài-đặt-cảm-biến-độ-ẩm-cho-trang-trại-lan">Hướng dẫn cài đặt cảm biến độ ẩm cho trang trại Lan</h1>
<h2 id="mục-đích">1. Mục đích</h2>
<p>Tài liệu hướng dẫn lắp đặt cảm biến độ ẩm đất, kiểm tra dữ liệu và điều khiển máy bơm nước tự động bằng Python.</p>
<h2 id="chuẩn-bị-thiết-bị">2. Chuẩn bị thiết bị</h2>
<ul>
<li>
<p>Cảm biến độ ẩm đất (loại cũ hoặc mới).</p>
</li>
<li>
<p>Raspberry Pi hoặc thiết bị điều khiển tương thích.</p>
</li>
<li>
<p>Máy bơm nước, mạch điều khiển, dây nối và nguồn điện.</p>
</li>
</ul>
<h2 id="cài-đặt-môi-trường">3. Cài đặt môi trường</h2>
<p>Mở Terminal và chạy lệnh:</p>
<p>Bash</p>
<pre><code>python --version
python -m pip install gpiozero

</code></pre>
<h2 id="bảng-so-sánh-cảm-biến">4. Bảng so sánh cảm biến</h2>
<p><strong>Tiêu chí</strong></p>
<p><strong>Cảm biến loại cũ</strong></p>
<p><strong>Cảm biến loại mới</strong></p>
<p><strong>Nguyên lý</strong></p>
<p>Điện trở thay đổi theo độ ẩm</p>
<p>Đo điện dung của đất</p>
<p><strong>Chống ăn mòn</strong></p>
<p>Thấp hơn</p>
<p>Tốt hơn</p>
<p><strong>Độ bền</strong></p>
<p>Dễ ảnh hưởng bởi môi trường đất</p>
<p>Tuổi thọ cao hơn</p>
<p><strong>Giá thành</strong></p>
<p>Rẻ</p>
<p>Cao hơn</p>
<h2 id="code-python-điều-khiển-máy-bơm">5. Code Python điều khiển máy bơm</h2>
<p>Python</p>
<pre><code>from gpiozero import OutputDevice
from time import sleep

PUMP_PIN = 17
MOISTURE_THRESHOLD = 30
pump = OutputDevice(PUMP_PIN, active_high=True, initial_value=False)

def read_soil_moisture():
    soil_moisture = 25
    return soil_moisture

try:
    while True:
        soil_moisture = read_soil_moisture()
        print(f"Do am dat: {soil_moisture}%")

        if soil_moisture &lt; MOISTURE_THRESHOLD:
            pump.on()
            print("Dat kho - Bat may bom")
        else:
            pump.off()
            print("Do am du - Tat may bom")

        sleep(5)
except KeyboardInterrupt:
    print("Da dung chuong trinh")
finally:
    pump.off()
    pump.close()

</code></pre>
<p><em>Lưu ý: Không nối máy bơm công suất lớn trực tiếp vào chân GPIO.</em></p>
<h2 id="task-list-kiểm-tra-thiết-bị">6. Task List kiểm tra thiết bị</h2>
<ul>
<li class="task-list-item">
<p><input type="checkbox" class="task-list-item-checkbox" disabled=""> Kiểm tra kết nối chân và nguồn điện cảm biến.</p>
</li>
<li class="task-list-item">
<p><input type="checkbox" class="task-list-item-checkbox" disabled=""> Kiểm tra mạch điều khiển máy bơm.</p>
</li>
<li class="task-list-item">
<p><input type="checkbox" class="task-list-item-checkbox" disabled=""> Cài đặt Python và thư viện <code>gpiozero</code>.</p>
</li>
<li class="task-list-item">
<p><input type="checkbox" class="task-list-item-checkbox" disabled=""> Kiểm tra giá trị độ ẩm đọc được.</p>
</li>
<li class="task-list-item">
<p><input type="checkbox" class="task-list-item-checkbox" disabled=""> Thử nghiệm bật/tắt máy bơm an toàn khi đất khô và đủ ẩm.</p>
</li>
<li class="task-list-item">
<p><input type="checkbox" class="task-list-item-checkbox" disabled=""> Lưu code và tài liệu lên GitHub.</p>
</li>
</ul>
<h2 id="ký-tự-escape-trong-markdown">7. Ký tự Escape trong Markdown</h2>
<p>Sử dụng dấu gạch chéo ngược <code>\</code> để hiển thị ký tự đặc biệt (ví dụ: <code>\*</code> thay vì in nghiêng, <code>\#</code> thay vì tạo tiêu đề).</p>
<h2 id="kết-luận">8. Kết luận</h2>
<p>Markdown giúp tài liệu kỹ thuật dễ quản lý và trực quan thông qua Inline Code, Code Block, Table và Task List.</p>

