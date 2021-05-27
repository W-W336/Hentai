# 出现下面的问题可以参考此文章
  - 重启持续进入fastboot
  - 电脑端点击刷入后迟迟不显示==“刷机完成！请手动恢复出厂设置”==

## 解决方案
   - 安装[驱动](https://pan.baidu.com/s/191DWjPZeuRBIlqkJxYAyVQ),提取码：ybdk 
     
>### Windows 10

       1. 如果要在 Windows 10 系统上首次安装 Android USB 驱动程序，请执行以下操作：
       2. 将您的 Android 设备连接到计算机的 USB 端口。
       3. 在 Windows 资源管理器中，打开计算机管理。
       4. 在计算机管理左侧窗格中，选择设备管理器。
       5. 在设备管理器右侧窗格中，找到并展开便携式设备或其他设备，具体取决于您看到的是哪一项。
       6. 右键点击已连接设备的名称，然后选择更新驱动程序软件。
       7. 在硬件更新向导中，选择浏览计算机以查找驱动程序软件，然后点击下一步。
       8. 点击浏览，然后找到 USB 驱动程序文件夹。例如，Google USB 驱动程序位于 android_sdk\extras\google\usb_driver\。
       9. 点击下一步以安装驱动程序。
       10. 安装好了


>### Windows 8.1 

       1. 如果要在 Windows 8.1 系统上首次安装 Android USB 驱动程序，请执行以下操作：
       2. 将您的 Android 设备连接到计算机的 USB 端口。
       3. 访问搜索功能，具体方法如下：
         - 触摸屏：在计算机上，从屏幕右侧边缘向里滑动，然后点按搜索。
         - 使用鼠标：指向屏幕的右下角，向上移动鼠标指针，然后点击搜索。
         - 在搜索框中，输入相应内容，然后点击设备管理器。
         - 双击相应的设备类别，然后双击所需的设备。
         - 点击驱动程序标签页，点击更新驱动程序，然后按照说明操作。


>### Windows 7
       1.将您的 Android 设备连接到计算机的 USB 端口。
       2.从桌面上或 Windows 资源管理器中右键点击计算机，然后选择管理。
       3.在左侧窗格中选择设备。
       4.在右侧窗格中找到并展开其他设备。
       5.右键点击相应的设备名称（如 Nexus S），然后选择更新驱动程序软件。这将启动硬件更新向导。
       6.选择浏览计算机以查找驱动程序软件，然后点击下一步。
       7.点击浏览，然后找到 USB 驱动程序文件夹。（Google USB 驱动程序位于 android_sdk\extras\google\usb_driver\。）
       8.点击下一步以安装驱动程序。
     
     
     *或者，如果要在 Windows 7 及更高版本的系统上使用新驱动程序升级现有的 Android USB 驱动程序，请执行以下操作：

       1. 将您的 Android 设备连接到计算机的 USB 端口。
       2. 从桌面上或 Windows 资源管理器中右键点击计算机，然后选择管理。
       3. 在“计算机管理”窗口的左侧窗格中选择设备管理器。
       4. 在右侧窗格中找到并展开 Android 手机。
       5. 右键点击 Android Composite ADB Interface，然后选择更新驱动程序。这将启动硬件更新向导。
       6. 选择从列表或指定位置安装，然后点击下一步。
       7. 选择在这些位置上搜索最佳驱动程序，取消选中搜索可移动媒体，并选中在搜索中包括这个位置。
       8. 点击浏览，然后找到 USB 驱动程序文件夹。（Google USB 驱动程序位于 android_sdk\extras\google\usb_driver\。）
       9. 点击下一步以升级驱动程序。

# 进入到正常的安装流程
  - 重启到 fb，双击刷机包里的 “双击刷入.bat” 直到出现 “刷机完成！请手动恢复出厂设置”，然后在 fastbootd 里选择 recovery 双清重启就可以了。


# 刷入magisk

   使用酷友分享的[一键刷入`boot.img`工具](https://pan.baidu.com/s/1drGiTLXGXwqNT9KAQml2Rw),提取码：q8fe 
   
   里面有`booot.img`镜像文件，就是酷安`@魂梦九霄`大佬分享的类原生hentai包里面的，不放心的自行更换即可
   如果是全新没root过的手机，顺序的部分是
   ```
   1. 先提取目前ROM的Boot.img（每个OEM ROM的更新都会有）
   2. 把 Magisk App 进行安装，从 App 里面的安装，选择 Patch Boot（选择并修补一个文件，修补完成的会保存在Download文件夹中，命名为magisk_patched-xxx.img）
   3. 修补完成会产生 Patch_boot.img ，将其提取到电脑
   4. 手机端重开到 Fastboot 模式
   5. 电脑端将刚刚提取的修补档案用 Fastboot 指令刷入 Boot 分割区
   6. 重开机，Enjoy
   ```
 *注意事项：<br>
 把你自己修补好的boot文件改名1.img放到刷入工具的路径，注意后缀不能出问题！<br>
 如果跟手机连接不正常。请在本工具包找到驱动文件安装试试。
 
## 其他帮助：
- 刷入`boot.img`工具也可以使用`@浅陌初心i`大佬的,酷安搜索他的帖子[面具教程](https://www.coolapk.com/feed/26100021?shareKey=ZTUyNzZlOWVjZDJiNjA4MDNjZDU~&shareUid=2840059&shareFrom=com.coolapk.market_11.1.2)。很详细，建议多看几遍
- 详细刷机方法可以参考`@wushidi`大佬的[帖子](https://www.coolapk.com/feed/17697847?shareKey=Y2MwMjU2MTA2ZTc4NjA4MDNiZTM~&shareUid=2840059&shareFrom=com.coolapk.market_11.1.2)
- 参考工具还有`@残芯此生不换_TWRP`大佬的[输入工具2.0](https://chuxin86.lanzous.com/i0KpInnxgvg)
- k40 谷歌相机请访问`@魂梦九霄`的[博客](https://blog.lcon.wang/index.php/archives/102.html)


参考文档:<br>
https://developer.android.com/studio/run/oem-usb#InstallingDriver<br>https://blog.csdn.net/abcs77/article/details/109698777
   
# 特别感谢
感谢酷安`@魂梦九霄`大佬提供的建议思路，以及分享的hentai包<br>
感谢酷安`@浅陌初心i`大佬<br>
感谢酷安`@wushidi`大佬<br>
感谢酷安`@残芯此生不换_TWRP`大佬<br>
感谢酷安`@shenmedongxi`的文案提供
       
        
        
        
