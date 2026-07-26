# GSP NEXT30 – GS1 Smart Factory

Gói phát hành độc lập cho **GS1 – Nhà máy Goldsun Hà Nội**. Dashboard dùng
chung lõi tính toán với GS6 nhưng có cấu hình nguồn, schema kiểm tra và
namespace riêng.

## Nguồn đã cấu hình

- File ID: `1c3_CSdnh9sxALEt-6FKyrd-4-J1K_Yhl`
- Tệp: `P3_Tong_Hop_LTT_2507-HN.xlsx`
- Sheet: `P3.Tổng hợp lệnh thao tác`
- Header: dòng 9; vùng đọc: `A9:CT`
- Điều kiện nhận dòng: cột E bằng `GS1`
- Mảng sản xuất được quy về 6 value stream từ cột AF:
  `Flexo`, `Hộp bồi & Offset`, `Sóng & phôi`, `Pallet`, `Phụ kiện`,
  `Khay giấy`; mã ngoài quy tắc vào `GS1 khác`.

## Nguyên tắc an toàn

- Mapping số liệu giữ cố định theo vị trí cột `S/U/AR/AT/BG/BI/CH`.
- Manifest phải có `plant = GS1`; dữ liệu nhà máy khác bị chặn trước phát hành.
- Nguồn lỗi thì workflow dừng; GitHub Pages tiếp tục giữ bản hợp lệ gần nhất.
- Dashboard mặc định tải tháng mới nhất; chỉ tải toàn bộ tháng khi người dùng
  chọn `Tất cả các tháng`.
- Không upload Excel vào repository.

## Tệp cấu hình riêng

- `factory-config.json`: bộ xử lý dữ liệu và workflow.
- `factory-config.js`: giao diện và nhận diện nhà máy.

Không sửa `index.html` hoặc `scripts/` khi chỉ đổi nguồn/nhà máy.
