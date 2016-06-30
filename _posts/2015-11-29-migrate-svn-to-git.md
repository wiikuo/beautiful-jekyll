---
layout: post
category : how-to
tagline: "遷移 Subversion 至 Git"
tags : [svn, git]
---


# 前情提要

想要用 Git 但是團隊還在用 SVN 怎麼辦? 其實可以透過 Git 與 SVN 的儲存庫同步，這樣就可以一邊使用 SVN ，一邊使用 Git 了


# 設定步驟

## Step 1. 建立一個使用者對照檔目的

如果希望在 git 的 log 記錄中，看到作者欄是你指定的名稱，就需要編輯這個檔

作法: 建立一個純文字檔，以以下的格式建立 已經在 svn 中 commit 過的全部使用者 wii = Wii Kuo <wiikuo@facebook.com>svn 帳號 = 姓名 <email信箱>


## Step 2. 自 SVN 儲存庫複製至 Git

執行以下指令

`git svn clone http://127.0.0.1/project1 -A .gitusers --stdlayout`

* http://127.0.0.1/project1 請換成你的 SVN 儲存庫的 URL
* gitusers 則是 Step 1 建立的對映檔路徑
* --stdlayout 則是當 SVN 的目錄結構是標準的結構(trunk, branches tags)時要告知 Git 用的

等待 Git 將 SVN 同步下來，之後這樣就可以把 SVN 儲存庫搬到 Git 囉。


# 補充

如果有一些比較特殊的情形，可以再看看下面參考網址的內容做調整。

* http://triptico.com/notes/8d4510bb.htmlhttp://john.albin.net/git/convert-subversion-to-git
