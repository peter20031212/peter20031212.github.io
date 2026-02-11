---
title: "Linux 文件格式介紹"
date: 2026-02-11 12:00:00 +0800
categories: [Linux, 文件系統]
tags: [文件格式, ext4, inode, bash]
---

# Linux 文件格式介紹

本文將介紹 Linux 中常見的文件格式，以及如何查看文件類型和結構。

---

## 1. 常見 Linux 文件格式

Linux 系統中常見的文件格式有：

1. **普通檔案 (Regular File)**  
   - 存放文字、程式、資料等  
   - 例如 `.txt`, `.log`, `.sh`  
   - 查看方式：`ls -l`

2. **目錄 (Directory)**  
   - 存放文件的容器  
   - 查看方式：`ls -ld /home`

3. **符號鏈接 (Symbolic Link)**  
   - 指向另一個文件或目錄  
   - 創建命令：`ln -s source target`  
   - 查看方式：`ls -l`（會顯示指向哪裡）

---

## 2. 檢查文件類型

使用 `file` 命令可以快速查看文件格式：

```bash
file example.txt
file /bin/ls
