Mục tiêu:
Thiết kế bàn phím gaming 6 phím tự thiết kế để bluetooth/sạc typc-C.

Thông tin:
nguyên liệu: (bền, nhẹ)
màu: đen
khối lượng: 
kích thước:
Bàn phím: hỗ trợ hotswap / dùng mechanical switch
Vi điều khiển: nRF52840
Firmware: ZMK
Pin: Li-Po 1000 mAh
Switch: Hotswap Kailh

Số phím: 6
=>Thông tin về nRF52840:
CPU:	ARM Cortex-M4F
Clock:	64 MHz
Bluetooth:	BLE 5.0 / 5.1
USB	✔️ (52840)
HID latency	⭐⭐⭐⭐⭐
QMK / ZMK mạnh

🔹 Bluetooth
🔹 Pin 1000 mAh
🔹 Type-C sạc
🔹 Công tắc bật/tắt Bluetooth (nguồn)
🔹 Hotswap
🔹 Không nói chung chung – có tên linh kiện cụ thể

🧠 Kiến trúc tổng thể (để bạn hiểu BOM)
USB Type-C
   │
IC sạc pin ─── Li-Po 1000mAh
   │
LDO / Buck 3.3V
   │
nRF52840  ← BLE + USB
   │
Matrix 6 phím (Hotswap + Diode)

✅ 1️⃣ Vi điều khiển (MCU – QUAN TRỌNG NHẤT)
🔹 nRF52840 (chọn 1 trong 2)
🔸 Cách A (dễ nhất – khuyên dùng)

Module nRF52840

Ví dụ:

E73-2G4M08S1C

Raytac MDBT50Q

Ưu điểm:

Có sẵn antenna

Dễ layout

BLE ổn định

📦 Mua: 1 cái

✅ 2️⃣ USB Type-C (sạc + USB HID)
🔹 Cổng USB

USB Type-C 16 pin (USB 2.0 only)

📦 1 cái

🔹 Điện trở CC

5.1kΩ 1% × 2

CC1 → GND

CC2 → GND

🔹 Tụ lọc VBUS

100nF (0.1µF) ×1

10µF ×1

✅ 3️⃣ IC sạc pin Li-Po (CỰC QUAN TRỌNG)
🔹 Khuyên dùng
TP4056 (Type-C version)

HOẶC

MCP73831

📦 1 IC

🔹 Linh kiện đi kèm (TP4056)

Rprog 1.2kΩ → ~1A sạc

10µF ×2 (IN, BAT)

LED báo sạc ×2 (đỏ / xanh)

Điện trở LED 1kΩ ×2

✅ 4️⃣ Pin

Pin Li-Po 3.7V – 1000 mAh

Có mạch bảo vệ (PCM) → KHUYÊN DÙNG

📦 1 viên

✅ 5️⃣ Công tắc bật / tắt Bluetooth (NGUỒN)
🔹 Công tắc trượt (slide switch)

SPDT / SPST SMD

Dòng ≥ 1A

📦 1 cái

👉 Đặt giữa pin và LDO để ngắt nguồn hoàn toàn

✅ 6️⃣ Ổn áp 3.3V cho nRF52840
🔹 LDO (ít nhiễu, đủ dùng)

ME6211C33

MCP1700-3302

XC6206P332

📦 1 IC

🔹 Tụ LDO

1µF ×2

100nF ×1

✅ 7️⃣ Ma trận phím (6 phím)
🔹 Socket hotswap

Kailh Hotswap Socket (PG1350 / MX) ×6

🔹 Switch

Cherry MX / Kailh / Gateron ×6

🔹 Diode chống ghost

1N4148 SMD (SOD-123) ×6

✅ 8️⃣ Nút phụ
🔹 Reset

Tact switch SMD ×1

🔹 Nút BOOT (nếu cần DFU)

Tact switch SMD ×1

✅ 9️⃣ Tụ decoupling (BẮT BUỘC)

100nF (0.1µF) × 6–10

4.7µF – 10µF ×2

👉 Đặt sát chân VDD nRF52840

✅ 🔟 Header nạp & debug (khuyên có)

SWD header 4 pin

SWDIO

SWCLK

3.3V

GND

📦 1 bộ

✅ 1️⃣1️⃣ LED (TÙY CHỌN)
🔹 LED trạng thái

LED SMD 0603 ×1–2

R 1kΩ ×1–2

⚠️ Không khuyên RGB cho pin nhỏ (nhưng vẫn được)

🧾 TỔNG HỢP BOM (CHECKLIST)
IC / Module

☐ nRF52840 module ×1

☐ TP4056 / MCP73831 ×1

☐ LDO 3.3V ×1

Nguồn

☐ Pin Li-Po 1000mAh ×1

☐ USB Type-C ×1

☐ Slide switch ×1

Phím

☐ Kailh hotswap ×6

☐ Switch ×6

☐ Diode 1N4148 ×6

Thụ động

☐ 5.1kΩ ×2

☐ 1kΩ ×4

☐ 1.2kΩ ×1

☐ 100nF ×10

☐ 1µF ×4

☐ 10µF ×4

Khác

☐ Reset switch ×1

☐ Boot switch ×1

☐ SWD header ×1

🎯 Kết luận

👉 Cấu hình này là CHUẨN cho macro pad / mini keyboard BLE gaming
👉 Pin 1000 mAh → 8–20 giờ dùng thoải mái
👉 nRF52840 + ZMK → độ trễ thấp nhất

Nếu bạn muốn, bước tiếp theo mình có thể:

Vẽ sơ đồ nguyên lý hoàn chỉnh

Gợi ý module nRF52840 dễ mua tại VN

Tối ưu pin để đạt 15–20h

Chuẩn bị BOM dạng Excel để đi mua

Thành phần	Vị trí
Switch	Mặt trước
Hotswap socket	Mặt sau (dưới switch)
nRF52	Mặt sau – sát cạnh
Anten BLE	Mép PCB
Pin 1000 mAh	Mặt sau – xa anten
Type-C	Cạnh dưới
Công tắc ON/OFF	Cạnh bên
SWD pad	Mặt sau
🔥 Tóm lại (câu trả lời ngắn gọn)

Với bàn phím 6 phím BLE + pin + Type-C,
vi điều khiển nRF52 phải đặt ở MẶT SAU PCB, sát cạnh PCB để anten hướng ra ngoài,
không đặt dưới switch, không đặt sát pin, không đặt gần USB.