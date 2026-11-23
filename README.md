[![GitHub Release](https://img.shields.io/github/release/nphung-sudo/zapret-openwrt)](https://github.com/nphung-sudo/zapret-openwrt/releases)
[![Github All Releases](https://img.shields.io/github/downloads/nphung-sudo/zapret-openwrt/total.svg)](https://github.com/nphung-sudo/zapret-openwrt/releases)

# zapret-openwrt: zapret2 branch

Customized & optimized OpenWrt packages (ipk/apk) for the [zapret2](https://github.com/bol-van/zapret2) anti-DPI utility, with LuCI web interface.

Nhánh **zapret2**: gói OpenWrt cho **zapret2** (thế hệ mới của zapret, chiến lược viết bằng Lua/LuaJIT), kèm giao diện quản lý LuCI.
Bản cho zapret thế hệ 1 nằm ở nhánh [`zapret1`](https://github.com/nphung-sudo/zapret-openwrt/tree/zapret1).

> **Zapret2 is not a VPN! Zapret2 is an Anti-DPI utility!**
> Zapret2 không phải VPN. Lưu lượng vẫn đi thẳng ra Internet; zapret2 chỉ biến đổi gói tin để hệ thống DPI của nhà mạng không nhận diện được.

## Packages / Các gói

| Package | Mô tả |
|---|---|
| `zapret2` | Gói chính: `nfqws2` + LuaJIT, script khởi động, cấu hình mặc định, hostlist |
| `luci-app-zapret2` | Giao diện web: **Services → Zapret2** |

- OpenWrt 24.10: `.ipk`
- OpenWrt 25.x: `.apk` (thư mục `apk/` trong file ZIP)

> Không cài đồng thời `zapret` và `zapret2` trên cùng một router.

## Installation / Cài đặt

1. Tải file ZIP **zapret2** đúng kiến trúc CPU của router tại [Releases](https://github.com/nphung-sudo/zapret-openwrt/releases).
   Kiểm tra kiến trúc: `cat /etc/openwrt_release | grep DISTRIB_ARCH`
2. **System → Software → Update lists...**, sau đó **Upload Package...** và cài lần lượt `zapret2` rồi `luci-app-zapret2`.
3. Đăng xuất, đăng nhập lại → mục **Services → Zapret2** sẽ xuất hiện.
4. Sau mỗi lần thay đổi cấu hình, bấm **Restart**.

Hướng dẫn chi tiết (bản gốc): [wiki của remittor/zapret-openwrt](https://github.com/remittor/zapret-openwrt/wiki)

## Build

Build tự động bằng GitHub Actions (OpenWrt SDK):

- **Actions → build → Run workflow** (chọn nhánh `zapret2`) để build thử, hoặc
- push tag dạng `v0.<major>.<date>` (vd. `v0.9.20260307`) trỏ vào commit của nhánh này để build và tạo release.

## Differences from upstream / Khác biệt so với bản gốc

- Build, release và updater trỏ về repo này thay vì repo gốc.
- _(Cập nhật danh sách tùy chỉnh / tối ưu tại đây)_

## Screenshots

![image](https://github.com/user-attachments/assets/b79940b3-6a0d-4310-bd58-e461be004397)

## Credits

- [bol-van/zapret2](https://github.com/bol-van/zapret2): tác giả công cụ zapret2
- [remittor/zapret-openwrt](https://github.com/remittor/zapret-openwrt): tác giả gói OpenWrt và LuCI gốc ([donate](https://github.com/remittor/donate))

License: [MIT](LICENSE)
