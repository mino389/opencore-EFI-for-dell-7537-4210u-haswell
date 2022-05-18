# opencore-EFI-for-dell-7537-4210u-haswell

Đây là bản dựng OpenCore cho sản phẩm DELL Inspiron 7537 với thông số cấu hình chi tiết bên dưới:

* Chi tiết: https://downloads.dell.com/manuals/all-products/esuprt_laptop/esuprt_inspiron_laptop/inspiron-15-7537_reference%20guide_en-us.pdf
* Thông tin thêm: https://www.notebookcheck.net/Review-Dell-Inspiron-15-7537-Notebook.104976.0.html

# Hình ảnh
![Ảnh chụp Màn hình 2022-02-13 lúc 17 55 33](https://user-images.githubusercontent.com/55343489/153750013-69cb0e9d-6355-450b-90b6-14bb804e2ef2.png)

# THÔNG SỐ CẤU HÌNH:
*   CPU: Intel 4210u Haswell
*   GPU: Intel 4400 (GT750m đã tắt)
*   AUDIO: ALC283 (layout_id=88)
*   NIC: RTL8111
*   RAM: 2x8GB DDR3
*   SSD: 1TB 2.5" SATA
*   WIFI: BCM94360HMB
*   USB: 3.0x4
*   Card Reader: RTL8411B
#   BIOS SETUP
*   _ENABLE_
- VT-x
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: UEFI Mode
- DVMT Pre-Allocated(iGPU Memory): 64MB
- SATA Mode: AHCI
*   _DISABLE_
- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port
- VT-d (can be enabled if you set DisableIoMapper to YES)
- CSM
- Thunderbolt(For initial install, as Thunderbolt can cause issues if not setup correctly)
- Intel SGX
- Intel Platform Trust
#  HOẠT ĐỘNG:
*   Wifi, bluetooth, usb x4 port, igpu 4400, bàn phím, bàn di chuột, HDMI, Âm thanh - 3.5 jack - hdmi audio, ngủ -thức, quản lý điện năng cpu - quạt - nhiệt độ, card reader, airdrop*, camera, iMessage, facetime, icloud.
# VẤN ĐỀ TỒN TẠI:
*   Hệ thống gần như hoạt động tốt.
*   Chỉnh độ sáng bàn phím không khả dụng trong cài đặt
*   airdrop gửi file đi ( cần phải đánh thức airdrop của 2 thiết bị nhận có hỗ trợ)
*   1 số cử chỉ bàn di chuột không hỗ trợ
# HỖ TRỢ:
* MACOS Monterey 12
* Haswell(4th gen Intel) Mobile:
Core i3-4005U
Core i3-4010U
Core i3-4030U
Core i5-4200U
Core i5-4210U
Core i5-4300U
Core i5-4310U
Core i7-4500U
Core i7-4510U
# LƯU Ý:
* Mọi chỉnh sửa "Config.plist" từ phần mềm bên thứ 3 không phải "Propertree" có thể làm hệ thống không thể khởi động <OC0.8.0>
* GenSMBIOS theo mô hình của bạn *ROM-En0*, mặc định macbookpro 11.4
* Khuyến nghị nên thay thẻ WIFI BCM94360HMB - không có Wifi với thẻ Intel xuất xưởng
* Thêm Kext WIFI trên Monterey không được hỗ trợ có thể gây ra lỗi Panic-Kernel
