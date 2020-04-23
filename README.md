# Giới thiệu về TorghostNG
TorghostNG là một công cụ bạn kết nối Internet ẩn danh qua TOR.
TorghostNG Được gõ lại từ [TorGhost](https://github.com/SusmithKrishnan/torghost) bằng Python 3.

TorghostNG đã được chạy thử trên Kali Linux, Manjaro...

# Cài đặt TorghostNG
Bộ cài đặt TorghostNG hiện đang hỗ trợ các bản phân phối Linux:
* Dựa trên Arch Linux
* Dựa trên Debian/Ubuntu
* Dựa trên Fedora, CentOS, RHEL, openSUSE
* [Solus OS](https://getsol.us)
* [Alpine Linux](https://alpinelinux.org)
* [OpenWrt Linux](https://openwrt.org)
* [Void Linux](https://voidlinux.org)
* Và bậc lão thành trong làng Linux: [Slackware](http://slackware.com)
* (Sao mà lắm trình quản lý gói thế :v)

Để cài đặt TorghostNG, bạn chỉ cần mở Terminal lên và gõ mấy câu lệnh sau:
    
    git clone https://github.com/gitkern3l/TorghostNG
    cd TorghostNG
    sudo python3 install.py
    sudo torghostng
    
Nhưng với Slackware, bạn phải gõ `sudo python3 torghostng.py` để chạy TorghostNG :v

# Trợ giúp
    TorghostNG 1.0 - Giúp bạn kết nối Internet ẩn danh qua TOR
    Được gõ lại từ TorGhost bằng Python 3
    usage: torghostng [-h] -s|-x|-id|-m|-c|-l|--list
    CÁC LỰA CHỌN:
    -h, --help       Hiển thị phần trợ giúp và thoát
    -s, --start      Bắt đầu kết nối đến mạng TOR
    -x, --stop       Ngưng kết nối đến mạng TOR
    -id ID QUỐC GIA  Thay đổi địa chỉ IP sang một quốc gia cụ thể. Vô CountryCode.org để xem ID
    -mac INTERFACE   Thay đổi ngẫu nhiên địa chỉ MAC. Dùng lệnh 'ifconfig' để xem các interface
    -c, --checkip    Xem địa chỉ IP hiện tại
    --nodelay        Tắt hiệu ứng thời gian đi
    -l, --language   Thay đổi ngôn ngữ hiển thị. Tiếng Anh là mặc định
    --list           Hiển thị danh sách các ngôn ngữ hiện có
    -u, --update     Kiểm tra cập nhật
    --dns            Dùng cái này để sửa vấn đề về DNS`

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

![Don't torrent through Tor, please](https://github.com/GitHackTools/Store-the-pictures/raw/master/Đừng%20torrent%20qua%20tor%20mà%20-%20Hilda%20meme.png)

# Một vài hình ảnh về Torghost
* Cài đặt ngôn ngữ: `torghostng -l`

![Setting language on TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/Cài%20đặt%20ngôn%20ngữ%20cho%20TorghostNG.png)

* Kiểm tra địa chỉ IP: `torghostng -c`

![Checking IP address with TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/Kiểm%20tra%20địa%20chỉ%20IP%20với%20TorghostNG.png)

* Thay đổi địa chỉ MAC: `torghostng -m INTERFACE`

![Changing MAC address with TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/Thay%20%C4%91%E1%BB%95i%20%C4%91%E1%BB%8Ba%20ch%E1%BB%89%20MAC%20v%E1%BB%9Bi%20TorghostNG.png)

* Ngắt kết nối khỏi mạng TOR: `torghostng -x`

![Disconnecting from Tor network with TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/Torghost%20ng%E1%BA%AFt%20k%E1%BA%BFt%20n%E1%BB%91i%20kh%E1%BB%8Fi%20m%E1%BA%A1ng%20TOR.png)

* Chọn điểm thoát TOR ở quốc gia cụ thể: `torghostng -id COUNTRY ID`

![Connecting to TOR exitnode in a specific country](https://github.com/GitHackTools/Store-the-pictures/raw/master/TorghostNG%20k%E1%BA%BFt%20n%E1%BB%91i%20%C4%91%E1%BA%BFn%20Vi%E1%BB%87t%20Nam.png)
