# Hướng dẫn phát hành GS1

## 1. Tạo repository riêng

Tên khuyến nghị:

`gsp-next30-gs1-smart-factory`

Upload toàn bộ nội dung bên trong gói GS1 vào thư mục gốc. Phải giữ đúng:

- `.github/workflows/update-dashboard.yml`
- `scripts/process_excel.py`
- `scripts/verify_build.py`
- `factory-config.json`
- `factory-config.js`
- `index.html`

Không upload file Excel nguồn.

## 2. Cấu hình GitHub Pages

`Settings` → `Pages` → `Build and deployment` → `Source` → `GitHub Actions`

## 3. Chạy lần đầu

`Actions` → `Cập nhật Factory Dashboard` → `Run workflow` → nhánh `main`.

Chỉ nghiệm thu khi các bước xử lý, kiểm tra và phát hành đều xanh.

## 4. URL dự kiến

`https://manhtranvan021981-sys.github.io/gsp-next30-gs1-smart-factory/`

## 5. Điểm kiểm tra bắt buộc

- Đầu trang ghi `GS1 · Nhà máy Goldsun Hà Nội`.
- Trạng thái nguồn ghi `P3_Tong_Hop_LTT_2507-HN.xlsx`.
- Manifest có `plant = GS1`.
- Tổng dòng nhận chỉ bao gồm cột E = `GS1`.
- Bộ lọc tháng có `Tất cả các tháng`.
- Khi nguồn GS1 lỗi, dashboard GS6 vẫn hoạt động độc lập.
