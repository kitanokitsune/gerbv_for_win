# gerbv 2.7.0 for Windows
ガーバーデータをWindows上で表示できます。
  
<img src="./sample.png" width="600px" alt="gerbv" title="gerbv">

## Overview
[gerbv 2.7.0](https://sourceforge.net/projects/gerbv/files/gerbv/gerbv-2.7.0/ ) のWindows実行用ファイル一式です。[32bit版](./32bit) と [64bit版](./64bit) があります。  
ビルドには msys64 (mingw-w64) を使用しました。  


## Install
[32bit版](./32bit) または [64bit版](./64bit) の中身を適当なディレクトリへ配置してください。  
このとき **bin**, **lib**, **share** のディレクトリの相対位置が変わらないようにしてください（以下の位置関係を守ってください）。  
```TEXT
<install_dir> --+-- bin\ （この中に gerbv.exe がある）
                |
                +-- etc\
                |
                +-- lib\
                |
                +-- share\
```  
**`<install_dir>`** は任意の場所／名前で構いませんが、**bin**, **lib**, **share** の位置関係や名前は変えないでください。変えてしまうと **gerbv.exe** が初期化ファイルや日本語訳ファイル等を見つけられなくなってしまいます。  


## Localization
日本語メニューのファイルは **share\locale\ja\LC_MESSAGES\** にあります。これ以外の場所に配置すると gerbv がファイルを認識できなくなり、メニューが英語表記（デフォルトの状態）に戻ります。  

gerbv の日本語訳を直す場合は **ja.po** ファイルをテキストエディタで編集した後、**gerbv.mo** に変換してください（変換には **msgfmt** コマンドが必要です）。  
 msys (msys64) 環境がある場合は **compile_po.sh** を実行すれば変換できます。  
出来あがった **gerbv.mo** を **share\locale\ja\LC_MESSAGES\** へコピーしてください。  

なお、**ja.po** の文字コードは UTF-8 でなければなりません。このため、コマンドプロンプトへ出力する文字列（例えば **`gerbv.exe --help`** を実行した場合に表示されるメッセージなど）は日本語に翻訳しない方がよいでしょう（コマンドプロンプトは標準の文字コードが CP932/Shift-JIS のため文字化けしてしまう）。  


## Source Code
本プログラムに使用したソースコードは、（この時点での最新版である）gEDA プロジェクトの git から clone した以下の版をベースにしています。  
[http://git.geda-project.org/gerbv/tree/?id=b5f1eacd798f327ab319af939f89031db4b7c10a](http://git.geda-project.org/gerbv/tree/?id=b5f1eacd798f327ab319af939f89031db4b7c10a)  

このソースに以下のパッチを当てました（パッチ適用後のソースファイルは [src](./src) ディレクトリにあります）。  
**パッチの内容**
+ [#79 Allow non-ASCII install path on MS-Windows](https://sourceforge.net/p/gerbv/patches/79/ )
+ [#78 Open non-ASCII filename](https://sourceforge.net/p/gerbv/patches/78/ )
+ [#77 Fix double-freeing memory](https://sourceforge.net/p/gerbv/patches/77/ )
+ [#76 Allow 'gerbv foo.gvp' to act like 'gerbv -p foo.gvp' was specified](https://sourceforge.net/p/gerbv/patches/76/ )
+ [#75 Fix bounding box calculation for slots](https://sourceforge.net/p/gerbv/patches/75/ )



## License
本ソフトウェアはオリジナルの gerbv に倣い GPLv2 に従って配布されます。  
```TEXT
Copyright (C) 2020 kitanokitsune

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.
```
---
kitanokitsune / 北乃きつね
