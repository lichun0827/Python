:::success
[TOC]
:::

# **Python**
<div align="justify">
Python 易於撰寫且應用廣泛，可用於資料分析、網頁開發、機器學習等多個領域。
</div>

# 1. 安裝 Python
<div align="justify">
1. 進入 <a href="https://www.python.org/">Python 官網</a>，點擊**Download**，選擇最新版本並下載。<br>
2. 打開下載的檔案，勾選 <strong>Add Python.exe to PATH</strong>，然後點擊 <strong>Install Now</strong>。<br>
3. 等待安裝完成。
</div>

# 2. 安裝 PyCharm Community 版
<div align="justify">
PyCharm 是一個整合開發環境（IDE），用來撰寫和執行 Python 程式碼。<br><br>
1. 搜尋 <strong>PyCharm</strong> 並進入官網的下載頁面。<br>
2. 下載 <strong>Community 版</strong>，右鍵點擊下載的檔案，選擇「以系統管理員身分執行」。<br>
3. 安裝時，如圖所示：<br>
   - 勾選 <strong>Create desktop shortcut</strong>（建立桌面捷徑）。<br>
   - 勾選 <strong>Add PyCharm to PATH</strong>（將 PyCharm 加入 Windows 環境變數）。<br>
   - 勾選 <strong>Associate .py files</strong>（將 .py 檔案與 PyCharm 關聯）。<br>
4. 其餘步驟使用預設設定安裝。
</div>

