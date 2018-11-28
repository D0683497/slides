# Regular Expression

---

練習網站

http://www.rubular.com/

---

Hellow world.

`w` 

Hello<span style="color:red;">w</span> <span style="color:red;">w</span>orld.

---

Hellow world.

`low`

Hel<span style="color:red;">low</span> world.

---

`.`

代表任意字元

(不包含`\n`)

----

Hellow world.

`o.`

Hell<span style="color:red;">ow</span> w<span style="color:red;">or</span>ld.

---

`[ ]`

選多個字元

----

Hackersir

`[abcdefgh]`

H<span style="color:red;">ac</span>k<span style="color:red;">e</span>rsir

----

Hackersir

`[a-h]`

H<span style="color:red;">ac</span>k<span style="color:red;">e</span>rsir

---

`^`

代表不要

注意:在`[ ]`裡面才是

----

Hackersir

`[^a-h]`

<span style="color:red;">H</span>ac<span style="color:red;">k</span>e<span style="color:red;">rsir</span>

---

縮寫

+ `\d` = `[0-9]`
+ `\w` = `[A-Za-z0-9_]` 注意有底線
+ `\s` = `[\t\s\r]` 
+ `\D` = `[^\d]`
+ `\W` = `[^\w]`
+ `\S` = `[^\s]`

---

`*`

代表任意次數

----

Hackersir

`c.*`

Ha<span style="color:red;">ckersir</span>

---

`+`

代表至少一次

----

banana

`n+a`

ba<span style="color:red;">nana</span>

---

`?`

代表零或一次

----

banana

`n?a`

b<span style="color:red;">anana</span>

---

`|`

或

----

iOS and android

`and|android`

iOS <span style="color:red;">and and</span>roid

----

`android|and`

iOS <span style="color:red;">and android</span>

---

`^`

開頭

----

hello hello

`^he`

<span style="color:red;">he</span>llo hello

---

`$`

結尾

----

hello hello

`llo$`

hello he<span style="color:red;">llo</span>

---

`{次數}`

`{最少次數, 最多次數}`


----

Hello world.

`l{2}`

He<span style="color:red;">ll</span>o world.

----

Hello world.

`l{1,}`

He<span style="color:red;">ll</span>o wor<span style="color:red;">l</span>d.

---

# python 實作

---

```python
import re
```

---

線上的python編譯器

https://repl.it/repls/OffensiveDualRelationaldatabase

---

```python
re.search(正則表達式, 字, (flags))
```

掃描整個字串，return第一個成功的

----

| flag | 說明 |
| -------- | -------- |
| re.I | 忽略大小寫 |
| re.L | 表示特殊字符 |
| re.M | 多行模式 |
| re.S | 讓 \. 包含換行 |
| re.U | 表示特殊字符 |
| re.X | 忽略空格和註解 |

----

`group( )`

`groups( )`

----

```python=
import re

s = '123asd789'
m = re.search("([0-9]*)([a-z]*)([0-9]*)",s)

print(m.groups())
print(m.group())
print(m.group(1))
print(m.group(2))
print(m.group(3))
```

----

>('123', 'asd', '789') 

>123asd789 

>123 

>asd 

>789

---

```python
re.match(正則表達式, 字, (flags))
```

從第一個字開始，return第一個成功的

----

```python
re.fullmatch(正則表達式, 字, (flags))
```

從第一個字開始，全部成功才return

---

```python
re.findall(正則表達式, 字, (flags))
```

掃描整個字串，return一個list

----

```python=
import re

s = "hello hello"
m = re.findall("l", s)

print(m)
```
>['l', 'l', 'l', 'l']

---

```python
re.sub(正則表達式, 要換的字, 原本的字, (更換次數), (flags))
```

掃描整個字串，並替換

----

```python=
import re

s = "hello hello"
m = re.sub("[hl]", 'w', s, 3)

print(m)
```
>wewwo hello

---

# 練習

---

## 練習第一題

字串:Minions love banana.

輸出:['ni', 'ns'] 

----

解答：
```python=
import re

s = 'Minions love banana.'
m = re.findall("n[is]", s)
print (m)
```

---

## 練習第二題

驗證身分證格式是否正確(不須驗證內容)

身份證字號格式:
第一碼:A-Z(大寫英文)
第二碼:1(男)或2(女)
後八碼:0-9(數字)

**不要給我用一堆if硬幹**

----

範例:

![](https://i.imgur.com/ZbsIe5E.png)

----

解答：

```python=
import re
while (1):
    s = input('請輸入身份證字號:')
    o = re.fullmatch("^[A-Z][12][0-9]{8}$", s)
    if s == 'end':
        break
    elif s != None:
        print('Ture')
    else:
        print('False')
```

---

## 練習第三題

驗證email格式

email格式:
英文或數字 + @ + 英文.英文(.英文)

----

範例:

![](https://i.imgur.com/gJxIqzU.png)

----

解答：

```python=
import re

while (1):
    s = input('請輸入email:')
    o = re.fullmatch("[a-zA-Z0-9]*\@[a-z]*\.[a-z]*\.?[a-z]{0,}", s)
    if s == 'end':
        break
    elif o != None:
        print('Ture')
    else:
        print('Flase')
```

---

## 練習第四題

請輸入一個由a、b、c組成的字串

並判別a是否出現偶數次

----

解答：

```python=
import re

a = input('輸入:')
b = re.findall('a', a)
if len(b) % 2 == 0:
    print('Ture')
else:
    print('False')
```

---

## 練習第五題

請輸入一個由a、b、c組成的字串

並判別不含子字串ab

----

解答：

```python=
import re

a = input('輸入:')
b = re.findall('ab', a)
if len(b) == 0:
    print('Ture')
else:
    print('Flase')
```

---

## 練習第六題

請輸入二進制數，並判別是否為4的倍數

(用re.match寫)

----

解答：

```python=
import re

text = input("請輸入二進制數，並判別是否為4的倍數：\n")

if re.match(r'^1[01]*00$',text):
    print('True')
else:
    print('Flase')
```

---

## 練習第七題

修改html的標籤

用visual studio code 

把`<p></p>`改成`<h3></h3>`

----

```html
<!DOCTYPE html>
<html>
<body>

<div style="background-color:black;color:white;padding:20px;">
  <h2>London</h2>
  <p>Hello</p>
  <p>asdfg</p>
</div> 

</body>
</html>
```

---

## 練習第八題

黑客社CTF

https://ctf.hackersir.org

----

![](https://i.imgur.com/21UGExp.png)

---

## 補充

## sscanf( )

---

`%8s`

讀8個字

---

`%[^字元]`

到這個字元為止

---

`%[1-9]`

只讀1到9

---

`%*`

捨棄掉

---

```c=
#include<stdio.h>

int main(){
	int a, b;
    
	sscanf("-70x^8", "%dx%*1s%d", &a, &b);
	printf("%d\n%d", a, b);
    
	return 0;
} 
```

>-70
<br>
>8

---

影片網址：

https://youtu.be/vYGERshoBdQ

---