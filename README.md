# 52-考研备考服务平台系统-考研系统

[文档地址](http://wechat.zjrcsy.cn/)

**技术栈：** Spring Boot + Vue

**访问说明：** 前后端分离部署；前端默认通过 Vite 开发服务或构建产物访问，后端提供 `/api`（用户端）与 `/admin`（管理端）接口，具体域名与端口以本地 `application.yml` 及前端环境配置为准。



## 补充说明

- 后端技术要点：Spring Boot、MyBatis-Plus、Spring Security + JWT、MySQL、Redis（如 Token 与热点统计）、本地文件存储、Knife4j 接口文档等，详见仓库内《考研咨询与辅导系统_完整设计方案.md》。  
- 前端技术要点：Vue 3、Element Plus、Pinia、Vue Router、Axios、ECharts 等。  
- 项目代码目录：`kaoyan-system/`（后端）、`kaoyan-web/`（前端）、`sql/kaoyan_db.sql`（数据库脚本）。



## 用户端

1. **首页：** 轮播图、考研倒计时、热门资讯与推荐课程入口。  
2. **账户：** 用户注册与登录；JWT 鉴权；部分功能需登录后使用。  
3. **考研资讯：** 资讯列表与详情；分类与排序；富文本阅读；点赞、收藏与评论（含回复）。  
4. **报考指南：** 院校库浏览与筛选；专业库浏览与筛选；院校详情（专业与分数线等关联信息）；专业详情（开设院校等）。  
5. **在线咨询：** 提交咨询工单；查看历史咨询及回复状态；配合前台 FAQ 常见问题展示。  
6. **课程中心：** 课程列表与分类筛选；课程详情；下单与支付流程；我的已购课程。  
7. **课程评价：** 已购用户可对课程评分与文字评价（业务上限制每课单次评价）。  
8. **在线练习：** 试卷列表与模拟考试；答题页倒计时与逐题作答；提交后成绩与解析；练习记录列表与单次记录详情（支持多种练习类型在历史记录中展示）。  
9. **错题集：** 错题列表与科目归类；待复习提示；错题重做与复习间隔策略。  
10. **交流中心：** 帖子列表与话题广场；发帖（富文本）；帖子详情、评论与回复；点赞与收藏。  
11. **个人中心：** 资料维护（昵称、头像、目标院校/专业、密码等）；我的订单；我的收藏；我的帖子。



## 管理员端

1. **首页：** 数据概览与统计图表（用户、订单、刷题等趋势与汇总指标）。  
2. **用户管理：** 用户列表检索与分页；账号启用/禁用。  
3. **系统内容：** 轮播图维护（图片、链接、排序、上下架）。  
4. **考研资讯：** 资讯发布与编辑（富文本）、分类与置顶；资讯评论管理与违规处理。  
5. **报考数据：** 院校信息维护；专业信息维护；院校与专业关联及分数线等配置。  
6. **FAQ 管理：** 常见问题的新增、编辑、排序与分类。  
7. **咨询管理：** 咨询工单列表与状态筛选；查看详情并回复用户。  
8. **课程管理：** 课程分类（含层级）；课程上架信息、价格与上下架；课程评价显示/隐藏。  
9. **订单管理：** 订单检索与状态筛选；订单详情；退款等售后处理（与已购课程权益联动）。  
10. **题库与试卷：** 题目维护与筛选；Excel 批量导入；试卷组卷、分值与启用状态。  
11. **交流社区：** 话题维护；帖子列表、违规处理、置顶；帖子评论管理。



## 用户端界面示意![image-20260414222314363](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222314363.png)

![image-20260414222323898](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222323898.png)

![image-20260414222328789](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222328789.png)

![image-20260414222334132](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222334132.png)

![image-20260414222341880](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222341880.png)

![image-20260414222348548](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222348548.png)

![image-20260414222353303](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222353303.png)

![image-20260414222357094](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222357094.png)

![image-20260414222410176](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222410176.png)

![image-20260414222425459](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222425459.png)

![image-20260414222429756](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222429756.png)

![image-20260414222501608](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222501608.png)

![image-20260414222505623](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222505623.png)

![image-20260414222509772](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222509772.png)

![image-20260414222513950](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222513950.png)

![image-20260414222518969](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222518969.png)



## 管理员端界面示意![image-20260414222531206](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222531206.png)

![image-20260414222536869](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222536869.png)

![image-20260414222547033](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222547033.png)

![image-20260414222553068](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222553068.png)

![image-20260414222559108](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222559108.png)

![image-20260414222602308](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222602308.png)

![image-20260414222605767](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222605767.png)

![image-20260414222613069](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222613069.png)

![image-20260414222619532](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222619532.png)

![image-20260414222622999](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222622999.png)

![image-20260414222627530](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222627530.png)

![image-20260414222632678](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222632678.png)

![image-20260414222636126](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222636126.png)

![image-20260414222640310](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20260414222640310.png)

![image-20260414222653721](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/image-20260414222653721.png)
