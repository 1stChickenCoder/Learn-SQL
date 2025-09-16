## Kết nối đến Cluster Mongo Atlas

Trên web chọn connect - compass - copy đường link

Trên compass nhấn `add new connect` - truyền đường link vào ` đổi mật khẩu

## Tạo database đầu tiên

Name: facebook_dev
Collection: users

## Thêm các trường

Chọn vào collection `users` tiếp theo chọn `Add Data` và chọn `Insert Document`

```js
    [
        {
            "name": "Đoàn Duy Hoàn",
            "age": 24
        },
        {
            "name": "Phạm Bảo Đạt",
            "age": 14
        }
    ]
```

## Tìm những doc có trường cụ thể

