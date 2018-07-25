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

* Restart máy tính khi xong.

### Cài đặt Ubuntu trên Microsoft Store



## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

### Body text

Lorem ipsum dolor sit amet, test link adipiscing elit. **This is strong**. Nullam dignissim convallis est. Quisque aliquam.

![Smithsonian Image]({{ site.url }}/img/Bash-Ubuntu-Win10.png)
{: .pull-right}

*This is emphasized*. Donec faucibus. Nunc iaculis suscipit dui. 53 = 125. Water is H2O. Nam sit amet sem. Aliquam libero nisi, imperdiet at, tincidunt nec, gravida vehicula, nisl. The New York Times (That’s a citation). Underline.Maecenas ornare tortor. Donec sed tellus eget sapien fringilla nonummy. Mauris a ante. Suspendisse quam sem, consequat at, commodo vitae, feugiat in, nunc. Morbi imperdiet augue quis tellus.

HTML and CSS are our tools. Mauris a ante. Suspendisse quam sem, consequat at, commodo vitae, feugiat in, nunc. Morbi imperdiet augue quis tellus. Praesent mattis, massa quis luctus fermentum, turpis mi volutpat justo, eu volutpat enim diam eget metus.

### Blockquotes

> Lorem ipsum dolor sit amet, test link adipiscing elit. Nullam dignissim convallis est. Quisque aliquam.

## List Types

### Ordered Lists

1. Item one
   1. sub item one
   2. sub item two
   3. sub item three
2. Item two

### Unordered Lists

* Item one
* Item two
* Item three

## Tables

| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|----
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=====
| Foot1   | Foot2   | Foot3
{: rules="groups"}

## Code Snippets

{% highlight css %}
#container {
  float: left;
  margin: 0 -240px 0 0;
  width: 100%;
}
{% endhighlight %}

## Buttons

Make any link standout more when applying the `.btn` class.

{% highlight html %}
<a href="#" class="btn btn-success">Success Button</a>
{% endhighlight %}

<div markdown="0"><a href="#" class="btn">Primary Button</a></div>
<div markdown="0"><a href="#" class="btn btn-success">Success Button</a></div>
<div markdown="0"><a href="#" class="btn btn-warning">Warning Button</a></div>
<div markdown="0"><a href="#" class="btn btn-danger">Danger Button</a></div>
<div markdown="0"><a href="#" class="btn btn-info">Info Button</a></div>

## Notices

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice}
