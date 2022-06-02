源码下载https://www.jianshu.com/p/7c6ab4081aff
1.java: 无效的目标发行版: 11   File -> Porject struc   中设置成 8
                            File -> Settings        Build -> Compiler -> java Compiler 设置成8
2.访问页面报错
    ContextConfig.java 中  webConfig();下添加代码
    context.addServletContainerInitializer(new JasperInitializer(), null);

java-jsy  test-servlet项目war放入webapp
http://localhost:8080/testservlet/hello

#server.xml
<br>Engine 		                    对应tomcat,指定默认域名
<br>    List<Host>  	            支持多域名配置同一ip
<br>        List<Context>  	        多个应用,即webapp目录下文件
<br>            List<Wrapper>  	    多个servlet类型,多例是区分
<br>                List<Servlet>	Servlet对象


ServletDemo extends HttpServlet  单例的
ServletDemo extends HttpServlet implements SingleThreadModel  多例的

#启动类  Bootstrap