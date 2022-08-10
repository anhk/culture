---
layout: post
title: Windows系统窗口消失之谜及解决方法
category: Windows
---

在使用Windows操作系统的时候，你有否试过你打开的一些窗口不见了。但在任务栏仍然见到它的“身影”，但点击任务栏的窗口，与鼠标右键选择“还原”也无补于事，窗口还是不出现在桌面上。最近笔者找到了其原因和解决方法。

 <!--more-->
这是因为Windows操作系统是基于消息机制，但运行的程序收到消息的变化，便会触动该窗口“重画”，窗口“失踪”是因为这个时候由于系统的一些失误，或其他意外原因令到窗口重画在我们能看到的桌面之外。例如，我们的分辨率是800×600，但窗口的坐标是(900，100)，这时候我们便看不到窗口，只要把窗口移动到我们能看到的范围就可以了。

解决方法: 因为我们没有办法把鼠标定位在窗口的确实位置，我们要借助键盘来进行解决问题。

1. 把鼠标的光标放在任务栏上的该“失踪”窗口位置，点击一下，这样接下来的操作便是对其进行。
1. 按ALT+空格，这个快捷键打开控制菜单。
1. 按M键，“失踪”窗口便处于移到状态。这时候，桌面上便没有了鼠标的光标。
1. 随便移动一下键盘上的方向键。这样，鼠标的光标实际上于处于移动窗口绑在一起了。
1. 移动鼠标，直至窗口出现在桌面，点击鼠标左键或者按键盘Esc键停止移动，窗口便会重新出现在桌面上
