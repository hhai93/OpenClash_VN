## Cách 1 — Dùng URL của Subconverter (API)

Yêu cầu bạn có dịch vụ **Subconverter** đang chạy (local hoặc server). Mặc định cổng là `25500`.

**Link tạo cấu hình Clash (ví dụ):**
```
http://<SUBCONVERTER_HOST>:25500/sub?target=clash&url=<SUBSCRIPTION_URL>&config=<CONFIG_URL>
```
- `<SUBCONVERTER_HOST>`: link server đang host Subconverter
- `<SUBSCRIPTION_URL>`: link sub proxy của bạn (**Dạng encode**).
- `<CONFIG_URL>`: link đến file config *.ini* (**Dạng encode**).

**Ví dụ thực tế (local):**
```
http://localhost:25500/sub?target=clash&url=https%3A%2F%2Fexample.com%2Fmy-sub.txt&config=https%3A%2F%2Fraw.githubusercontent.com%2F%3Cuser%3E%2F%3Crepo%3E%2Fmain%2Fmerged_vn_full.ini
```

> Kết quả trả về là file YAML Clash. Bạn có thể lưu thành `profile.yaml` và import vào Clash/Clash Meta/OpenClash.

---

## Cách 2 — Dùng qua giao diện LUCI OpenClash (OpenWrt)

1. Vào **Services → OpenClash** và bảo đảm **Core** đã được cài.
2. Chọn tab **Config Subscribe**.
3. Chọn **Add** > Nhập: **Config Alias - đặt tên**, **Subscribe Address - link sub proxy của bạn** > Tick **Subscribe Convert Online** > **Template name**: Chọn **Custom template** > dán link file *.ini* vào **Custom Template URL**
4. Chọn **Commit Settings** > **Update Config** để OpenClash tải cấu hình về.
5. Quay lại tab **Overview** và khởi chạy.

---

### OpenWrt & dnsmasq
> Bạn có thể forward từ dnsmasq sang Clash:
  ```
  127.0.0.1#5450
  ```
> Hoặc có thể xóa block **dns** nếu sử dụng Adguard Home.
---

### Tham khảo
- [Subconverter by tindy2013](https://github.com/tindy2013/subconverter)
- [Custom OpenClash Rules by Aethersailor](https://github.com/Aethersailor/Custom_OpenClash_Rules)