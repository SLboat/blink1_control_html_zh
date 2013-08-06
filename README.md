## 这里是 ##
* Blink1Control的中文翻译界面

## 我们是 ##
* 我们大部分是小孩子，除了一两个不是
* 我们喜欢这个小灯-大部分时候

## 如何使用 ##
* 提取整个库里的文件解压到Blink1Control的html目录里

## 制造者 ##
* 小梦@淀粉-主翻译
* 小约子@淀粉-文档翻译
* 船长-整合翻译
* 小浩子-MarkDown语法专家

## 官方文档 ##
==============================================

To get compiled application, download:
http://thingm.com/blink1/downloads/Blink1Control-win.zip

To run Blink1Control, double-click the Blink1Control.exe application icon.

Blink1Control requires Microsoft's .NET Framework 4.5, 
available free from http://www.microsoft.com/en-us/download/details.aspx?id=30653

You will also need to give Blink1Control permission to access local networks.

When Blink1Control is running, minimizing its window will put it in the system tray. 
Double-click to get it back.


Local webserver URL API:  

See the document 'blink1/docs/app-url-api.md'


Releases 
========

0.9.5 -- 15 Jan 2013 
- initial release to public
- requires .NET Framework 4.5

0.9.6 -- 20 Jan 2013 
- fixed some settings loading bugs

0.9.7 -- 27 Jan 2013
- .NET Framework requirement now 4.0 instead of 4.5
- fixed up IFTTT event sources
- added logging to logs/log.txt
- added Start Minimized option
- cleaned up HTML UI a little

(to get version: right-click on Blink1Control.exe, go to Properties > Details)


Building
========
To build, open solution file 'Blink1Control/Blink1Control.sln' in Visual Studio Desktop Express 2012.

All dependencies are included in the source tree.

For more information on Blink1Control internals, see the github at:
  https://github.com/todbot/blink1/tree/master/windows


Open Source Software used in this application
=============================================

In general, the software packages are copied wholesale, complete with their respective licensing.

- blink1-lib - C-library to talking to blink(1), wraps HIDAPI
-- http://github.com/todbot/blink1

- CefSharp - .NET binding for Chromium Embedded Framework
-- https://github.com/chillitom/CefSharp

- MiniHttpd - stand-alone HTTP web server library
-- http://www.codeproject.com/Articles/11342/MiniHttpd-an-HTTP-web-server-library

- Json.NET - JSON framework for .NET
-- http://json.codeplex.com/


Compilation Notes
=================

Blink1Control currently targets x86 and .NET Framework 4.5.  
There may be a way of downgrading to .NET 4.0, but I don't know how to do it.
The x86 dependency is because of the CefSharp library, which was compiled x86.



Packaging Steps (in lieu of real installer, these are mostly notes to tod)
===============
% In VS2012: Build
% cd blink1/windows/Blink1Control/Blink1Control/bin/x86/Debug
% rm -rf *xml *pdb *application *manifest *vshost* debug.log logs
% cd .. 
% rm -rf Blink1Control*  # (in case already exists)
% mv Debug Blink1Control 
% zip -r Blink1Control-win-0.9.5.zip Blink1Control