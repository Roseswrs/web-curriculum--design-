author:14130140400 王如思
## 一、概述
  该系统主要功能是为大学生提供一个类似于班级共同拥有的博客，用户可登录注册，并发布消息。其他用户可查看消息，并对此消息发表评论。基于
  此基础，该系统有意向发展为某个高校的校内论坛。
## 二、web应用功能需求
- 1 .用户注册功能：用户可以使用学号在本系统上注册账号。
- 2 .用户登录功能：已经注册的用户可以使用学号登录该系统。
- 3 .用户可以发布班级信息：已经登录的用户可以发布班级通知，班级通知上会注明通知标题，发布人，发布时间以及通知概要。
- 4 .可以浏览通知信息列表：通知信息分页显示，每10条一页，可以通过点击翻页。
- 5 .可以浏览通知详情：用户通过点击列表上的条目进入相应的班级信息详情页。
- 6 .可以在班级通知详情页对该通知发布评论和留言（仅对已经登录用户提供）。
- 7 .可以根据学号或姓名查找用户：如果查找用户是当前登录用户，则提供注销账号和修改个人信息的权限；如果不是当前登录用户，则只有查看的权限。
- 8 .用户界面简洁大方，易于使用，交互逻辑清晰。
- 9 .为了系统的安全性能，我们在登录和注册界面均使用了图形验证码。

## 三、初步的web应用用户界面
   界面设计要满足简洁大方，可以满足用户的基本要求即可。目前所需要的界面大概如下：
- 1 初始登录界面：包含登录和注册按钮，以方便新老用户使用。
- 2 系统主页面：包含创建新通知，通知信息列表（分页，每页大概有10条，可点击翻页），查找用户等几大板块。
- 3 创建新通知页面：包含标题，日期（系统自动生成），发布人（自动生成，目前登录的账号），通知概要，提交按钮。
- 4 通知详情：可通过点击信息列表中的某个信息跳转到详情页面，该页面需包含评论等功能。
- 5 查找用户：用户匹配跳转到该用户的个人信息界面，可进行个人信息的修改。用户不匹配，则跳转到查找用户的个人信息界面，但不提供修改功能。
- 6 个人信息界面：包含基本信息以及已发布的班级信息通知。
 
## 四、web应用质量需求
  目前该web应用的质量要求只限于用户信息的保护和查找效率，其他质量相关的需求会在之后逐步改善和迭代。
- 1 为防止有人恶意攻击该网站，并且防止恶意注册和暴力破解，我们对登录界面和注册界面添加了图形验证码。
- 2 对数据库进行操作时，应在有效防止SQL注入式攻击的同时，增强SQL语句的执行效率，缩短数据库的数据请求响应时间，优化用户体验。
 
## 五、项目约束
  项目需在本学期内由团队人员齐力完成。
  
## 六、发展需求
  该系统目前支持为班级信息通知，人数较少，后期有意改为整个学校的论坛，我们需对网站访问量的增长有个初步的估计，为防止后期系统的大幅度修改，应当使用可伸缩的架构。
