土司自动签到脚本

*****************
准备环境：

python3、可写的目录权限（用于生成日志）

用法：

<details>
  <summary>1. Windows下设置自动签到：</summary>
  
    1) . 打开命令行cmd，输入： 
     schtasks /create /sc daily /tn "t00ls_sign" /tr "python3 t00ls_auto_sign.py"
  
    2) .在cmd输入compmgmt.msc，打开计算机管理，在左侧选择系统工具->任务计划程序->活动任务->找到t00ls_sign双击->属性->操作->编辑，
      在“起始于”里写入你存放脚本的文件夹路径。
    
    3) .上面两步都要做，可以在log.txt查看签到日志.
</details>


<details>
  <summary>2. Linux下设置自动签到：</summary>
  
    1) 
      crontab -e
  
    2) 写以下指令，每天5.00am自动执行。
      0 5 * * * python /path/t00ls_auto_sign.py
</details>
    

<details>
  <summary>3. 手动签到一次：</summary>
    
    python3 t00ls_auto_sign.py
</details>


  
