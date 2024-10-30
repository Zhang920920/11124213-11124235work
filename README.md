# 南華大學軟體工程-期中報告
11124213 張芮瑜 11124235 吳易軒
# 實驗三、UML靜態建模之類的分析與設計
## 實驗目的
透過 [UML建模](https://so.csdn.net/so/search?q=UML%E5%BB%BA%E6%A8%A1&spm=1001.2101.3001.7020) 過程掌握類的分析與設計方法
## 實驗環境
[PowerDesigner](https://so.csdn.net/so/search?q=UML%E5%BB%BA%E6%A8%A1&spm=1001.2101.3001.7020)
## 實驗任務
針對迷你[圖書管理系統](https://gitcode.com/open-source-toolkit/ede4c/overview?utm_source=highlight_word_gitcode&word=%E5%9B%BE%E4%B9%A6%E7%AE%A1%E7%90%86%E7%B3%BB%E7%BB%9F)的用例圖(圖一)，展開分析，完成類建模。
# 圖
圖一:迷你圖書管理系統用例圖
![](https://tinyurl.com/32vjen57)
## 實驗步驟
分析實驗任務內容，並利用UML完成類的建模並生成對象，主要包括：
```
1.定義類（包括類名、屬性、操作等）  
2.建模類之間的關係（包含關聯、泛化、依賴、實現等）  
3.構建完整的類圖（至少包含抽象類、組合、聚合、多重性、可見性和介面等）  
4.根據類圖，生成系統某一時刻的對象圖  
注意：上述括號中的內容必須體現在圖中，缺一項本實驗得分扣5分；請自行設計類圖和對象圖，注意邏輯。
```
## 實驗過程
1.完整的類圖:
# 圖
![](https://tinyurl.com/bdh8jwnd)
分析：

上圖總的來說共有六個類，其中分別是 `User`、`RegisteredUser`、`OrdinaryUser`、`LibraryManager`、`MailSystem`、`Library`。
其中，`MailSystem` 是接口。`User` 類關聯 `RegisteredUser` 和 `OrdinaryUser` 類，同時這兩個類和 `User` 之間也存在聚合關係。`LibraryManager` 和 `OrdinaryUser` 都繼承自 `RegisteredUser` 類。`Library` 類依賴於 `RegisteredUser` 和 `OrdinaryUser` 類；`LibraryManager` 還實現了 `MailSystem` 接口，並且與 `Library` 之間存在組成關係，各個類都設置了一定的可見性，有的定義了一些操作方法。
2.對象圖:
# 圖
![](https://tinyurl.com/kc6xv2vp)
從上圖可以看出有三個對象。
# 參考資料
https://blog.csdn.net/guleilei0/article/details/124869507
