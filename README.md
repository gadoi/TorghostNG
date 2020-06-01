# Giới thiệu về TorghostNG
![TorghostNG now supports Privoxy](https://github.com/GitHackTools/Store-the-pictures/blob/master/TorghostNG%20%20Privoxy.png)

TorghostNG là một công cụ bạn kết nối Internet ẩn danh qua Tor.
TorghostNG Được gõ lại từ [TorGhost](https://github.com/SusmithKrishnan/torghost) với Python 3.

TorghostNG đã được chạy thử trên Kali Linux, Manjaro...

# Có gì mới ở TorghostNG 1.5
* Bản 1.5 lỗi quá nên có bản 1.5 để sửa lỗi thôi :smile:

# Trước khi bạn dùng TorghostNG
* Vì mạng Tor, iptables sẽ chặn các kết nối BitTorrent. Mặc dù bạn có thể "vượt rào" với phần cài đặt trong phần mềm torrent 😥 Rất khó để chặn hoàn toàn torrent.
* Vì lý do bảo mật, TorghostNG sẽ vô hiệu hóa IPv6 để ngăn ngừa IPv6 rò rỉ (mình bị dính chưởng rồi nè lmao).

# Cài đặt TorghostNG
Bộ cài đặt TorghostNG hiện đang hỗ trợ các bản phân phối Linux:
* Dựa trên Arch Linux
* Dựa trên Debian/Ubuntu
* Dựa trên Fedora, CentOS, RHEL, openSUSE
* [Solus OS](https://getsol.us)
* [Void Linux](https://voidlinux.org)
* Và bậc lão thành trong làng Linux: [Slackware](http://slackware.com)
* (Sao mà lắm trình quản lý gói thế :v)

Để cài đặt TorghostNG, bạn chỉ cần mở Terminal lên và gõ mấy câu lệnh sau:
    
    git clone https://github.com/gitkern3l/TorghostNG
    cd TorghostNG
    sudo python3 install.py
    sudo torghostng
    
Nhưng với Slackware, bạn phải gõ `sudo python3 torghostng.py` để chạy TorghostNG :v

# Cách cập nhật TorghostNG
Bạn chỉ cần gõ `torghostng -u` để TorghostNG tự động cập nhật thôi, nhưng nó sẽ tải TorghostNG mới về thư mục `/root` đó, vì bạn phải chạy TorghostNG với quyền root mà. Nếu bạn không muốn vậy thì bạn có thể vô thư mục mà bạn tải TorghostNG về và gõ `git pull -f` và `sudo python3 install.py` thôi.

# Trợ giúp
    CÁC LỰA CHỌN:
      -h, --help       Hiển thị phần trợ giúp và thoát
      -s, --start      Bắt đầu kết nối đến mạng Tor
      -x, --stop       Ngưng kết nối đến mạng Tor
      -r, --renew      Thay đổi mạch Tor
      -id ID QUỐC GIA  Thay đổi địa chỉ IPv4 sang một quốc gia cụ thể. Vô CountryCode.org để xem ID
      -mac INTERFACE   Thay đổi ngẫu nhiên địa chỉ MAC. Dùng lệnh 'ifconfig' để xem các interface
      -c, --checkip    Xem địa chỉ IP hiện tại
      --dns            Dùng cái này để sửa vấn đề về DNS
      -l, --language   Thay đổi ngôn ngữ hiển thị. Tiếng Anh là mặc định
      --list           Hiển thị danh sách các ngôn ngữ hiện có
      -u, --update     Kiểm tra cập nhật
      --nodelay        Tắt hiệu ứng thời gian đi`

Bạn cũng có thể dùng nhiều lựa chọn cùng lúc như:
* `torghostng -s -m INTERFACE`: đổi địa chỉ MAC trước khi kết nối
* `torghostng -c -m INTERFACE`: kiểm tra địa chỉ IP và thay địa chỉ MAC
* `torghostng -s -x`: kết nối đến Tor rồi ngưng luôn :v
* ...

Nếu bạn còn có thắc mắc nào khác thì xem [video hướng dẫn sử dụng](https://bit.ly/34TNglL) nè 🙂

Hy vọng các bạn sẽ yêu video hướng dẫn đó 😃

# Lưu ý
Mạng TOR không thể giúp bạn hoàn toàn ẩn danh, chỉ giúp bạn gần như hoàn toàn thôi:
* [Tor’s Biggest Threat – Correlation Attack](https://theonionweb.com/2016/10/25/tors-biggest-threat-correlation-attack)
* [Is Tor Broken? How the NSA Is Working to De-Anonymize You When Browsing the Deep Web](https://null-byte.wonderhowto.com/how-to/is-tor-broken-nsa-is-working-de-anonymize-you-when-browsing-deep-web-0148933)
* [Use Traffic Analysis to Defeat Tor](https://null-byte.wonderhowto.com/how-to/use-traffic-analysis-defeat-tor-0149100)
* ...

Bạn nên cài [NoScript](https://noscript.net) trước khi lướt web với TOR. NoScript sẽ chặn các đoạn mã JavaScript/Java/Flash trên các trang web để đảm bảo chúng sẽ không làm lộ danh tính thật của bạn

# Và làm ơn
* **Đừng spam hay tấn công DoS qua Tor.** Làm vậy không hiệu quả và chỉ làm Tor bị ghét.
* **Đừng tải torrent qua Tor.** Điều này không hay tẹo nào, tải torrent qua Tor phá vỡ tính ẩn danh và làm tiêu tốn tiền bạc của các tình nguyện viên mạng Tor. Nếu bạn muốn giữ ẩn danh khi tải torrent thì dùng VPN hoặc là proxy nhé nhé.

[Bittorrent over Tor isn't a good idea](https://blog.torproject.org/bittorrent-over-tor-isnt-good-idea)

![Don't torrent over Tor, please](https://github.com/GitHackTools/Store-the-pictures/raw/master/Đừng%20torrent%20qua%20tor%20mà%20-%20Hilda%20meme.png)

# Nhật ký thay đổi
Phiên bản 1.5
* Sửa lỗi của phiên bản 1.4

Phiên bản 1.4
* Hỗ trợ kết nối mạng Tor với Privoxy

Phiên bản 1.3
* Sửa lỗi

Phiên bản 1.2
* Sửa lỗi `update_commands` và vài thứ trong [torghostng.py](https://github.com/gitkern3l/TorghostNG/blob/master/torghostng.py)
* Thay đổi vài thứ trong [`theme.py`](https://github.com/gitkern3l/TorghostNG/blob/master/torngconf/theme.py)
* Thay đổi vài thứ trong [`install.py`](https://github.com/gitkern3l/TorghostNG/blob/master/install.py)
* Hỗ trợ đổi mạch Tor với `-r`

Phiên bản 1.1
* Có kiểm tra IPv6
* Thay "TOR" bằng "Tor"
* Chặn kết nối BitTorrent
* Tự động vô hiệu hóa IPv6 trước khi kết nối đến Tor

# Một vài hình ảnh về Torghost (bản 1.0)
* Cài đặt ngôn ngữ: `torghostng -l`

![Setting language on TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/Cài%20đặt%20ngôn%20ngữ%20cho%20TorghostNG.png)

* Kiểm tra địa chỉ IP: `torghostng -c`

![Checking IP address with TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/Kiểm%20tra%20địa%20chỉ%20IP%20với%20TorghostNG.png)

* Thay đổi địa chỉ MAC: `torghostng -m INTERFACE`

![Changing MAC address with TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/Thay%20%C4%91%E1%BB%95i%20%C4%91%E1%BB%8Ba%20ch%E1%BB%89%20MAC%20v%E1%BB%9Bi%20TorghostNG.png)

* Ngắt kết nối khỏi mạng Tor: `torghostng -x`

![Disconnecting from Tor network with TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/Torghost%20ng%E1%BA%AFt%20k%E1%BA%BFt%20n%E1%BB%91i%20kh%E1%BB%8Fi%20m%E1%BA%A1ng%20TOR.png)

* Chọn điểm thoát Tor ở quốc gia cụ thể: `torghostng -id COUNTRY ID`

![Connecting to Tor exitnode in a specific country](https://github.com/GitHackTools/Store-the-pictures/raw/master/TorghostNG%20k%E1%BA%BFt%20n%E1%BB%91i%20%C4%91%E1%BA%BFn%20Vi%E1%BB%87t%20Nam.png)

# To-do lists
* Chặn bỏ xừ torrent, vì mạng Tor
* Hỗ trợ IPv6 (có được không?)
* Có giao diện người dùng cuối
* Sửa lỗi, cải thiện TorghostNG (luôn luôn rồi)