![1](https://github.com/lichun0827/Python/blob/main/rkz7OLZDJx%5B1%5D.png%3D50%2525x)


# 3. 撰寫程式
<p style="text-align: justify;">
    打開 PyCharm，並新建一個專案<strong>(New Project)</strong>，<br>
    在創建專案時，會看到一個選項為「Create a main.py welcome script」，問是否要建立一個<strong>main.py</strong>檔案。這時的選擇取決於專案的複雜程度：
</p>

![image](https://hackmd.io/_uploads/B1Bl_8Wwyx.png=50%x)

<p style="text-align: justify;">
    藍色部分為<strong>專案名稱</strong>，圖中有一個「Create a main.py welcome script」選項，問是否要建立一個<strong>main.py</strong>檔案。如果你不建立 `main.py` 檔案，對於簡單的專案來說，可能不會有太大影響，但如果專案逐漸變得複雜，擁有一個 `main.py` 檔案會讓程式結構更清晰且易於管理。`main.py` 通常是專案的進入點，負責啟動程式，並且可以統一處理一些設定和流程邏輯。<br><br>
    如果專案有 `main.py`，這通常表示這個專案有多個程式檔或模組，而 `main.py` 是負責啟動整個專案流程的「主程式」。<br>
    在較複雜的專案中，為了讓程式碼更有組織，通常會將不同的功能或邏輯分散到多個檔案中。每個檔案（或稱為「模組」）通常包含一些特定的功能或類別，這樣便於重複使用和維護。例如，你可能會有：
    <ul>
        <li>`main.py`：專案的主程式，負責啟動整個專案，並可能引入其他模組執行主要的邏輯。</li>
        <li>`utils.py`：包含一些工具函式的檔案，提供程式中需要反覆使用的功能。</li>
        <li>`database.py`：負責處理資料庫操作的檔案。</li>
        <li> `models.py`：存放與數據模型相關的程式碼。</li>
    </ul>
    在這樣的結構中，`main.py` 就像是「引導者」，它會統籌整個專案的流程，並依序調用其他檔案中的程式碼。這樣可以讓專案更容易維護，也方便多人協作開發。<br>
    接下來按<strong>創建(Creat)</strong>。
</p>

![image](https://github.com/lichun0827/Python/blob/main/rkz7OLZDJx%5B1%5D.png%3D50%2525x)

<p style="text-align: justify;">
    接下來就可以建立新檔案撰寫第一支程式。右鍵目錄區剛設定的專案目錄，有兩種方式可創建python檔:
    <ol>
        <li>點選New>File，在跳出設窗中輸入檔案名稱(如 test.py或main.py)，需以<strong>.py</strong>結尾，之後按enter，就創建完成。</li>
        <li>點選New>Python File，在跳出設窗中輸入檔案名稱(如test或main)，再點選一次下方的Python File，按Enter，就創建完成.py的檔案。</li>
    </ol>
<br>
<p>在右方程式碼撰寫區，輸入print("Hello Python!")，表示輸出雙引號內的文字「Hello Python!」。接下來有三種方式可以執行Python程式指令:</P>
    <ol>
        <li>右鍵，點選「Run '專案名稱'」。</li>
        <li>按 Shift+F10。</li>
        <li>點擊右上角綠色箭頭</li>
        <li>當按下Alt+Shift+E，可以執行單行程式碼</li>
    </ol>
    當結果運算出現「Hello Python!」，就完成第一支程式碼了。</p>

![image](https://hackmd.io/_uploads/SkV3OwWPJg.png)

## 3-1. 變數和資料型別
變數是一個可重複使用的容器，用於儲存值。當我們在創建一個變數實，我們需要給他一個名稱，來表示所包含的內容

### 資料型別1: string 字串
>字串應使用 " 或 ' 包起來。透過 type() 可以查看資料型態，確認 name 是字串型態的變數，而 "我的名字是" 也是字串，因此可以直接相加。也可以使用 f-string 格式化方式，將非字串型態的變數嵌入字串中進行顯示。範例如下：
>```
># string 字串
>name = "Lili"
>print("我的名字是" + name)  # 直接相加
>print(f"我的名字是 {name}")  # f-string 格式化
>print(type(name))  # 查看資料型態
>```
>**output:**
>```
>我的名字是Lili
>我的名字是 Lili 
><class 'str'>
>```

### 資料型別2: Integer 整數
> height 是一個數值型整數變數，其資料型態為 integer，用來表示不帶小數點的數值。透過 type() 可以檢查變數型態，範例中 height 為整數型態。當要將整數與字串結合輸出時，需使用str() 轉換為字串型態，或者直接用 *f-string* 來格式化輸出。範例如下：
height為數值型整數變數，
>```
>##integer 整數
>height = 170
>print("我的身高是" + str(height) + "公分") # 使用 >str() 轉換型態
>print(f'我的身高是 {height} 公分')# f-string
>print(type(height))
>```
>**output:**
>```
>我的身高是170公分
>我的身高是 170 公分
><class 'int'>
>```
### 資料型別3: float 浮點數
>weight 是一個浮點數型變數，其資料型態為 float，用來表示帶有小數點的數值。透過 type() 可以檢查變數型態，範例中的 weight 為浮點數型態。浮點數通常用於需要精確表示非整數值的情境，例如測量數值或計算結果。範例如下：
>```
># float 浮點數
>weight = 52.5
>print(f"我的體重是 {weight} 公斤")  # 使用 f-string >格式化輸出
>print(type(weight))  # 查看變數型態
>```
>**output:**
>```
>我的體重是 52.5 公斤
><class 'float'>`
>```
### 資料型別4: boolean 布林值
>is_online 是一個布林值變數，其資料型態為 boolean，用來表示邏輯上的「真」或「假」。布林值只有兩個可能的值：True 或 False。範例如下：
>```
>## boolean 布林值 {true,false}
>is_online = True
>print(f"在嗎? {is_online}")
>print(type(is_online))
>```
>**output:**
>```
>在嗎? True
><class 'bool'>
>```
>布林值經常用在條件判斷，如檢查用戶是否在線、驗證密碼是否正確，或決定某段程式碼是否應執行。例如：
>```
>if is_online:
>    print("使用者目前在線。")
>else:
>    print("使用者離線。")
>```
>結果顯示為==使用者目前在線。==。
## 3-2. 資料型別轉換
型別轉換是將一個資料型別轉換成另ˋ種資料型別的過程。分為顯式型別轉換（Explicit Type Casting）與隱式型別轉換（Implicit Type Casting）。
### 顯式型別轉換（強制轉換變數型別）
> 變數的初始宣告，初始的型別如下:
>* name 為 字串 (str)
>* weight 為 整數 (int)
>* height 為 浮點數 (float)
>* student 為 布林值 (bool)
>進行顯示型別轉換
>1. float():將變數型別轉換成浮點數
>2. int():將變數型別轉換成整數，小數部分被截掉（不是四捨五入）。
>3. str():將變數型別轉換成字串
>4. bool():將變數型別轉換成布林值，(非空字串、非零數字皆為 True)。
>```
># 型別轉換 type cating
>name = "Lili"
>weight = 57
>height = 169.9
>student = True
>print(type(name))
>print(type(weight))
>print(type(height))
>print(type(student))
>
>## 顯示型別轉換
>weight = float(weight) #轉換成浮點數
>print(weight)
>print(type(weight))
>height = int(height) #轉換成整數(直接截掉小數部分)
>print(height)
>print(type(height))
>student = str(student) #轉換成字串
>print(student)
>print(type(student))
>name = bool(name) #轉換成布林值
>print(name)
>print(type(name))
>```
>顯示型別轉換結果:
>```
>57.0
><class 'float'>
>169
><class 'int'>
>True
><class 'str'>
>True
><class 'bool'>
>```
### 隱式型別轉換（自動進行型別轉換）
>自動根據**運算**需求，在不同型別之間進行轉換，這些轉換是隱式（不需要手動轉換），避免資料丟失或運算錯誤。
>1. 整數（int） → 浮點數（float）
>2. 整數（int） → 複數（complex）
>3. 布林值（bool） → 整數（int）:在數值運算中，True 被視為 1，False 被視為 0，所以 bool 會自動轉換為 int。
>4. 布林值（bool） → 浮點數（float）
>
>**有些型別不會自動進行型別轉換**
>1. 字串（str）
>2. 列表（list）
>3. 元組（tuple）
>4. 集合（set）
>```
>## 隱式嫌別轉換
>### 整數（int） → 浮點數（float）
>x = 10
>y = 2.0
>print(type(x))
>x =x/y
>print(x)
>print(type(x))
>
>### 整數（int） → 複數（complex）
>a = 3   # int
>b = 2 + 4j  # complex
>result = a + b  # 3 (int) + (2 + 4j) (complex)
>print(result)   # (5+4j)
>print(type(result))  # <class 'complex'>
>
>### 布林值（bool） → 整數（int）
>a = True   # 代表 1
>b = False  # 代表 0
>print(a + 5)  # 1 + 5 = 6
>print(b + 10) # 0 + 10 = 10
>print(type(a + 5))  # <class 'int'>
>
>### 布林值（bool） → 浮點數（float）
>a = True   # 代表 1
>b = 2.5    # float
>result = a + b  # 1 + 2.5
>print(result)   # 3.5
>print(type(result))  # <class 'float'>
>```
