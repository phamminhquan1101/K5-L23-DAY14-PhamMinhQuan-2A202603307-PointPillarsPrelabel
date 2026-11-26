# Báo cáo Day 14 — <Họ và tên> — <MSSV></mssv>

- Mã học viên dùng với `--student`: `2A202603307>`
- `seed_tag` trong `frames_A.txt`: 82ac3100fd

## 1. Dự đoán trước sweep (bước 5b)

Tôi dự đoán tăng `score_thr` sẽ giảm công sửa. Trong tập A, 59/74 hộp cần xóa có score dưới 0,5, còn phần lớn hộp khớp nhãn có score cao. Tuy nhiên, tăng ngưỡng có thể loại cả hộp đúng và làm tăng số vật cần thêm lại.

## 2. Tập A: sửa tay và tune

| Cấu hình           | Xóa | Thêm | Sửa | Chi phí |
| -------------------- | ---: | ----: | ---: | -------: |
| Gốc                 |      |       |      |          |
| `best_config.json` |      |       |      |          |

- Tham số đã đổi trong `best_config.json`: ...
- Kết quả leave-one-out (dán các dòng `scripts/pp_sweep.py` in ra): ...
- Cấu hình có ổn định trên từng frame không? Vì sao tôi vẫn chọn (hoặc không chọn) nó: ...

## 3. Trước/sau (bước 8)

![so sánh](<../../d14_<ID></id>/compare/.jpg>)

- `scripts/pp_compare.py` báo giảm (hoặc tăng) ...% công sửa trên tập A.
- Dự đoán ở mục 1 đúng hay sai? Giải thích bằng số box xóa/thêm/sửa: ...

## 4. Tập B

Số đo từ `scripts/pp_prelabel.py --frames d14_<ID>/frames_B.txt --config d14_<ID>/best_config.json --gt d14_<ID>/ref_B.json`:

| Xóa | Thêm | Sửa | Chi phí |
| ---: | ----: | ---: | -------: |
|      |       |      |          |

- Loại box tốn công sửa nhất ở tập B: ...

## 5. Giới hạn

- Nêu ít nhất 2 giới hạn (ví dụ: chỉ 3 frame tune; model KITTI không có Truck/Bus; chi phí là công thức, chưa phải thời gian sửa thật): ...
