# Checklist toàn khóa: tài sản anh chị phải cầm về

**Khóa:** AI Agent cho Sale & Marketing · CES Global
**6 buổi x 150 phút · Hơn 40 tài sản dùng được**

Đây là bảng anh chị tự tick, không phải bảng giảng viên chấm. Một dòng chỉ được tick khi anh chị **mở được file thật** ra xem, không tick bằng trí nhớ.

**Cách dùng:**

1. Mở thư mục làm việc bên cạnh, dò từng dòng.
2. Dòng nào chưa có thì ghi vào cột cuối cách xử lý: chạy lại prompt trong tài liệu buổi đó, hay dùng bộ demo Thảo An thay thế.
3. Dò lại một lượt trước buổi 6, vì buổi 6 gom hết tài sản của 5 buổi trước. Thiếu đầu vào là ngồi làm lại và mất thời gian của cả lớp.
4. Sau buổi 6, dò lại lần cuối khi sắp xếp vào cấu trúc thư mục `<ten-thuong-hieu>-ai-system/`.

**"Thư mục làm việc"** trong bảng này là thư mục anh chị tạo ở buổi 1 và mở bằng tab Code của Claude Desktop. Sau buổi 6, các file được chuyển vào 8 thư mục đánh số, cột "Lưu ở đâu" ghi kèm chỗ mới.

---

## Buổi 1 · Bốn tầng ngữ cảnh

Tài liệu tra lại: [buoi-01-bon-tang-ngu-canh.md](buoi-01-bon-tang-ngu-canh.md)

| ✓ | Tài sản | Lưu ở đâu | Đạt khi |
|---|---|---|---|
| ☐ | Máy đã cài xong | Claude Desktop và Git trên máy | Mở Claude Desktop thấy tab Code, tài khoản trả phí dùng được |
| ☐ | Thư mục làm việc | Màn hình nền hoặc `C:\Users\<tên đăng nhập>\<tên thư mục>` | Mở được bằng tab Code, Claude đọc được file trong đó |
| ☐ | Hồ sơ sản phẩm | Thư mục làm việc, sau buổi 6 vào `01-nen-tang/` | Có tên sản phẩm, thành phần, công dụng, giá; chỗ chưa có thì để trống chứ không điền bừa |
| ☐ | `CLAUDE.md` đủ 9 mục | Ngay gốc thư mục làm việc, **không chuyển vào thư mục đánh số** | Claude trả lời đúng thương hiệu mà không cần nhắc lại. Có câu định vị, 3 thông điệp, 5 nỗi đau, giọng văn, từ cấm |
| ☐ | Câu định vị | Trong `CLAUDE.md` | Một câu, nói được bán gì cho ai và khác ở đâu |
| ☐ | 3 thông điệp bán hàng | Trong `CLAUDE.md` | Mỗi thông điệp gắn với một nhóm sản phẩm và một tình huống dùng |
| ☐ | 5 nỗi đau khách | Trong `CLAUDE.md` | Viết bằng lời khách, không phải lời marketing |
| ☐ | Memory đã bật và đã kiểm | Settings của Claude Desktop | Đã thử thấy Claude nhớ đúng, và biết đường vào xem, sửa, xóa cái nhớ sai |
| ☐ | Skill `viet-bai-ban-hang` | `.claude/skills/viet-bai-ban-hang/SKILL.md` | Đúng đường dẫn, có frontmatter `name` và `description`, chạy ra kết quả thật |
| ☐ | 3 bài bán hàng, lưu thành `bai-ban-hang-mau.md` | Thư mục làm việc, sau buổi 6 vào `01-nen-tang/` | Do chính Skill sinh ra, không dính từ cấm, soát xong là đăng được |
| ☐ | 10 hook và 10 CTA, lưu thành `hook-cta.md` | Thư mục làm việc, sau buổi 6 vào `01-nen-tang/` | Mỗi hook bám một nỗi đau; mỗi CTA rõ hành động tiếp theo và hợp kênh |
| ☐ | 1 kết nối MCP | Settings, mục Connectors | Claude đọc được dữ liệu từ Google Drive hoặc Sheet. Dùng tài khoản demo, không dùng tài khoản công ty thật |

