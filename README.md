# python-installation
1. 程序安装
2. 注册配置
3. 远程管理
4. 其他发送安装成功信息等

1： 执行install.py -> 确认安装路径(eg:/root  /usr/local)
                   -> 开始配置： recv:(eth0),确认后需要检查网口的正确性
				   -> send:(eth1)
				   -> 开启多少个发送线程 send_thread:(8)
				   -> dst_mac:(00:00:00:00:00:00) -->最终配置到monitor.json文件中
				   -> copy程序 文件到安装目录(判断之前是否已经安装过)
				   
2：注册，调用云端注册接口
            api.router.lianel.com/Acinfo/byPassCreateSnByMac
			参数
			timestamp
			mac
			sign
			设备通过mac生成sn
			返回{
			‘status’:0,
			'info' :['sn':'dsadadasdsa'],
			'data' :['sn':'dsadadasdsa']
			}
			旁路设备获取sn接口
            -> 设备id最终配置写到 stmtr.ini
3. 远程管理ssh等源码安装
            -> 是否需要确认能否远程

4. 最终把 设备相关信息发送邮件
