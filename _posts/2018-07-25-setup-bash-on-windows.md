---
layout: post
title: "Cài đặt và cấu hình bash Ubuntu 16.04 trên Windows 10"
excerpt: "Cách để có được một command-line đẹp và tiện dụng ngay trên Windows"
categories: [Linux]
tags: [Linux, bash, ubuntu 16.04, zsh, oh-my-zsh]
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

Theo mình thì nên dùng phiên bản đầu tiên bởi nó ổn định và ít lỗi hơn 😃. Sau khi cài đặt xong và restart, bạn có thể chạy lệnh `bash` hoặc `ubuntu` trên command prompt. Chi tiết cách cài đặt bạn có thể xem trên trang chủ [Microsoft](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

## Cài đặt Hyper Terminal
Lên trang chủ của [Hyper](https://hyper.is/) và tải bản mới nhất cho Windows. Cài đặt nó.

## Cài đặt cURL and Git
Vào bash Ubuntu đã được cài đặt ở trên thực hiện các lệnh sau:
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

## Cài đặt Zsh
Để cài đặt Zsh thực hiện lệnh sau:
{% highlight Command %}
sudo apt-get install zsh
{% endhighlight %}

## Cài đặt Oh My Zsh
Thực hiện lệnh 
{% highlight Command %}
curl -L https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh | bash
{% endhighlight %}
và chờ cho đến khi cài đặt xong

## Cấu hình và chạy Oh My Zsh
Bây giờ mỗi lần khi bạn cần sử dụng bash shell và zsh, bạn cần thực hiện lệnh `bash` (hoặc `ubuntu`) và sau đó là `zsh`. Để cấu hình cho `bash` mặc định là `zsh` chúng ta cần thêm vào đầu file `.bashrc` lệnh sau:
{% highlight Command %}
bash -c zsh
{% endhighlight %}
Sử dụng lệnh `sudo nano ~/.bashrc` để mở file `.bashrc`. 

## Cấu hình và chạy Hyper Terminal
Sau khi cài đặt Hyper Terminal mở file `%USERPROFILE%/.hyper.js` (ví dụ của mình là trong thư mục `C:\Users\quatp\.hyper.js`) và thay thế dòng 
{% highlight Shell %}
shell: '',
{% endhighlight %}
bằng
{% highlight Shell %}
shellArgs: ['--login'],
{% endhighlight %}
và 
{% highlight Shell %}
shell: 'C:\\Windows\\System32\\cmd.exe',
{% endhighlight %}
bằng 
{% highlight Shell %}
shellArgs: ['--login', '-i', '/c wsl'],
{% endhighlight %}

Bây giờ mỗi khi bạn mở Hyper termial, nó sẽ sử dụng `zsh` làm môi trường shell mặc định. Và chúng ta có Hyper termial trông như sau:

![Smithsonian Image]({{ site.url }}/img/Hyper-Terminal-Without-Theme.png)
{: .pull-left}

Theme và các plugins cho Hyper Terminal bạn có thể tìm thấy ở [đây](https://github.com/bnb/awesome-hyper). Mình sử dụng [hyper-material-theme](https://github.com/equinusocio/hyper-material-theme) và có được:

![Smithsonian Image]({{ site.url }}/img/Bash-Ubuntu-Win10.png)
{: .pull-right}

## Thay đổi Oh My Zsh Theme
Danh sách Oh My Zsh theme bạn có thể tìm thấy ở [đây](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes). Mặc định oh-my-zsh sử dụng theme robbyrussell. Nếu bạn muốn thay đổi theme, mở `~/.zshrc` và thay đổi tên "robbyrussell" là theme bạn muốn sử dụng.

## Cài đặt zsh-syntax-highlighting plugin
Mở terminal và download `zsh-syntax-highlighting` plugin bằng lệnh:
{% highlight Command%}
  
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
{% endhighlight %}
Nếu biến `$ZSH_CUSTOM` tồn tại và chứa giá trị thì sử dụng nó luôn, nếu không sử dụng `~/.oh-my-zsh/custom`. Để active plugin, mở file `.\zshrc` và tìm đến dòng sau:
{% highlight Shell %}
# Which plugins would you like to load? (plugins can be found in ~/.oh-my-zsh/plugins/*)
# Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
# Example format: plugins=(rails git textmate ruby lighthouse)
# Add wisely, as too many plugins slow down shell startup.
plugins=(git)
{% endhighlight %}
Sau đó thay dòng `plugins=(git)` bằng:
{% highlight Shell %} 
plugins=(git zsh-syntax-highlighting)
{% endhighlight %}
Save lại. Cuối cùng thực hiện lệnh:
{% highlight Command %} 
source ~/.zshrc
{% endhighlight %}
Restart terminal và chúng ta có thể thấy kết quả 😍.

![Smithsonian Image]({{ site.url }}/img/Hyper-Terminal-With-Theme.png)
{: .pull-left}

Bạn có thể khai báo các alias trong file `~/.zshrc`.