**Phép thử quan trọng nhất của buổi 1:** hỏi Claude một điều mà hồ sơ ghi rõ là chưa có, ví dụ ngân sách quảng cáo tháng trước. Nó điền một con số nghe hợp lý là **chưa đạt**, dù mọi thứ khác xong hết.

---

## Buổi 2 · Customer Insight Agent

Tài liệu tra lại: [buoi-02-customer-insight-agent.md](buoi-02-customer-insight-agent.md)

| ✓ | Tài sản | Lưu ở đâu | Đạt khi |
|---|---|---|---|
| ☐ | Skill Customer Insight | `.claude/skills/customer-insight/SKILL.md` | Chạy lại trên đợt dữ liệu mới vẫn ra bảng đúng định dạng |
| ☐ | File dữ liệu khách đã đánh mã | Thư mục làm việc, sau buổi 6 vào `02-khach-hang/` | Tối thiểu 20 mẩu, đã bỏ tên thật và số điện thoại, mỗi mẩu một mã kiểu R01, M01, C01 |
| ☐ | `insight-khach-hang.md` | Thư mục làm việc, cạnh `CLAUDE.md`; sau buổi 6 vào `02-khach-hang/` | Mỗi dòng có mã nguồn và câu trích nguyên văn; cột tần suất ghi dạng "9 trên 30 mẩu"; chỗ suy ra gắn `[SUY LUẬN]` |
| ☐ | 3 persona | Trong `insight-khach-hang.md` | Mỗi persona truy được về ít nhất một trích dẫn, không mô tả nghề nghiệp hay thu nhập mà dữ liệu không nhắc tới |
| ☐ | 5 content angle | Trong `insight-khach-hang.md` | Mỗi angle truy được về ít nhất một trích dẫn |
| ☐ | 5 bài social | Thư mục làm việc, sau buổi 6 vào `02-khach-hang/` | Bám angle, đúng giọng thương hiệu, mỗi bài có một câu trích nguyên văn của khách |
| ☐ | 3 brief hình ảnh | Thư mục làm việc, sau buổi 6 vào `02-khach-hang/` | Người thiết kế đọc là làm được, không phải hỏi lại |
| ☐ | 3 visual đăng được | Thư mục làm việc, sau buổi 6 vào `02-khach-hang/` | Đúng tỷ lệ kênh, có nhận diện thương hiệu, mở xem được |
| ☐ | `CLAUDE.md` đã cập nhật mục 5 nỗi đau | Ngay gốc thư mục làm việc | Năm nỗi đau nay có mã trích dẫn và tần suất, không còn là phỏng đoán của buổi 1 |

---

## Buổi 3 · Sales Agent

Tài liệu tra lại: [buoi-03-sales-agent.md](buoi-03-sales-agent.md)

| ✓ | Tài sản | Lưu ở đâu | Đạt khi |
|---|---|---|---|
| ☐ | 3 skill đã chỉnh theo ngành và chính sách của mình | `.claude/skills/lead-scoring/SKILL.md`, `.claude/skills/soan-proposal/SKILL.md`, `.claude/skills/theo-duoi-chot-don/SKILL.md` | Chấm được lead mới theo đúng bộ tiêu chí đã định, không đổi kết quả mỗi lần chạy |
| ☐ | Danh sách 10 lead đủ 6 cột | Thư mục làm việc, sau buổi 6 vào `03-ban-hang/` | Có tên cơ sở, loại hình, khu vực, kênh liên hệ, người phụ trách, ghi chú trao đổi nguyên văn. Thiếu thì để trống |
| ☐ | Bảng chính sách giá và chiết khấu | Thư mục làm việc, sau buổi 6 vào `03-ban-hang/` | Có mục "điều chưa có chính sách", tối thiểu 5 dòng |
| ☐ | `bang-diem-lead.md`, 10 lead | Thư mục làm việc, sau buổi 6 vào `03-ban-hang/` | Có tiêu chí, trọng số tổng 100, điểm, lý do, hành động kế tiếp, và cột độ tin cậy. Lead thiếu ghi chú phải bị hạ độ tin cậy |
| ☐ | 10 email cá nhân hóa | Thư mục làm việc, sau buổi 6 vào `03-ban-hang/` | Phép thử đổi tên: thay tên lead này bằng lead khác mà email vẫn dùng nguyên si được thì đó là mẫu điền tên, chưa đạt |
| ☐ | 10 tin nhắn Zalo hoặc LinkedIn | Thư mục làm việc, sau buổi 6 vào `03-ban-hang/` | Ngắn, hợp kênh, nêu rõ lý do liên hệ |
| ☐ | 1 kịch bản gọi 5 phút | Thư mục làm việc, sau buổi 6 vào `03-ban-hang/` | Có mở đầu, câu hỏi thăm dò, chuyển tiếp, kết |
| ☐ | 10 kịch bản xử lý từ chối | Thư mục làm việc, sau buổi 6 vào `03-ban-hang/` | Mỗi lời từ chối có câu trả lời không hứa quá chính sách |
| ☐ | `proposal-<mã lead>.md`, 3 tới 5 trang | Thư mục làm việc, sau buổi 6 vào `03-ban-hang/` | Bảng giá đúng chính sách. Khách hỏi điều chưa có chính sách thì để trống và ghi "cần xin ý kiến", không tự hứa con số |

