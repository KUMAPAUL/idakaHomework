# hw3：跟你朋友介紹 Git
## 先簡單介紹 Git 是什麼
Git 是版本控制軟體，版本控制每個人一定都有使用過，像是以前做報告的時候，會有 期中報告第1版.ppt、期中告報第2版.ppt、...、期中報告final版，這就是版本控制，當你覺得 final 版不好時，想回到某 n 版，再從第 n 版改下去，Git 就是在幫你做這件事，你不用自己手動儲存，或是想回到某個版本，需要手動自己找，當資料非常龐大的時候，就會非常的麻煩。Git 會自動幫你把這些做好。
## 介紹基本指令
`git init` 把 Git 加到目錄裡，任何想用 Git 版本控制的資料夾，一開始都需先 `git init`。  
`git status` 查看目前 Git 的狀態，像是有哪些檔案未被加入 Git，有哪些檔案更動過下 commit 了沒。  
`git add` 將 status 裡未被加入 Git 的檔案加入版本控制。`git add 檔名` 將檔案加入 Git，如果有很多檔案想加入 Git，可以使用 `git add .`  
`git commit` 新建版本。可以用 `git commit -m "commit name"` 輸入這個版本的說明。  
`git log` 查看版本日誌。  
`git checkout` 回到某個版本。  
.gitignore 如果有不想被加入版本控制的檔案，可以將檔案名稱輸入到 .gitignore 裡。   
以上就是個人常用的基本指令。  
接下來介紹 Git 裡面的分支 branch。  
假設今天軟體開發商有一個穩定的功能已經在市場上使用，今天如果想要開發新功能，那就需要開一條新的分支，因為如果在原本的單條線裡面直接 commit，在新功能開發到一半的時候，原本的穩定版出現了一些 bug，這時候因為只有一條線，所以當 bug 修復好時，只能 commit 在新功能後面，這樣發布的時候，就會被使用者看到還未開發完全的新功能。  
  
`git branch` 開一個新的分支   
`git checkout` 切換到某分支  
`git merge` 合併兩個分支  
`git branch -v` 可以查看目前有哪些分支  
`git branch -d` 可以刪除分支  
當 merge 時遇到 conflict，系統會出現 merge fail: merge conflict xxx 檔案，或是可以用 `gst` 來查看哪個檔案有衝突，然後需要進到檔案手動修正衝突的地方，git 會幫你標出衝突的地方，可以選擇保留主線或分支的內容，或是手動新增一個新內容，改完之後就可以 git commit 然後合併。  
合併完之後，`git log` 可以看到主線的 commit、branch 的 commit 跟 conflict 完的 commit。
