---
layout: default
---

# 維護mail server

- 這篇只是廢文跟murmur請跳過

## 開頭一定抱怨

阿我們的mail server是多久沒修CVE出來也不會更新

我這屆處理，然後它的版本又不正確我是要怎樣

sender count 裡面有超級劣質的code 我也不知到如何設計成那樣的不要問我

## mail server 問題

1. 垃圾郵件送出無法以數量截攔
2. sender count (郵件計數)無法正常運作
3. mail server年久失修無更新極有可能有漏洞

## 垃圾郵件

啊就某老師被盜帳號

然後我要一直停權復權是怎樣我的問題ㄛ

之後我還要用policyd 真的血汗勞工

## sender count


shell script寫的

我有修正他連送出失敗都可以過的東西拉

不過變得比較慢QQ

不過cron是寫在root極度有可能利用他來提權

方法如下
1. 利用bounce丟東西給maillog
2. 繞過sed的偵測
3. 直接注入code給sed參數即可取得mail的root權限

~~拜託不要亂打我們伺服器雖然反正2個月就會消失ㄌ~~

## postfix dovecot

阿贛我按到pkg自動更新

阿贛我按到pkg更新

~~我好棒~~

然後因為不支援mysql的database

所以我就要port tree整個重裝

然後花了一天的時間

不過值得拉

被打CVE得不償失

~~被Ibilis講的我很怕~~

## 心得 

這是我高二第一次修mail server拉

希望之後不會2個月不會有問題

有好的開始就會是成功的一半

~~可是先森這不是一個好的開始ㄅ~~