---

## Buổi 4 · Content Engine Agent

Tài liệu tra lại: [buoi-04-content-engine-agent.md](buoi-04-content-engine-agent.md)

| ✓ | Tài sản | Lưu ở đâu | Đạt khi |
|---|---|---|---|
| ☐ | Skill Content Engine đã chỉnh cho ngành mình | `.claude/skills/content-engine/SKILL.md` | Nhận insight, trả ra lịch và bài đúng ràng buộc; tới bước viết caption thì gọi lại skill `viet-bai-ban-hang` |
| ☐ | Campaign brief 8 mục | Thư mục làm việc, sau buổi 6 vào `04-chien-dich/` | Có mục tiêu bằng con số, đối tượng, thông điệp, kênh, cách đo |
| ☐ | `lich-14-ngay.md` | Ngay trong thư mục làm việc, sau buổi 6 vào `04-chien-dich/` | Bảng 14 dòng, 8 cột, không ô nào trống. Đủ 4 loại ngày: giáo dục, bằng chứng, xử lý phản đối, ưu đãi |
| ☐ | 10 bài social, trong đó 1 carousel | Thư mục làm việc, sau buổi 6 vào `04-chien-dich/noi-dung-da-kenh/` | Không trùng ý; mỗi bài một nỗi đau, một điểm khác biệt, một lời kêu gọi |
| ☐ | 3 email nurturing | Thư mục làm việc, sau buổi 6 vào `04-chien-dich/noi-dung-da-kenh/` | Có mạch nối, không phải 3 email rời nhau |
| ☐ | 1 khối landing page | Thư mục làm việc, sau buổi 6 vào `04-chien-dich/noi-dung-da-kenh/` | Đủ tiêu đề, lợi ích, bằng chứng, nút hành động |
| ☐ | 3 kịch bản video 30 tới 60 giây | Thư mục làm việc, sau buổi 6 vào `04-chien-dich/noi-dung-da-kenh/` | Có 3 giây mở đầu giữ người xem |
| ☐ | Carousel 6 tới 8 slide | Thư mục làm việc, sau buổi 6 vào `04-chien-dich/noi-dung-da-kenh/` | Mỗi slide một ý, slide cuối có lời kêu gọi |
| ☐ | 5 brief hình ảnh hoặc video | Thư mục làm việc, sau buổi 6 vào `04-chien-dich/` | Đủ để sản xuất mà không hỏi lại |
| ☐ | Bảng ràng buộc của ngành mình | Dán vào đầu file skill Content Engine | Có từ cấm, cam kết bị cấm, quy định ngành, cụm công dụng được phép nói, tên người duyệt cuối |

---

## Buổi 5 · Automation và MCP

Tài liệu tra lại: [buoi-05-automation-va-mcp.md](buoi-05-automation-va-mcp.md) và [buoi-05-luong-post-bai.md](buoi-05-luong-post-bai.md)

