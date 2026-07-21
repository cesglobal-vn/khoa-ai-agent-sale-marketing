# Review và tin nhắn khách Thảo An

> File đầu vào cho **Customer Insight Agent** (buổi 2). Dữ liệu giả định, mô phỏng review Shopee và inbox Facebook thật. Mỗi dòng là một mẩu nguyên văn để agent trích dẫn.
>
> Quy tắc: agent chỉ được rút insight từ file này. Insight nào không trích dẫn được thì phải gắn `[SUY LUẬN]`.

## A · Review Shopee

| ID | Sao | SKU | Nguyên văn |
|---|---|---|---|
| R01 | 5 | Serum rau má | "Da mình nhạy cảm lắm, dùng cái này không bị rát gì hết. Mừng ghê." |
| R02 | 5 | Serum rau má | "Mua vì thấy ghi không cồn. Dùng 3 tuần thấy mấy vết thâm mụn cũ mờ đi chút." |
| R03 | 4 | Serum rau má | "Ổn, nhưng chai 30ml hơi nhanh hết so với giá 320k." |
| R04 | 5 | Serum rau má | "Đọc thành phần thấy toàn cái đọc được, không có chất gì lạ. Yên tâm hơn mấy loại kia." |
| R05 | 3 | Serum rau má | "Dùng 1 tuần chưa thấy gì rõ lắm. Chắc phải kiên trì." |
| R06 | 5 | Kem nghệ mật ong | "Thơm mùi mật ong nhẹ, không gắt. Da khô của mình hợp." |
| R07 | 4 | Kem nghệ mật ong | "Kem hơi đặc, buổi sáng dùng thì bí, mình chuyển sang bôi tối thôi." |
| R08 | 2 | Kem nghệ mật ong | "Bôi lên hơi vàng da, phải chờ lâu mới thấm. Không hợp gu mình." |
| R09 | 5 | Mặt nạ đất sét | "Vùng chữ T bớt bóng dầu thật. Tuần đắp 2 lần." |
| R10 | 4 | Mặt nạ đất sét | "Đắp xong hơi khô căng, phải dưỡng ẩm ngay sau đó." |
| R11 | 5 | Serum rau má | "Trước mình dùng loại khác bị nổi mẩn, đổi qua đây thì ổn. Sẽ mua lại." |
| R12 | 5 | Combo | "Shop tư vấn kỹ, hỏi da mình thế nào rồi mới gợi ý. Thích cách bán hàng này." |
| R13 | 3 | Mặt nạ đất sét | "180k 5 miếng thấy hơi cao, ngoài kia rẻ hơn." |
| R14 | 5 | Serum rau má | "Hàng Việt mà chất lượng ổn, ủng hộ." |
| R15 | 4 | Serum rau má | "Giao hơi chậm, mất 5 ngày. Sản phẩm thì ok." |

## B · Tin nhắn inbox Facebook

| ID | Nguyên văn khách hỏi |
|---|---|
| M01 | "Da mình nhạy cảm lắm, dùng cái này có bị rát không shop?" |
| M02 | "Sản phẩm này có cồn không ạ? Mình dị ứng cồn." |
| M03 | "Em bị mụn ẩn với thâm, nên dùng cái nào ạ?" |
| M04 | "Có test da liễu thật không shop, cho xem giấy được không?" |
| M05 | "Bao lâu thì thấy hiệu quả ạ?" |
| M06 | "Đang dùng của hãng khác, đổi qua có sao không?" |
| M07 | "320k mắc quá, có size nhỏ dùng thử không shop?" |
| M08 | "Mua combo có giảm giá không ạ?" |
| M09 | "Shop có ship COD không? Mình muốn xem hàng rồi mới trả." |
| M10 | "Bầu dùng được không shop?" |
| M11 | "Mình mua trên Shopee được không hay đặt ở đây?" |
| M12 | "Da mình vừa khô vừa mụn thì hợp cái nào?" |
| M13 | "Có bị vón cục khi dùng chung kem chống nắng không?" |
| M14 | "Sao thấy shop rẻ hơn chỗ khác, hàng có chuẩn không?" |
| M15 | "Dùng hết chai có phải dùng tiếp không hay ngưng được?" |

## C · Bối cảnh kèm theo

- Phần lớn tin nhắn đến trong khung 20h đến 23h.
- Khách hỏi rất kỹ trước khi mua, trung bình 4 đến 6 lượt tin nhắn mới chốt.
- Sau khi bỏ Zalo, toàn bộ việc tư vấn và chốt dồn về inbox Facebook.

## Chỗ còn thiếu dữ liệu

- Khách phần lớn ở tỉnh thành nào.
- Tỷ lệ mua lần đầu so với mua lại.
- Lý do khách nhắn tin rồi không mua.
