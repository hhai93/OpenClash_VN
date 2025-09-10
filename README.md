## Cách sử dụng

**Link tạo cấu hình Clash (ví dụ):**
```
http://<SUBCONVERTER_HOST>/sub?target=clash&url=<SUBSCRIPTION_URL>&config=<CONFIG_URL>
```
- `<SUBCONVERTER_HOST>`: link server Subconverter (Ex: *https://sub.ops.ci*)
- `<SUBSCRIPTION_URL>`: link sub proxy của bạn (Dạng encode, Ex: *https%3A%2F%2Fshadowmere.xyz%2Fapi%2Fb64sub%2F*)
- `<CONFIG_URL>`: link đến file config *.ini* (Dạng encode, Ex: *https%3A%2F%2Fraw.githubusercontent.com%2Fhhai93%2FOpenClash_VN%2Frefs%2Fheads%2Fmain%2Fclash_template_vn.ini*)

Nếu lười bạn có thể dùng luôn git này (Paste vào trình duyệt)
```
https://sub.ops.ci/sub?target=clash&url=https%3A%2F%2Fshadowmere.xyz%2Fapi%2Fb64sub%2F&config=https%3A%2F%2Fraw.githubusercontent.com%2Fhhai93%2FOpenClash_VN%2Frefs%2Fheads%2Fmain%2Fclash_template_vn.ini
```
Hoặc dùng trên web ui: https://sub.ops.ci

Kết quả trả về bạn có thể lưu thành `profile.yaml` và import vào Clash/Clash Meta/OpenClash.

---

### OpenWrt & dnsmasq
Bạn có thể forward từ dnsmasq sang Clash:
  ```
  127.0.0.1#5300
  ```
Hoặc có thể xóa block **dns** nếu sử dụng Adguard Home.

---

### Tham khảo
- [Subconverter by tindy2013](https://github.com/tindy2013/subconverter)
- [Custom OpenClash Rules by Aethersailor](https://github.com/Aethersailor/Custom_OpenClash_Rules)