| ✓ | Tài sản | Lưu ở đâu | Đạt khi |
|---|---|---|---|
| ☐ | `automation-map.md` | Ngay trong thư mục làm việc, sau buổi 6 vào `05-tu-dong-hoa/` | Tối thiểu 3 luồng, đủ 5 cột: kích hoạt, xử lý, đưa ra, ai duyệt, ghi log ở đâu. Ô "Ai duyệt" ghi tên người |
| ☐ | Bảng quản lý trên Sheet, Airtable hoặc Notion | Ngoài máy; ghi link vào `automation-map.md` | Có cột Trạng thái và cột Người duyệt, link mở được |
| ☐ | 1 automation chạy được, hoặc prototype | Thư mục làm việc, sau buổi 6 vào `05-tu-dong-hoa/` | Chạy thử được ít nhất một lượt từ đầu tới cuối. Prototype thì có ảnh chụp từng bước |
| ☐ | Bảng log bài đăng | Cùng chỗ với bảng quản lý | Tối thiểu 6 cột: ngày, nội dung, kênh, ai duyệt, kết quả, ghi chú |
| ☐ | 1 mẫu thông báo hoặc email nội bộ | Thư mục làm việc, sau buổi 6 vào `05-tu-dong-hoa/` | Người nhận đọc xong biết ngay phải làm gì tiếp |
| ☐ | 1 checklist kiểm soát rủi ro đã điền | Thư mục làm việc, sau buổi 6 vào `05-tu-dong-hoa/` | Ghi rõ việc nào tuyệt đối không chạy tự động, và trả lời được: kênh đang nối là kênh gì, duyệt xong có hẹn giờ không, học xong có gỡ quyền không |
| ☐ | Đã tập một lần dời giờ và một lần hủy bài đã hẹn | Không có file, tự kiểm | Anh chị gõ được câu để dời giờ và câu để hủy, không phải tra lại tài liệu |

**Luật riêng buổi 5:** kênh đang nối phải là kênh demo hoặc kênh cá nhân, không phải fanpage công ty đang chạy. Mọi luồng có bước gửi ra ngoài đều phải có chốt duyệt trước bước đó, kể cả trước bước hẹn giờ.

---

## Buổi 6 · Claude Skill và Playbook

Tài liệu tra lại: [buoi-06-claude-skill-va-playbook.md](buoi-06-claude-skill-va-playbook.md)

| ✓ | Tài sản | Lưu ở đâu | Đạt khi |
|---|---|---|---|
| ☐ | Claude Skill hoàn chỉnh | `.claude/skills/<tên-skill>/SKILL.md`; một bản để đọc đặt ở `06-skill/` | Đủ 7 mục; tiêu chuẩn đầu ra viết bằng số cho từng loại; ba nguyên tắc chống bịa nằm nguyên văn trong phần thân |
| ☐ | Skill chạy được ngoài bối cảnh gốc | Ghi kết quả 2 phép thử vào workbook | Chạy 2 yêu cầu chưa từng làm, trong phiên mới, không nhắc tên skill, cả 2 đều đạt đúng bảng tiêu chuẩn do chính anh chị viết |
| ☐ | AI Agent Playbook | `00-doc-truoc/playbook.md` | Đủ 7 mục: mục đích, ai dùng, quy trình, tiêu chuẩn đầu ra, ranh giới, chỉ số đo, xử lý khi agent ra sai |
| ☐ | Bộ tài sản sắp xếp theo project | Thư mục `<ten-thuong-hieu>-ai-system/` | Đủ 8 nhánh đánh số; `CLAUDE.md` và `.claude/skills/` nằm ở gốc; người khác đọc tên 3 tài sản bất kỳ, anh chị mở được cả 3 trong 10 giây |
| ☐ | Automation hoặc prototype bàn giao được | `05-tu-dong-hoa/` | Kế thừa buổi 5, chạy được, có bước người duyệt, có hướng dẫn chạy |
| ☐ | Demo agent 5 phút | Ghi chú demo trong workbook, kèm phiếu chấm chéo | Trình bày dưới 5 phút có bấm giờ, mở đầu bằng kết quả không bằng tên công cụ, đạt từ 10 trên 12 điểm chấm chéo |
| ☐ | Kế hoạch triển khai 14 ngày | `00-doc-truoc/ke-hoach-14-ngay.md` | Đủ 14 dòng, 4 cột ngày, việc, ai làm, kết quả cần thấy. Cột "ai làm" ghi tên người thật. Ngày 7 và ngày 14 có mốc kiểm chỉ số |

