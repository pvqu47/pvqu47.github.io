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

### Cài đặt Ubuntu từ Microsoft Store
Hỗ trợ từ phiên bản windows 16215 trở lên
{: .notice}

Hiện tại, từ 8/5/2018 thì trên Microsoft Store có 3 phiên bản Ubuntu là:
* [Ubuntu](https://www.microsoft.com/en-us/p/ubuntu/9nblggh4msv6?rtc=1) (Phiên bản ban đầu)
* [Ubuntu 16.04](https://www.microsoft.com/en-us/p/ubuntu-1604/9pjn388hp8c9)
* [Ubuntu 18.04](https://www.microsoft.com/en-us/p/ubuntu-1804/9n9tngvndl3q) (Bản mới nhất)

Theo mình thì nên dùng phiên bản đầu tiên bởi nó ổn định và ít lỗi hơn 😃. Sau khi cài đặt xong và restart, bạn có thể chạy lệnh bash hoặc ubuntu trên command prompt. Chi tiết cách cài đặt bạn có thể xem trên trang chủ [microsoft](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

## Cài đặt Hyper Terminal
Lên trang chủ của Hyper và tải bản mới nhất cho Windows. Cài đặt nó.

## Cài đặt cURL and Git
Vào bash Ubuntu đã được cài đặt ở trên sử dụng các lênh sau:
* Cài cURL
{% highlight Command %}
sudo apt-get install curl
{% endhighlight %}
* Cài Git
{% highlight Command %}
sudo apt-add-repository ppa:git-core/ppa
sudo apt-get update
sudo apt-get install git
{% endhighlight %}


