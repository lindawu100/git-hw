# 0311 - git進階補充

**git並不在乎檔案名稱，僅在乎檔案內容

**git並不在乎檔案名稱，僅在乎檔案內容

**git並不在乎檔案名稱，僅在乎檔案內容


當操作git add +檔案時(如index.html), git會將檔案裡的“內容物”壓縮並使用演算法丟至.git目錄裡,並形成blob的檔案

註：

演算法特點為：檔案內容如果一樣或沒有修改,git仍會長出commit,但blob僅會覆蓋原檔,並更改覆蓋時間

**相關指令：**

* git cat-file a618 -t(檢視狀態)

* git cat-file a618 -p(檢視內容物)

* cat+檔名 , 能將該檔名內容show在terminal上

# 1st commit

* 指令：mkdir project
  
  建立了project目錄

* 指令：touch index.html

  新增了index.html檔案(此時在working directory)

* 指令：git add index.html

  此時在git裡長出了blob(把index.html加至staging area)

* 指令：mkdir config

  建立了config資料夾(project目錄內)

* 指令：touch config/database.yml

  在config目錄裡,新增了database.yml檔案(此時在working directory)

* 指令：git add config/database.yml

  在config目錄裡長出了blob(把database.yml加至staging area)

* 指令：git commit -m "1st-commit"
![](https://i.imgur.com/qtrbCNe.png)


＊並且HEAD與Master也會出現在commit上＊

# 2nd commit
![](https://i.imgur.com/Z6KVsF2.png)

1.HEAD與Master往前一次移動

2.第二次的commit會指向前一次

3.root tree會指向config目錄(因為在git認為第二次的目錄內容並無差異)



# 3rd commit
![](https://i.imgur.com/GPYEZs3.png)


---

**git中的名詞解釋**
![](https://i.imgur.com/GTIQyzI.png)
