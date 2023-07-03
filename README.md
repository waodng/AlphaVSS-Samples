# AlphaVSS-Samples

This repository contains sample projects for the [AlphaVSS](https://github.com/alphaleonis/AlphaVSS) library.  If you want to report an issue, please do so in the [AlphaVSS](https://github.com/alphaleonis/AlphaVSS) repository.

## AlphaShadow

This project is an adoption of the official C++ [VShadow Tool Sample](https://docs.microsoft.com/en-us/windows/win32/vss/vshadow-tool-and-sample) from Microsoft to 
.NET and AlphaVSS.  It  is a command-line tool that you can use to create and manage volume shadow copies.  Run `AlphaShadow help` for more informtion.

## VssBackup

此处关于占用线程的文本文件读取，有处代码有问题，位于 VssBackup 类中的GetStream 方法采用的是系统system.io的File读取会报错：
影子副本属于内核文件，无法读取的错误，需要改成这样才可以：return Alphaleonis.Win32.Filesystem.File.OpenRead(GetSnapshotPath(localPath));

This is a project containing a couple of examples combining [AlphaFS](https://github.com/alphaleonis/AlphaFS) and [AlphaVSS](https://github.com/alphaleonis/AlphaVSS).

## SnapshotQuery

This is a very simple example just illustrating how to start with AlphaVSS.