---

## Đếm nhanh: anh chị đang có bao nhiêu

| Nhóm | Số tài sản | Đã có |
|---|---|---|
| Agent và skill | 7: `viet-bai-ban-hang`, Customer Insight, Lead Scoring, Soạn proposal, Theo đuổi chốt đơn, Content Engine, Skill đóng gói buổi 6 | ____ trên 7 |
| Nội dung | 18 bài social trở lên, 3 email nurturing, 3 kịch bản video, 1 carousel, 1 khối landing page, 8 brief hình ảnh | ____ |
| Bán hàng | 10 email, 10 tin nhắn, 1 kịch bản gọi, 10 kịch bản xử lý từ chối, 1 bảng điểm lead, 1 proposal | ____ |
| Nền tảng | Thư mục làm việc, `CLAUDE.md`, Memory, `insight-khach-hang.md`, campaign brief, `lich-14-ngay.md`, `automation-map.md`, bảng quản lý, Playbook, kế hoạch 14 ngày | ____ trên 10 |

Tick đủ bảng trên là vượt 40 tài sản dùng được.

---

## Ba câu tự hỏi cuối khóa

Ba câu này quan trọng hơn số lượng. Trả lời thật, vì không ai chấm anh chị ở đây.

**1. Người khác dùng lại được không?**

Đưa Skill và Playbook cho một đồng nghiệp chưa học khóa này. Họ chạy trên một yêu cầu chưa từng làm, không hỏi anh chị câu nào. Kết quả có đạt đúng bảng tiêu chuẩn đầu ra do chính anh chị viết không.

Họ phải hỏi lại dù chỉ một câu, thì đó là dấu hiệu Skill hoặc Playbook còn thiếu một phần mà anh chị đang giữ trong đầu. Ghi lại đúng câu hỏi đó, và bổ sung đúng chỗ đó.

- [ ] Đã đưa cho một người chạy thử. Họ hỏi lại ____ câu. Đã bổ sung xong.

**2. Agent có chịu nói "chưa đủ dữ liệu" không?**

Chọn ba con số mà hồ sơ trong thư mục làm việc ghi rõ là chưa có. Mở một phiên mới, hỏi thẳng ba câu đó.

Có bất kỳ câu nào trả về một con số, một khoảng, hay một mức "tham khảo của ngành" là **chưa đạt**, dù mọi thứ khác đẹp. Con số đó anh chị sẽ mang đi báo cáo sếp hoặc đưa vào proposal gửi khách. Bỏ qua ở đây là để lại rủi ro thật cho việc thật.

- [ ] Đã chạy 3 câu hỏi. Cả 3 đều trả về "chưa đủ dữ liệu" kèm tên nguồn cần bổ sung.

**3. Có đo được không?**

Sau 14 ngày triển khai, anh chị nhìn vào đâu để biết việc này có tác dụng.

Ba chỉ số quá trình đo được ngay từ tuần 1: thời gian làm một đầu ra; số đầu ra mỗi tuần; tỉ lệ nháp được duyệt ngay lần đầu. Chỉ số kinh doanh cần thêm chu kỳ, đọc được từ tuần thứ 4 trở đi.

Trả lời được ba câu "trước bao nhiêu, giờ bao nhiêu, đo bằng cách nào" là đạt. Trả lời "thấy nhanh hơn nhiều" là chưa đo được gì.

- [ ] Thời gian làm 1 đầu ra: trước ____ phút, giờ ____ phút. Đo bằng: ____
- [ ] Số đầu ra mỗi tuần: trước ____, giờ ____. Đo bằng: ____
- [ ] Tỉ lệ nháp duyệt ngay lần đầu: ____ trên ____. Đo bằng: ____

---

CES Global · Creative, Effective, Sustainable
