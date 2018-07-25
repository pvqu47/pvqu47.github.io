---
layout: post
title: "Cài đặt và cấu hình bash Ubuntu 16.04 trên Windows 10"
excerpt: "Cách để có được một command-line đẹp và tiện dụng ngay trên Windows"
categories: [Linux]
comments: true
image:
  feature: https://raw.githubusercontent.com/pvqu47/pvqu47.github.io/master/img/Bash-Ubuntu-Win10.png
  credit: pvqu47
---

Ngày trước để có được một môi trường command-line để làm việc mà vẫn dùng Windows mình thường cài song song Ubuntu với Windows hoặc sử dụng máy ảo trên VMware, song hai cách trên mình thấy khá là bất tiện 😞. Với cách thứ nhất bạn phải dành ra một phần ổ cứng để cài Ubuntu, gặp nhiều lỗi linh tinh khi chuyển đổi giữa hệ điều hành. Còn cách thứ hai thì tốn nhiều RAM và thời gian mở lâu 😴   

## Cài đặt Ubuntu 16.04

### Cài đặt Windows Subsystem for Linux

Bật tính năng "Windows Subsystem for Linux" và sau đó restart.
* Open PowerShell với Administrator và chạy lệnh:
{% highlight PowerShell %}
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
{% endhighlight %}

* Restart lại máy tính khi xong.

### Cài đặt Ubuntu trên Microsoft Store
