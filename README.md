# TUNet CLI

version 0.2.0

by 思無邪SyiMyuZya

----

清華校園網命令行版用戶認證工具。

用於無圖形界面之環境。可顯示當前在線狀態、登入登出校園網。

需要python2(>=2.6)以執行。

1.  顯示在線狀態

    ```sh
    ./tunetctl
    ```

2.  登入

    ```sh
    ./tunetctl -l  # （提示輸入用戶名、密碼）

    # 登錄並保存用戶信息到指定文件
    ./tunetctl -s user.txt

    # 使用文件保存的用戶信息：
    ./tunetctl -f user.txt

    # 使用默認文件（~/.tunet）登入
    ./tunetctl -d
    ```

3.  登出

    ```sh
    ./tunetctl -o
    ```

4.  顯示幫助

    ```sh
    ./tunetctl -h
    ```

----

### TODO

* [x] 支持新版協議
* [x] 用文件保存/讀取用戶名與密碼（md5散列值）
* [ ] ~~重構選項解析部分的代碼，用argparse替代getopt~~
* [ ] 處理網絡異常
* [ ] ~~將服務器原始錯誤信息改為提示信息（新協議原始信息已經足夠）~~
* [ ] 多語言（不一定實作…因為無圖形界面時貌似不需要多語言？）
