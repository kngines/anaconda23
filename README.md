# anaconda23s
- 分析工具搭建 && 常见问题与总结
	- anaconda + odps
	- [anaconda + hive](https://blog.csdn.net/qq_24452475/article/details/94319179)

### 构建文档详细版
- Anaconda环境安装及多内核配置.docx 
### 构建文档mini版(5 steps)
- bash 安装
	
		bash Anaconda3-4.4.0-Linux-x86_64.sh
	
- 生成配置文件
		
		jupyter-notebook --generate-config -allow-config

- ipython创建密码
	
		ipython # 进入IPython 环境
	
		from notebook.auth import passwd # 导入登录认证模块
	
		passwd() # 调用生成密码方法

- 配置端口等信息
	
		c.NotebookApp.ip='*'    # 设置 ip
	
		c.NotebookApp.password = u'sha1:626ceb2480e8:01ebe2f1fb582129ab1ae45aa6e715c5a5244e1c' # 配置访问密码
	
		c.NotebookApp.open_browser=False # 在服务端启动Jupyter服务器后，默认不自动打开浏览器
	
		c.NotebookApp. port=8888    # 设置 Jupyter服务器 访问端口
	
		c.NotebookApp.notebook_dir='/home/kngines/jupyters' # 配置根目录
	
- nohup 后台运行
	
		nohup jupyter notebook --allow-root >> nohup.out 2>&1 &

---
- 可利用配置文件
	- jupyter_notebook_config.py
