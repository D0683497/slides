# Python 環境建置

---

## 下載 Python

----

首先 先去官網下載 Python 3.6.6 (64位元版本)

![](https://i.imgur.com/EFQSis5.png)

選取 Windows x86-64 executable installer

----

[或點我直接下載](https://www.python.org/ftp/python/3.6.6/python-3.6.6-amd64.exe)

---

## 開始安裝 Python

----

**記得一定要勾起 Add Python 3.6 to PATH !!!**

![](https://i.imgur.com/yuOGdxh.png)

----

點選 Install Now 然後點選"是"後 等待安裝至成功

----

如果有出現 Disable path length limit

![](https://i.imgur.com/8pEXDOX.png)

點選 Disable path length limit 點選 2 次"是"後 
即可按下 close 關閉安裝 安裝完成

----

如果沒出現 Disable path length limit

則可直接 按下 close 關閉安裝 安裝完成

----

### **到目前有問題都可以舉手**

---

## 環境變數 (PATH)

----

### 環境變數 是什麼?

----

羅列出 shell 搜尋 用戶 輸入的執行命令所在的目錄

簡單來說如果環境變數沒設定好

電腦就找不到該去哪裡執行了

![](https://i.imgur.com/TafsMav.png)

----

### PATH 設定教學

----

設定 環境變數 前
得先找好 Python 的路徑

----

#### Python路徑尋找

----

在開始列搜尋 "Python" 找到 並右鍵

<img src="https://i.imgur.com/xylYMzk.png" width="32%" height="32%">

----

開起檔案位置

<img src="https://i.imgur.com/hC5Mpdr.png" width="32%" height="32%">

----

進入到程式目錄 找到 Python3.6(64-bit) 右鍵 "內容"

<img src="https://i.imgur.com/GywLeUw.png" width="80%" height="80%">

----

選取 "捷徑" 複製 "開始位置" 及為 環境變數該新增的路徑

<img src="https://i.imgur.com/0rWqzj3.png" width="38%" height="38%">

----

#### 環境變數設定

----

首先 到桌面 按下你的 Win 鍵

<img src="https://i.imgur.com/wrHmouG.png" width="53%" height="53%">

----

輸入 "環境變數"

<img src="https://i.imgur.com/x75lUju.png" width="33%" height="33%">

----

點選 "進階"

<img src="https://i.imgur.com/VnYbPsp.png" width="52%" height="52%">

----

點選 "環境變數"

<img src="https://i.imgur.com/8fxaCt9.png" width="52%" height="52%">

----

選擇 "Path" 然後按 "編輯"

<img src="https://i.imgur.com/yV8cyxQ.png" width="60%" height="60%">

----

點選 "新增"

<img src="https://i.imgur.com/s35nuEk.png" width="60%" height="60%">

----

把 Python 的路徑加進去 

路徑大家不一定相同 此處填入剛剛尋找到的路徑

<img src="https://i.imgur.com/ZlHuQcZ.png" width="50%" height="50%">

----

此外這邊應填入之路徑還有除了

"......\Python\Python36\" 以外

----

為了使 pip(晚點會提到) 也加入環境變數

需也把 "......\Python\Python36\" 底下之 "\Scripts\" 也加入

----

應加入變數路徑為

"......\Python\Python36\"

"......\Python\Python36\Scripts\"

----

確認添加兩個變數路徑後 按 "確定" 離開

<img src="https://i.imgur.com/xQXHsSN.png" width="60%" height="60%">

---

## 安裝 pip

----

### pip 是什麼 ?

----

pip是一個以Python寫成的軟體包管理系統

簡單來講pip可以幫你安裝python的插件

----

各位很幸福 Python 3.6 已經幫你包好了

不然之前都是要另外安裝

----

### pip 安裝方式 

----

點擊 [get-pip.py](https://bootstrap.pypa.io/get-pip.py) 並 "右鍵" "另存新檔"
![](https://i.imgur.com/BgPO9mr.png)

----

選擇下載路徑(待會要開起它)
![](https://i.imgur.com/YKe8qRK.png)

----

開啟有 [get-pip.py](https://bootstrap.pypa.io/get-pip.py) 的資料夾
![](https://i.imgur.com/YPdf7dE.png)

----

進入資料夾後 按住 "shift" 並 "右鍵" 開啟 "PowerShell"
![](https://i.imgur.com/RdVZScf.png)

----

執行 [get-pip.py](https://bootstrap.pypa.io/get-pip.py) 檔
![](https://i.imgur.com/RV5bfyr.png)

```shell=
python get-pip.py
```

----

看到 Successfully installed pip 就代表成功安裝了
![](https://i.imgur.com/xCs74fO.png)


---

### pip 基本語法

----

打開 cmd (命令提示視窗)

![](https://i.imgur.com/SOZmhvp.png)

----

然後輸入`pip`

![](https://i.imgur.com/QP0Ny5z.png)

----

你會看到他的基本語法是

`pip <command> [option]`

command 跟 option要打什麼下面都有列出來

option 要不要打都可以

----

基本上社課只會用到安裝的功能而已

+ 看pip的版本
    + `pip -V` 
    + 注意是大寫的V
+ 安裝插件
    + `pip install 插件名稱`
+ 移除插件
    + `pip uninstall 插件名稱`
+ 看你安裝的全部插件
    + `pip freeze`
    + `pip list`

---

## 安裝 jupyter notebook

----

### jupyter notebook 是什麼 ?

----

Jupyer Notebook（以前稱為IPython notebook）

是一個介於IDE(Pycharm, Spider)以及Editor(Sublime text, Atom, VScode, 記事本)之間的一個讓你可以寫code的工具

**簡單來講可以用他寫code跟執行啦**

----

### 如何安裝 jupyter notebook

----

打開 cmd (命令提示視窗)
![](https://i.imgur.com/SOZmhvp.png)

----

cmd 打開長這樣
![](https://i.imgur.com/NHMAeRD.png)

----

對 cmd 下

```shell=
pip install jupyter notebook
```

----

中間會跑一堆長這樣的東西

![](https://i.imgur.com/nTBvQjK.png)

直到最後停止出現 Successfully......

----

### **到目前有問題都可以舉手**
-----
剛剛有出現 <font face="微軟正黑體" color=red>紅字</font> 或 <font face="微軟正黑體" color=yellow>黃字</font> 的請舉手

---

## 開啟 jupyter notebook

----

好 那現在再開啟 cmd (忘了怎麼開 自己去看前面)

----

對 cmd 下
``` shell=
jupyter notebook
```

----

然後就會在 cmd 看到這個畫面
![](https://i.imgur.com/VnTLfda.png)

----

同時你的預設瀏覽器會打開到這個畫面

<table>
    <tr>
        <th align="center">chrome 版本</th>
        <th align="center">ie 版本</th>
    </tr>
    <tr>
        <td align="center"><img src="https://i.imgur.com/5tyZ9Kz.png" width="80%" height=""></td>
        <td align="center"><img src="https://i.imgur.com/BgC2E6m.png" width="" height=""></td>
    </tr>
</table>

----

如果沒有出現 回到 cmd 找到
![](https://i.imgur.com/11Pwclj.png)
複製下方的網址貼到瀏覽器
(開頭是 http://localhost:8888/ 的那串)

---

## Python 版 "Hello world"

----

把檔案建在你要的地方(舉例：Desktop 桌面)
![](https://i.imgur.com/y76iNi1.png)
點進去~~~

----

點選 New 選擇 Python 3
![](https://i.imgur.com/kwVgszZ.png)

----

操作介面介紹
![](https://i.imgur.com/C6FwQAU.png)

----

檔名改成 Hello World 

程式碼：

```shell=
print("Hello World !!!")
```

----

然後 Run

或是按 ctrl+enter

![](https://i.imgur.com/tpLzHDa.png)

----

恭喜你(妳)學會了 Python

----

的萬分之一了

請繼續加油 社課記得都要來ㄛ

P.S. 還沒繳社費的 可以繳一下 謝謝!!!

----

![](https://i.imgur.com/j6jqY2P.png)

---

## 補充介紹
-----
### VS Code

----

VS Code 全名 Visual Studio Code

由微軟開發的**文字編輯器**

但他可以安裝很多擴充的功能

讓他也可以編譯

內建了 Git(版本控制)、代碼補全...

很多功能

----

但社課不會用到他

因為社課要做的事還蠻簡單的

所以用不到他

不過還是介紹一下

----

![](https://i.imgur.com/RfMiZmn.png)

[想下載的可以下載](https://code.visualstudio.com/docs/?dv=win)

---

## 補充介紹
-----
### Anaconda

----

![](https://i.imgur.com/CIWYKDP.png)

這是一個對新手很友善的 coding 環境

但 他很肥大 肥\~\~\~\~\~\~

----

他把很多你可能用到的功能直接包進去

但

其實你用不到

----

剛剛上面課程講到的東西你只需要下載並安裝他就好了

[Anaconda 官網載點](https://www.anaconda.com/download/)

----

下載 Python 3.6 version(64-Bit)

----

裝好你會得到

![](https://i.imgur.com/hzqVPWE.png)

開啟 jupyter notebook 只要點下去就好

----

Ancounda Prompt 

你可以把它當成 Ancounda 的 cmd

Spyder 也是一個可以 coding 的地方

----

大概這樣~~~
