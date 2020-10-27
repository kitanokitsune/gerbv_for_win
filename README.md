[日本語](./README_jp.md)  

# gerbv 2.7.0 for Windows
Windows port of gEDA gerber viewer
  
<img src="./sample.png" width="600px" alt="gerbv" title="gerbv">

## Overview
A set of [gerbv 2.7.0](https://sourceforge.net/projects/gerbv/files/gerbv/gerbv-2.7.0/ ) files for execution on MS-Windows. [32bit version ](./32bit) and [64bit version](./64bit) are available.
They are built with msys64 (mingw-w64).  


## Install
Copy the contents of [32bit](./32bit) or [64bit](./64bit) into an arbitrary directory.
Please keep the positional relation between **bin**, **lib** and **share** as below.  
```TEXT
<install_dir> --+-- bin\ （gerbv.exe is here）
                |
                +-- etc\
                |
                +-- lib\
                |
                +-- share\
```  


## Localization
The language file **gerbv.mo** should be placed in  **share\locale\<your lang>\LC_MESSAGES\ **.  


## Source Code
This package was based on the source code which was obtained from **git.geda-project.org**.
[http://git.geda-project.org/gerbv/tree/?id=b5f1eacd798f327ab319af939f89031db4b7c10a](http://git.geda-project.org/gerbv/tree/?id=b5f1eacd798f327ab319af939f89031db4b7c10a)  

I patched the following fix to the above source code. The result source is in [src](./src) directory.
**Patch contents**
+ [#79 Allow non-ASCII install path on MS-Windows](https://sourceforge.net/p/gerbv/patches/79/ )
+ [#78 Open non-ASCII filename](https://sourceforge.net/p/gerbv/patches/78/ )
+ [#77 Fix double-freeing memory](https://sourceforge.net/p/gerbv/patches/77/ )
+ [#76 Allow 'gerbv foo.gvp' to act like 'gerbv -p foo.gvp' was specified](https://sourceforge.net/p/gerbv/patches/76/ )
+ [#75 Fix bounding box calculation for slots](https://sourceforge.net/p/gerbv/patches/75/ )



## License
This software is distributed under GPLv2.
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
