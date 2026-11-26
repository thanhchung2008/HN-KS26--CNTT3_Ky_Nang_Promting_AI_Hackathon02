# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 07
- **Họ tên:**Đỗ Thành Chung
- **Lớp:**CNTT03
- **Link repository Pha2:**https://github.com/thanhchung2008/HN-KS26--CNTT3_Ky_Nang_Promting_AI_Hackathon02
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé vào cổng ra JSON

**KET QUA AI**

```text
[
  {
    "loai_ve": "VECH",
    "ngay_choi": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_tu": "nho",
    "ghi_chu": null
  },
  {
    "loai_ve": "VECN",
    "ngay_choi": "2027-01-03",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_tu": null,
    "ghi_chu": "Một người đang bó bột tay"
  },
  {
    "loai_ve": "VEVIP",
    "ngay_choi": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_tu": "lon",
    "ghi_chu": "Một bạn đi xe lăn"
  }
]
```

**Link trò chuyện:**https://share.gemini.google/RkPHAZ1TUJX5

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
* Tiền vé người lớn: 8 × 250.000 = 2.000.000 đồng.
* Tiền vé trẻ em: 4 × (250.000 × 60%) + 2 × 0 = 4 × 150.000 + 0 = 600.000 đồng.
* Tiền vé: 2.000.000 + 600.000 = 2.600.000 đồng.
* Giảm giá đoàn: 2.600.000 × 10% = 260.000 đồng (tiền vé sau giảm: 2.600.000 - 260.000 = 2.340.000 đồng).
* Phụ thu: 6 × 40.000 = 240.000 đồng.
* Tổng tiền: 2.340.000 + 240.000 = 2.580.000 đồng.

[RESULT: 2.580.000 đồng]
```

**Link trò chuyện:**https://share.gemini.google/9LXtuxTzvRxj

### b) Kiểm tra kết quả AI

Kết quả AI trả lời đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "dong_khu_choi",
  "so_khach": 4,
  "so_khu_bi_dong": 2,
  "tom_tat": "Khu trượt nước chính và khu sóng nhân tạo đóng cả ngày không báo trước."
}
```

**Link trò chuyện:**https://share.gemini.google/JseGh854ImaU

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| Đúng thông tin (50%) | 0.0 / 5.0 | - **Câu bị lỗi:** "Vé chiều bên em 150k thôi ạ, mát rượi luôn."<br>

<br>- **Lý do sai:** Báo sai giá vé chiều (VECH) là 150.000 đồng trong khi thông tin chuẩn là 180.000 đồng/vé người lớn.<br>

<br>

<br>- **Câu bị lỗi:** "Mưa mà đóng cửa thì bên em hoàn tiền mặt 100% cho chị nha."<br>

<br>- **Lý do sai:** Sai hoàn toàn chính sách đóng cửa vì thời tiết. Công ty không hoàn tiền mặt; khách đã vào dưới 2 giờ được tặng 1 vé cùng loại dùng trong 30 ngày, còn từ 2 giờ trở lên không được bù. | - **Câu sửa đề xuất:** "Giá vé chiều (VECH) bên em là 180.000 đồng/vé người lớn ạ."<br>

<br>

<br>- **Câu sửa đề xuất:** "Nếu công viên đóng cửa vì thời tiết, khách đã vào dưới 2 giờ sẽ được tặng 1 vé cùng loại sử dụng trong vòng 30 ngày (không áp dụng hoàn tiền mặt), còn khách đã vào từ 2 giờ trở lên sẽ không được bù vé ạ." |
| Đầy đủ (30%) | 0.0 / 3.0 | - **Câu bị lỗi:** Toàn bộ câu trả lời: "Hello chị! Vé chiều bên em 150k thôi ạ, mát rượi luôn. Mưa mà đóng cửa thì bên em hoàn tiền mặt 100% cho chị nha. Cần gì ới em nhé!"<br>

<br>- **Lý do sai:** Không có lời mời khách cung cấp ngày chơi và số lượng vé để đặt vé (và thiếu thông tin đối tượng áp dụng/điều kiện thời gian của chính sách thời tiết). | - **Câu sửa đề xuất:** "Chị vui lòng cho em xin ngày dự kiến đi chơi và số lượng vé để em hỗ trợ đặt vé cho mình nhé ạ." |
| Giọng điệu (20%) | 0.5 / 2.0 | - **Câu bị lỗi:** "Hello chị!"<br>

<br>- **Lý do sai:** Dùng từ chào tiếng Anh suồng sã ("Hello"), thiếu tính chuyên nghiệp trong tư vấn dịch vụ.<br>

<br>

<br>- **Câu bị lỗi:** "...mát rượi luôn."<br>

<br>- **Lý do sai:** Dùng khẩu ngữ suồng sã ("mát rượi luôn").<br>

<br>

<br>- **Câu bị lỗi:** "...hoàn tiền mặt 100% cho chị nha."<br>

<br>- **Lý do sai:** Dùng trợ từ suồng sã ("nha").<br>

<br>

<br>- **Câu bị lỗi:** "Cần gì ới em nhé!"<br>

<br>- **Lý do sai:** Dùng từ suồng sã ("ới"). | - **Câu sửa đề xuất:** "Dạ em chào chị ạ!"<br>

<br>

<br>- **Câu sửa đề xuất:** "...thời tiết buổi chiều khá mát mẻ, dễ chịu ạ."<br>

<br>

<br>- **Câu sửa đề xuất:** "...bên em hỗ trợ theo chính sách thời tiết của công viên ạ."<br>

<br>

<br>- **Câu sửa đề xuất:** "Chị cần hỗ trợ thêm thông tin gì, chị cứ nhắn để em tư vấn thêm nhé ạ!" |

Tổng điểm: 0.5 / 10
```

**Link trò chuyện:**https://share.gemini.google/bTecTf7R2LBQ
