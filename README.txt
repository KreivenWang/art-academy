美术设计学院 Arts & Design —— 官网 Demo
=========================================

一个面向 5–7 岁儿童插画启蒙的美术学校品牌官网演示站点，
基于 HTML5 UP 的 Dopetrope 模板改造，纯静态页面，无构建依赖。


项目定位
--------

品牌：美术设计学院 Arts & Design
受众：5–7 岁儿童及其家长
核心内容：展示学生作品、介绍师资与教学方式、提供在线报名与免费体验课预约


页面结构
--------

	index.html			首页
						品牌 Banner、三大教学优势、学生作品精选（6 幅）、
						校园动态（作品展 / 绘本营）、校区公告、联系信息

	left-sidebar.html	学生作品
						分班展示学员插画原作，附作品数量统计与创作故事说明

	right-sidebar.html	师资团队
						教师准入标准、90 分钟四段式课堂结构、师生比、教研制度

	no-sidebar.html		在线报名
						报名信息表单（孩子姓名/年龄、家长联系方式、意向课程、
						上课时段、备注）、报名流程说明

四个页面共用同一套导航与页脚，导航项：

	首页 · 课程（含假期营地二级菜单）· 学生作品 · 师资团队 · 在线报名


本地预览
--------

方式一（Python，推荐，无需安装依赖）：

	python -m http.server 5500

然后访问 http://localhost:5500/index.html

方式二：直接用浏览器打开 index.html

注意：请通过本地服务器访问，而不是双击 HTML 文件。
模板使用了相对路径加载 assets/ 与 images/，部分浏览器在 file:// 协议下
会出现脚本或字体加载受限的情况。


目录说明
--------

	index.html			首页
	left-sidebar.html	学生作品页
	right-sidebar.html	师资团队页
	no-sidebar.html		在线报名页

	images/				演示图片 pic01–pic10
						（模板自带占位图，正式上线需替换为真实学员作品）

	assets/css/main.css				全站样式（含表单、按钮、响应式网格）
	assets/css/fontawesome-all.min.css	图标库样式
	assets/css/images/bg.png		背景纹理

	assets/js/jquery.min.js			jQuery
	assets/js/jquery.dropotron.min.js	下拉菜单
	assets/js/browser.min.js			浏览器特性检测
	assets/js/breakpoints.min.js		响应式断点
	assets/js/util.js					工具函数
	assets/js/main.js					模板主脚本

	assets/webfonts/				Font Awesome 字体文件
	assets/sass/					SASS 源文件（未参与运行时，可忽略）


Demo 说明与已知限制
-------------------

1. 报名表单仅作前端演示
   no-sidebar.html 中的 form 使用 action="#"、method="post"，
   提交不会发送任何数据。接入真实后端时，替换 action 地址即可，
   表单字段已设置 name 属性可直接对接：
   child-name / child-age / parent-name / parent-phone /
   parent-email / course / timeslot / note

2. 课程下拉菜单指向同一个页面
   课程与假期营地下的所有条目目前都指向 no-sidebar.html，
   因为 Demo 阶段未拆分独立课程详情页。正式上线时建议为每门课
   单独建立页面，并同步更新四个页面的导航。

3. 图片为模板占位图
   images/pic01–pic10 为原模板示例图，文案中描述的学员作品
   （《会飞的鲸鱼》《彩色下雨天》等）与图片内容并不对应，
   正式上线需替换为真实作品照片。

4. 联系信息为虚构内容
   校区地址、电话、邮箱、社交账号链接均为演示数据，需替换为真实信息。

5. 表单样式未新增 CSS
   报名表单完全复用 main.css 中已有的 form / input / select / textarea /
   按钮样式，未修改任何样式文件，保持模板原有视觉体系。

6. 无构建流程
   纯静态 HTML + CSS + jQuery，无需 npm install 或打包，
   可直接部署到任意静态托管（如 Nginx、GitHub Pages、OSS）。


Credits
-------

	Template:
		Dopetrope by HTML5 UP (html5up.net | @ajlkn)
		Free for personal and commercial use under the CCA 3.0 license
		(html5up.net/license)

	Demo Images:
		Dreametry Doodle (dreametrydoodle.com)
		* 原模板演示图片，版权归原作者所有，未经授权请勿使用

	Icons:
		Font Awesome (fontawesome.io)

	Other:
		jQuery (jquery.com)
		Responsive Tools (github.com/ajlkn/responsive-tools)