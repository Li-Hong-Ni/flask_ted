### TED演讲数据可视化分析

github链接：[https://github.com/Li-Hong-Ni/flask_ted](https://github.com/Li-Hong-Ni/flask_ted)  
【请点击数据分析展示（TED数据分析）（TED数据筛选）】  
pythonanywhere部署：[http://lhn.pythonanywhere.com](http://lhn.pythonanywhere.com)  
TED数据分析：[http://lhn.pythonanywhere.com/line](http://lhn.pythonanywhere.com/line)    
TED数据筛选：[http://lhn.pythonanywhere.com/line](http://lhn.pythonanywhere.com/line)


#### 研究背景
##### TED由Richard Saulman创立于1984年，是一家旨在将技术(technology)，娱乐(entertainment)和设计(design)领域的专家聚集在一起的非盈利组织。Ted的口号是"Ideas worth spreading"，也就是“值得传播的思想”。主要研究数据集其中包含了2017年9月21日之前上传到官方网站TED.com的所有TED Talks演讲录制信息。  

#### HTML技术文档描述
1. 所有的HTML文件放置在templates文件夹中
- index_x.html：进入首页，用户结果页使用了def index_baxr():
- index.html：进入TED数据分析，用户结果页使用了def index_bar():  ，  def index_bar_every_1_tp():  ，  def index_bar_every():  ，  def index_bar_every_X():  ，  def index_bar_every_y():  ，  
- index_1.html：进入TED数据筛选，用户结果页使用了def index_bar_every_z():


#### python 文档描述
1. 安装并导入pandas、pyecharts、cufflinks等等三方包，利用pandas读取csv数据
2. app.py为主要路由函数设置
3. 安装flask环境，导入flask函数和html文件，完成web应用
4. 创建url和函数，用url修饰函数，呈现不同的HTML页面 
  
#### Web App动作描述  
1. web后端服务器启动：执行app.py请求web应用
2. 前端浏览器web请求并访问
3. 后端服务器web响应并执行函数
4. 前端浏览器响应：  
进入首页显示研究背景和两个数据分析链接：  
a：TED数据分析  
用户点击不同数据目录出现不同数据图  
b: TED数据筛选  
用户点击提交课筛选不同主题的TED视频，可了解不同年份的该主题的视频数量  
#### 数据交互  
处理数据  

        for i in df:
    if i[0] not in res:
        res[i[0]] = {i[1]: 1}
    else:
        if i[1] not in res[i[0]]:
            res[i[0]][i[1]] = 1
        else:
            res[i[0]][i[1]] += 1
#### python 文档与html文档的数据交互
- python 文档与html文档的数据交互  
数据的传输 HTML和 Python（服务端 .py） 数据的传输  
- Jinja2方法 ： python函数返回值 render_template html：{{ the_color }}
