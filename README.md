[![GitHub Release](https://img.shields.io/github/release/nphung-sudo/zapret-openwrt)](https://github.com/nphung-sudo/zapret-openwrt/releases)
[![Github All Releases](https://img.shields.io/github/downloads/nphung-sudo/zapret-openwrt/total.svg)](https://github.com/nphung-sudo/zapret-openwrt/releases)

# zapret-openwrt (custom fork)

Customized & optimized OpenWrt packages (ipk/apk) for the [zapret](https://github.com/bol-van/zapret) anti-DPI utility, with LuCI web interface.

Bản fork tùy chỉnh và tối ưu của [remittor/zapret-openwrt](https://github.com/remittor/zapret-openwrt): gói OpenWrt cho công cụ chống DPI **zapret**, kèm giao diện quản lý LuCI.

> **Zapret is not a VPN! Zapret is an Anti-DPI utility!**
> Zapret không phải VPN. Lưu lượng vẫn đi thẳng ra Internet; zapret chỉ biến đổi gói tin để hệ thống DPI của nhà mạng không nhận diện được.

## Packages / Các gói

| Package | Mô tả |
|---|---|
| `zapret` | Gói chính: `nfqws`, `ip2net`, `mdig`, script khởi động, cấu hình mặc định, hostlist |
| `luci-app-zapret` | Giao diện web: **Services → Zapret** |

- OpenWrt 24.10: `.ipk`
- OpenWrt 25.x: `.apk` (thư mục `apk/` trong file ZIP)

## Installation / Cài đặt

1. Nếu từng cài zapret bằng `install_easy.sh`, chạy `/opt/zapret/uninstall_easy.sh` và xóa `/opt/zapret`.
2. Tải file ZIP đúng kiến trúc CPU của router tại [Releases](https://github.com/nphung-sudo/zapret-openwrt/releases).
   Kiểm tra kiến trúc: `cat /etc/openwrt_release | grep DISTRIB_ARCH`
3. **System → Software → Update lists...**, sau đó **Upload Package...** và cài lần lượt `zapret` rồi `luci-app-zapret`.
4. Đăng xuất, đăng nhập lại → mục **Services → Zapret** sẽ xuất hiện.
5. Sau mỗi lần thay đổi cấu hình, bấm **Restart**.

Hướng dẫn chi tiết (bản gốc): [wiki của remittor/zapret-openwrt](https://github.com/remittor/zapret-openwrt/wiki)

## Build

Build tự động bằng GitHub Actions (OpenWrt SDK):

- **Actions → build → Run workflow** để build thử, hoặc
- push tag dạng `v<version>` (vd. `v72.20260307`) để build và tạo release.

## Differences from upstream / Khác biệt so với bản gốc

- Build, release và updater trỏ về repo này thay vì repo gốc.
- _(Cập nhật danh sách tùy chỉnh / tối ưu tại đây)_

## Screenshots

![image](https://github.com/user-attachments/assets/b79940b3-6a0d-4310-bd58-e461be004397)

## Credits

- [bol-van/zapret](https://github.com/bol-van/zapret): tác giả công cụ zapret
- [remittor/zapret-openwrt](https://github.com/remittor/zapret-openwrt): tác giả gói OpenWrt và LuCI gốc ([donate](https://github.com/remittor/donate))

License: [MIT](LICENSE)
