#### 武汉2019新型冠状病毒疫情可视化(全国疫情地图及时间轴变化)
- 项目结构
    - nCoc_data_analysis
        - 数据获取与分析提取
    - china_shapfiles
        - 地图基础数据       
    - nCov_basemap_visualization    
        - 疫情数据可视化，包含全国疫情地图、世界疫情地图、主要省份疫情地图、全国疫情随时间变化图
- 可视化效果展示
![疫情地图1](疫情地图1.jpg)
![疫情地图2](疫情地图2.jpg)


#### 1. 数据来源
- 数据来源，腾讯新闻：https://news.qq.com/zt2020/page/feiyan.htm
- 经过解析后的数据地址(json格式数据)：https://view.inews.qq.com/g2/getOnsInfo?name=disease_h5
- json格式在线数据可能会失效，我已经下载保存到项目文件中(可以直接读取本地文件)：getOnsInfo.json

#### 2. 数据请求
- 使用requests请求
- 注意将json数据转换为dict格式

#### 3. 数据分析
- 数据统计主要包括：确诊、疑似、死亡、治愈
- 地区分类：按国家的数据、按省份统计的数据、按城市统计的数据
- 中国截止目前累积数据、每日累积的数据(1月13日开始进行每日数据统计)

#### 4. 疫情数据可视化
- 方案1：  basemap + matplotlib 
- 方案2：  ECharts
- 每日疫情变化时间图
- 中国疫情地图
