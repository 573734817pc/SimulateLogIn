1、功能：这是一个利用cookie进行模拟登陆的插件（cookie可以在浏览器中登陆后F12获取）
2、基于python开发
3、使用的时候只需要配置好SimulateLogInConf文件即可。
配置demo如下：
	# 默认编码
        self.encoding = 'utf8'
        # 浏览器登录后得到的cookie，也就是刚才复制的字符串
        self.cookie_str = r'ga=GA1.2.964601734.1546485094; __gads=ID=57cc9e1b2f188386:T=1546485229:S=ALNI_MbGBTRquroCotj8Qd4AaTIwELYwDg; UM_distinctid=1684f538f89210-0f4044f1ee46d8-5d1f3b1c-1fa400-1684f538f8a420; Hm_lvt_f1efa4dd0c4c1bdecd84dd62ecd602bc=1556428464; .CNBlogsCookie=8BD194E83671988C985523E326D52F82E11D12D93F6083CDA0856FC2A462B88AAF5CA6574644228B97BFAF793623E3018AB151BE994A5AD22B94482FB29205F14F343831748487FB06E84E90A6E572B055A7A5D2; _gid=GA1.2.669469701.1561354463; .Cnblogs.AspNetCore.Cookies=CfDJ8D8Q4oM3DPZMgpKI1MnYlrkWs2jL31eCjQPRRdjGU-4-TCf6JeUvpvG2oYo_jEWu8dOrcHuvn08bEYboGNL3Iab0c-9FRjvEoR1c6Kic-YY7U_eiYWdTi7Xmn8e7ek-BUDEIHC20z7GY4Ta77cXDX2ODTwK8HzqQ_G1aqqi3OvjflGCW3HbILY_AD4OPrDbPCA1PxaiA9TMSHHZGd7mHeQoyS5j8qkHTki5c_3rLRUKex90JWt3LASSxIvqxjIJq-tKqOZ7eh1Elqo2jiCoLbHW6u09-k9GwGUIRtUGFpB-bQA5zxPPmNr3O4WdORobsJQ; _gat=1; SERVERID=04ead23841720026ba009cb4f597ec8c|1561442873|1561442873'
        # 登录后才能访问的网页
        self.url = 'https://www.cnblogs.com/573734817pc/p/11078755.html'
        # User-Agent
        self.user_agent = 'Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/60.0.3112.113 Safari/537.36'
        #运行login方法
        self.simulate_login()

4、由于，该插件的oop设计策略为简单工厂模式，所以，可以实现配置多个simulate_login_confX(self)方法，模拟登陆多个网站的功能。
   配置了多个simulate_login_conf(self)方法后，在SimulateLogInRun文件中加入执行即可。
	SimulateLogInConf.SimulateLogInConf().simulate_login_confX()
