[![GitHub Release](https://img.shields.io/github/release/nphung-sudo/zapret-openwrt)](https://github.com/nphung-sudo/zapret-openwrt/releases)
[![Github All Releases](https://img.shields.io/github/downloads/nphung-sudo/zapret-openwrt/total.svg)](https://github.com/nphung-sudo/zapret-openwrt/releases)

# zapret-openwrt

Customized & optimized OpenWrt packages (ipk/apk) for the [zapret](https://github.com/bol-van/zapret) / [zapret2](https://github.com/bol-van/zapret2) anti-DPI utilities, with LuCI web interface.

Gói OpenWrt tùy chỉnh và tối ưu cho công cụ chống DPI **zapret** và **zapret2**, kèm giao diện quản lý LuCI. Dựa trên [remittor/zapret-openwrt](https://github.com/remittor/zapret-openwrt).

> **Zapret is not a VPN! Zapret is an Anti-DPI utility!**
> Zapret không phải VPN. Lưu lượng vẫn đi thẳng ra Internet; zapret chỉ biến đổi gói tin để hệ thống DPI của nhà mạng không nhận diện được.

## Branches / Các nhánh

| Nhánh | Nội dung | Gói | Tag release |
|---|---|---|---|
| [`main`](https://github.com/nphung-sudo/zapret-openwrt/tree/main) | Phần dùng chung: README, LICENSE, workflow | – | – |
| [`zapret1`](https://github.com/nphung-sudo/zapret-openwrt/tree/zapret1) | zapret thế hệ 1 (`nfqws`) | `zapret`, `luci-app-zapret` | `v72.YYYYMMDD` |
| [`zapret2`](https://github.com/nphung-sudo/zapret-openwrt/tree/zapret2) | zapret2 (`nfqws2` + LuaJIT) | `zapret2`, `luci-app-zapret2` | `v0.9.YYYYMMDD` |

> Không cài đồng thời `zapret` và `zapret2` trên cùng một router.

## Download / Tải về

[Releases](https://github.com/nphung-sudo/zapret-openwrt/releases): chọn file ZIP `zapret_…` hoặc `zapret2_…` đúng kiến trúc CPU của router
(`cat /etc/openwrt_release | grep DISTRIB_ARCH`). Hướng dẫn cài đặt: xem README của nhánh tương ứng.

## Build

- **Actions → build → Run workflow**, chọn nhánh `zapret1` hoặc `zapret2`.
- Hoặc push tag trỏ vào commit của nhánh tương ứng (không tag trên `main`).

`main` giữ `build.yml` và `releases.yml` vì GitHub chỉ hiện nút *Run workflow* và chỉ chạy sự kiện `release` / `workflow_run` theo workflow trên nhánh mặc định. Khi build, GitHub dùng `build.yml` của nhánh được chọn.

## Credits

- [bol-van/zapret](https://github.com/bol-van/zapret), [bol-van/zapret2](https://github.com/bol-van/zapret2): tác giả công cụ zapret
- [remittor/zapret-openwrt](https://github.com/remittor/zapret-openwrt): tác giả gói OpenWrt và LuCI gốc ([donate](https://github.com/remittor/donate))

License: [MIT](LICENSE)
