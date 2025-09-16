## SQL

- Học 1 ngôn ngữ nhưng dùng được ở nhiều CSDL khác nhau
- Schema chặt chẽ
- Khuyến khích các tiêu chuẩn chuẩn hóa để giảm thiểu dư thừa dữ liệu
- Có thể mở rộng nhưng hơi tốn công

## NoSQL

- Dữ liệu lưu dưới dạng JSON với các cặp key-value
- Không cần schema, lưu ở bất cứ thứ gì
- Hiệu năng tuyệt vời, mở rộng theo chiều ngang dễ dàng

## Ví dụ về sự ưu việt của NoSQL

### Dùng SQL

Giả sử tạo một CSDL lưu thông tin người dùng

- id
- title
- firstName
- lastName
- gender
- telephone
- address

**Vấn đề 1**: một người có thể có nhiều số điện thoại, không thể nào tạo thêm một đống `telephone1`, `telephone2`,... Tạo thêm một bảng riêng, bảng `telephones`:

- id 
- contract_id
- address
- telephone_type

**Vấn đề 2**: một người có thể có nhiều địa chỉ, email,... Lại phải tạo thêm bảng `addresses`, `emails`,... Và cuối cùng tạo bảng `contracts`

**Vấn đề 3**: trong CSDL chúng ta cần thêm các otherdata, các trường khác,...

> => Điều này làm cho CSDL bị phân mảnh

**Vấn đề 4**: áp dụng full-text search rất khó khăn. Khi muốn tìm một trường nào đó phải vào từng bảng...

> => SQL quá cứng nhắc

### Dùng NoSQL

```js
{
    name: [
        "Doan", "Duy", "Hoan",
    ],
    company: "PornHub",
    jobtitle: "Vice president",
    address: [
        {
            home: "Hai Phong",
            company: "Ha Noi",
        }
    ],
}
```

## Khi nào dung MongoDB

- Tích hợp data lớn
- Cấu trúc cơ sở phức tạp
- Cần khả năng mở rộng nhanh, rẻ
- Cần tốc độ phát triển phần mềm nhanh

## Khi nào dùng SQL

- CSDL chặt chẽ về cấu trúc
- Quen thuộc với ngôn ngữ SQL