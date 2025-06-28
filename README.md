# Laravel 12 輕量且注重隱私的產品分析

引入 panphp 的 pan 套件來擴增輕量且注重隱私的產品分析，僅追蹤曝光次數、懸停次數和點擊次數事件，不會收集任何個人資訊息，例如 IP 位址、使用者代理或任何可識別個人的任何資訊。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __Artisan__ 指令的 __migrate__ 來執行所有未完成的遷移，並執行資料庫填充（如果要測試的話）。
```sh
$ php artisan migrate --seed
```
- 執行 __Artisan__ 指令的 __pan__ 來執行視覺化您的產品分析。
```sh
$ php artisan pan
```
- 在瀏覽器中輸入已定義的路由 URL 來訪問，例如：http://127.0.0.1:8000。
- 你可以經由 `/login` 來進行登入，預設的電子郵件和密碼分別為 __admin@admin.com__ 和 __password__ 。

----

## 畫面截圖
![](https://i.imgur.com/keoxoC7.png)
> 尚未記錄任何分析

![](https://i.imgur.com/qNB1vkX.png)
> 看到使用者和網站內容項目的互動頻率
