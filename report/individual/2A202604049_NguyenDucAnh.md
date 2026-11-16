# Báo cáo cá nhân — HoVaTen-MSSV

Đổi tên file theo quy tắc `MSSV_HoTen.md`. Ví dụ: `20241234_NguyenVanAn.md`.

Đoạn video: MOT17-09, 150 frame (frame 1–150), nguồn MOTChallenge, giấy phép CC BY-NC-SA 3.0.

## 0. Thông tin học viên

- Họ tên:
- MSSV:
- Mã đề (A/B/C): B
- Email:
- Link repository:
- Giờ bắt đầu:
- Giờ kết thúc:

## 1. Xem trước đoạn video (CP0)

Ghi **trước khi vẽ**, mỗi người một dòng.

| Mã | Frame mốc nhận diện (không chắc là lần đầu xuất hiện) | Frame cuối thấy được | Rẽ / dừng / đổi tốc độ ở frame | Bị che ở frame | Ghi chú |
|---|---|---|---|---|---|
| P1 | 0 | Chưa xác định | Chưa ghi nhận | 121–130; bị che tiếp từ 134 (mốc kết thúc chưa biết) | Mốc theo bảng nhận diện đề B |
| P2 | 0 | Chưa xác định | Chưa ghi nhận | Chưa ghi nhận | Mốc theo bảng nhận diện đề B |
| P3 | 40 | Chưa xác định | Chưa ghi nhận | Chưa ghi nhận | Mốc theo bảng nhận diện đề B |
| P4 | 0 | Chưa xác định | Chưa ghi nhận | Chưa ghi nhận | Mốc theo bảng nhận diện đề B |
| P5 | 2 | Chưa xác định | Chưa ghi nhận | Chưa ghi nhận | Mốc theo bảng nhận diện đề B |

Các frame mốc lấy từ bảng nhận diện của đề B theo thứ tự P1–P5. Đây là frame có điểm nhận diện, không khẳng định là frame đầu tiên người đó xuất hiện. Kết quả tự kiểm không cho biết frame cuối thấy được hoặc các mốc rẽ/dừng/đổi tốc độ; những thông tin này chưa được ghi lại nên không thể suy ra chắc chắn từ số liệu export.

## 2. Keyframe và thời gian (CP1, CP4)

Số liệu dưới đây lấy từ lần tự kiểm các file export hiện có. Cột mã là **ID trong file CVAT**, chưa đối chiếu được với P1–P5 từ bảng nhận diện.

| Mã (CVAT track ID) | Số keyframe | Keyframe ở frame | Số frame có mặt | Keyframe / 100 frame | Thời gian (phút) | Chỗ khó |
|---|---|---|---|---|---|---|
| 0 | 12 | 0, 10, 20, 30, 40, 50, 60, 70, 80, 90, 100, 110 | 120 | 10.0 | | |
| 1 | 2 | 130, 131 | 10 | 20.0 | | |
| 2 | 11 | 50, 60, 70, 80, 90, 100, 110, 120, 130, 140, 149 | 100 | 11.0 | | |
| 3 | 16 | 0, 10, 20, 30, 40, 50, 60, 70, 80, 90, 100, 110, 120, 130, 140, 149 | 150 | 10.7 | | |
| 4 | 16 | 0, 10, 20, 30, 40, 50, 60, 70, 80, 90, 100, 110, 120, 130, 140, 149 | 150 | 10.7 | | |
| 5 | 4 | 0, 10, 20, 30 | 40 | 10.0 | | |
| 6 | 6 | 0, 10, 20, 40, 50, 90 | 110 | 5.5 | | |
| **Tổng** | **67** | | **680** | **9.9** | | |

Keyframe / 100 frame của cả bài = 67 ÷ 680 × 100 = **9.9**.

Hai track có nhiều keyframe nhất là CVAT track 3 và 4 (16 keyframe mỗi track). Kết quả tự kiểm không cho biết lý do đặt keyframe hoặc track tương ứng với P1–P5; cần đối chiếu lại trên CVAT.

Thời gian làm và chỗ khó chưa được ghi trong kết quả tự kiểm; cần điền theo thực tế.

## 3. Đoạn bị che (CP2)

Người bị che: `P1`

| Mốc | Frame |
|---|---:|
| Bắt đầu bị che (lần 1) | 121 |
| Kết thúc bị che (lần 1) | 130 |
| Bắt đầu bị che tiếp (lần 2) | 134 |
| Kết thúc bị che (lần 2) | Chưa cung cấp |
| Mất hẳn (bật `outside`) / hiện lại (tắt `outside`) | Chưa cung cấp |

- Lần che đầu kéo dài 10 frame (121–130), tương đương khoảng 0,33 giây ở 30 fps. Đây là thời gian bị che; chưa có thông tin cho biết P1 có bị che khuất hoàn toàn (`outside`) hay không.
- Quyết định: giữ cùng ID / tạo track mới.
- Lý do (trả lời 3 câu: khuất bao lâu so với 60 frame, ngoại hình có khớp, chỗ hiện lại có đúng hướng và tốc độ):

...

Theo thông tin bổ sung, P1 bị che ở frame 121–130 và bị che tiếp từ frame 134; chưa có mốc kết thúc lần che thứ hai. Kết quả CVAT ghi số frame `occluded` theo track lần lượt là: track 0: 10, track 1: 9, track 2: 10, track 3: 0, track 4: 70, track 5: 40, track 6: 20. Chưa có thông tin đối chiếu P1 với CVAT track ID nào.

Ảnh chụp màn hình:

![Trước khi che](images/che_1_truoc.png)
![Giữa đoạn che, thấy cờ trên panel object](images/che_2_giua.png)
![Sau khi hiện lại, cùng ID](images/che_3_sau.png)

## 4. Tự review ID (CP3)

Lượt 1 theo người (đi ngược từ frame 149 về 0 trên CVAT), lượt 2 theo cảnh (nhảy 10 frame). Ít nhất 3 dòng; không có lỗi thì ghi một dòng "đã kiểm hai lượt, không lỗi".

Loại lỗi dùng đúng một trong 7 mã: `id_switch`, `fragmentation`, `lost`, `merge`, `false_track`, `drift`, `flag`.

| Frame | Mã người | Loại lỗi | Mô tả một câu | Phát hiện ở lượt | Đã sửa? |
|---:|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

Tổng hợp số lỗi theo loại:

| `id_switch` | `fragmentation` | `lost` | `merge` | `false_track` | `drift` | `flag` |
|---:|---:|---:|---:|---:|---:|---:|
| | | | | | | |

Lỗi nào chỉ lượt 2 (theo cảnh) mới thấy, lượt 1 (theo người) không thấy? Vì sao?

...

## 5. File xuất và kết quả tự kiểm (CP4)

| Kiểm tra | Kết quả |
|---|---|
| Tên file MOT 1.1 | `NguyenDucAnh_mot.zip` |
| Tên file CVAT for video 1.1 | `Nguyenducanh_cvat_video.zip` |
| Số track ID khác nhau trong `gt/gt.txt` (phải là 5) | **7 — chưa đạt yêu cầu 5 track** |
| Frame `outside` không có dòng trong `gt.txt` (đúng / sai) | Chưa xác minh riêng |
| Job đã completed trên CVAT máy cá nhân | Chưa ghi nhận |

**Lưu ý về track thừa:** Tôi đã remove một track trong CVAT nhưng sau đó không còn tìm thấy track đó trong giao diện để xóa tiếp. Tuy nhiên, lần export được tự kiểm vẫn chứa 7 track ID trong cả hai file. Tôi đã hỏi coach để xác nhận cách xử lý. Vì chưa xác định được nguyên nhân và chưa có hướng dẫn xác nhận, tôi giữ nguyên kết quả tự kiểm, không tự kết luận track nào là `fragmentation` hay `false_track`.

Dán phần tóm tắt in ra từ `src/check_submission.py`:

```text
=== Tóm tắt ===
  Lỗi: 1   |   Cảnh báo: 0
  Còn [LỖI]: sửa trên CVAT, xuất lại rồi chạy lại script.
```

## 6. Ba câu kết

1. Nếu được gán lại, bạn sẽ đặt keyframe khác ở đâu? Vì sao?

   Nếu được gán lại, tôi sẽ đặt keyframe sát trước và sau các đoạn P1 bị che, nhất là quanh frame 121–130 và frame 133 trước khi bị che tiếp từ frame 134. Có hai người đi ngang che khuất P1, nên các keyframe quanh đoạn này giúp kiểm tra box và chỉnh lại khi P1 hiện ra.

2. Có chỗ nào bạn không chắc "cùng ID hay ID mới"? Bạn đã quyết định và ghi chú thế nào?

   Khi P1 bị hai người đi ngang che khuất, tôi không chắc người xuất hiện về sau có phải P1 hay không. Tôi dựa vào các lần P1 xuất hiện tiếp theo để nhận diện và quyết định giữ cùng ID.

3. Một lỗi ID trong job của bạn (nếu không còn sót, chọn lỗi đã sửa) có thể làm xe tự lái dự đoán sai chuyển động của người đó như thế nào? Lỗi đó ảnh hưởng MOTA hay IDF1 nhiều hơn?

   Hiện tôi chưa biết track thừa là fragmentation hay false_track. Tôi đã remove track trong CVAT nhưng file export vẫn còn ID đó và tôi không tìm thấy track để xóa; tôi đã hỏi coach. Vì chưa xác định loại lỗi nên hiện chưa thể kết luận lỗi làm xe dự đoán sai chuyển động như thế nào hoặc ảnh hưởng MOTA hay IDF1 nhiều hơn.

## Bonus (nếu làm)

### B1 — Hai người đi sát

...

### B2 — So cách đặt keyframe

| Cách đặt | Số keyframe | Frame trôi nhất | Ghi chú |
|---|---:|---:|---|
| Đều mỗi 30 frame | | | |
| Theo chỗ đổi hướng | | | |

...

### B3 — So với tracker có sẵn

| Frame | Mã người | Tracker làm gì | Nhãn của bạn | Giải thích (đoán rồi sửa / ghép IoU / box score thấp / ngoại hình) |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## 7. Tài liệu tham khảo và công cụ AI đã dùng

**Tài liệu tham khảo**
- MOT17-09, MOTChallenge (Milan et al., 2016), giấy phép CC BY-NC-SA 3.0.
- Tài liệu hướng dẫn của bài lab: `docs/GUIDELINE.md`, `docs/CVAT_CHEATSHEET.md`, `RUBRIC.md`.

**Công cụ AI**
- Copilot: giải thích kết quả của `src/check_submission.py`, tính/định dạng số liệu keyframe đã có trong file export, và hỗ trợ chỉnh câu chữ các thông tin do học viên cung cấp.
- Không dùng AI để sinh box/track hoặc thực hiện tự review ID. Câu 1–2 mục 6 được diễn đạt dựa trên ý do học viên cung cấp; câu 3 ghi nhận việc học viên chưa xác định được nguồn gốc track thừa.
