# JVM异常信息

* ## 接口

/send/api/exception

* ## 属性说明

| **名称** | **含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| tid | 租户码 |  |
| appid | 应用ID |  |
| srid | 服务ID |  |
| pt | excp |  |
| **content** |  |  |
| class | 发生的异常 |  |
| rqref | 请求来自哪个页面，例如在百度上点击链接到了这里，那么Referer:[http://www.baidu.com](http://www.baidu.com); 如果你是在浏览器的地址栏里输入，那么就没有这个Referer请求头了 |  |
| rqacc | 告诉服务器客户端可以接收的文档类型 |  |
| rqua | 与浏览器和操作系统有关的信息，有些网站会显示用户的系统版本和浏览器的版本信息，就是从这得到 |  |
| rqmeth | post/get |  |
| type | 错误类型 |  |
| txname | 事务名称 |  |
| txid | 事务ID |  |
| sid | 分布式事务ID |  |
| rquri | 请求的uri |  |
| ssc | session中的用户编码 |  |
| rqhost | 请求方的ip端口 |  |
| time | 耗时 |  |
| thread | 线程名称 |  |
| msg | 错误信息 |  |
| stk | 堆栈信息 |  |
| ts | 时间戳 |  |
| rphc | 表单的数据类型，说明会使用url编码。url编码的数据都是以“%”为前缀，后面跟随两位的16进制 |  |
| rqconl | 请求体的长度 |  |
| dbcnt | 请求数据库的次数 |  |

**注：rp和rq开头的字段分别对应http协议中的POST请求和GET请求，具体可参考http协议相关资料**

* ## 样例

\[

    {

        "content": \[

            {

                "port": 5796,

                "ts": 1490328985723,

                "class": "nc.uap.lfw.core.exception.LfwRuntimeException",

                "txname": "Unknown",

                "type": "TransactionError",

                "msg": "An exception occurred processing JSP page /sync/websm/pserver/html/nodes/login/uimeta.jsp at line 46\n\n43: \t\t&lt;link rel=\"shortcut icon\" href=\"/portal/ufida.ico\"/&gt;\t\n44: \t\t&lt;lfw:base/&gt;\t\t\n45: \t\t&lt;lfw:head/&gt;\t\t\n46: \t\t&lt;lfw:pageImport/&gt;\n47: \t\t&lt;link href=\"/portal/frame/themes/${THEME\_ID}/login/login.css\" rel=\"stylesheet\" type=\"text/css\"&gt;\n48: \t\t&lt;script&gt;\n49: \t\t&lt;%\n\n\nStacktrace:",

                "stk": \[

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.processError\(LfwDispatcherServlet.java:93\)",

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.doPost\(LfwDispatcherServlet.java:83\)",

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.doGet\(LfwDispatcherServlet.java:98\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:621\)",

                    "\tnc.uap.lfw.core.servlet.LfwServletBase.service\(LfwServletBase.java:30\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:722\)",

                    "\tsun.reflect.GeneratedMethodAccessor695.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:166\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:299\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.invoke\(ApplicationDispatcher.java:684\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.processRequest\(ApplicationDispatcher.java:471\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.doForward\(ApplicationDispatcher.java:402\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.access$0\(ApplicationDispatcher.java:333\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:102\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.forward\(ApplicationDispatcher.java:321\)",

                    "\tnc.uap.lfw.app.plugin.AppControlPlugin.handle\(AppControlPlugin.java:158\)",

                    "\tnc.uap.lfw.core.LfwCoreController.handleRequest\(LfwCoreController.java:23\)",

                    "\tnc.uap.portal.ctrl.PortalCoreController.handleRequest\(PortalCoreController.java:32\)",

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.doPost\(LfwDispatcherServlet.java:79\)",

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.doGet\(LfwDispatcherServlet.java:98\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:621\)",

                    "\tnc.uap.lfw.core.servlet.LfwServletBase.service\(LfwServletBase.java:30\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:722\)",

                    "\tsun.reflect.GeneratedMethodAccessor695.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:166\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:299\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.invoke\(ApplicationDispatcher.java:684\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.processRequest\(ApplicationDispatcher.java:471\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.doForward\(ApplicationDispatcher.java:402\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.access$0\(ApplicationDispatcher.java:333\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:102\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.forward\(ApplicationDispatcher.java:321\)",

                    "\tnc.uap.lfw.app.filter.AppFilter.doFilter\(AppFilter.java:52\)",

                    "\tnc.uap.portal.servlet.PortalAppFilter.doFilter\(PortalAppFilter.java:28\)",

                    "\tsun.reflect.GeneratedMethodAccessor745.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\tnc.uap.portal.login.filter.AbstractLfwLoginFilter.doFilter\(AbstractLfwLoginFilter.java:103\)",

                    "\tsun.reflect.GeneratedMethodAccessor700.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\tnc.uap.lfw.core.servlet.LfwRequestListener.doFilter\(LfwRequestListener.java:148\)",

                    "\tsun.reflect.GeneratedMethodAccessor697.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\tnc.uap.lfw.core.servlet.filter.compression.CompressingFilter.doFilter\(CompressingFilter.java:257\)",

                    "\tsun.reflect.GeneratedMethodAccessor713.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\tnc.uap.lfw.core.servlet.LogAroundFilter.doFilter\(LogAroundFilter.java:41\)",

                    "\tsun.reflect.GeneratedMethodAccessor692.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\torg.apache.catalina.core.StandardWrapperValve.invoke\(StandardWrapperValve.java:224\)",

                    "\torg.apache.catalina.core.StandardContextValve.invoke\(StandardContextValve.java:169\)",

                    "\torg.apache.catalina.authenticator.AuthenticatorBase.invoke\(AuthenticatorBase.java:472\)",

                    "\torg.apache.catalina.core.StandardHostValve.invoke\(StandardHostValve.java:168\)",

                    "\torg.apache.catalina.valves.ErrorReportValve.invoke\(ErrorReportValve.java:98\)",

                    "\torg.apache.catalina.core.StandardEngineValve.invoke\(StandardEngineValve.java:118\)",

                    "\torg.apache.catalina.connector.CoyoteAdapter.service\(CoyoteAdapter.java:407\)",

                    "\torg.apache.coyote.http11.AbstractHttp11Processor.process\(AbstractHttp11Processor.java:987\)",

                    "\torg.apache.coyote.AbstractProtocol$AbstractConnectionHandler.process\(AbstractProtocol.java:539\)",

                    "\torg.apache.tomcat.util.net.JIoEndpoint$SocketProcessor.run\(JIoEndpoint.java:298\)",

                    "\tjava.util.concurrent.ThreadPoolExecutor$Worker.runTask\(ThreadPoolExecutor.java:886\)",

                    "\tjava.util.concurrent.ThreadPoolExecutor$Worker.run\(ThreadPoolExecutor.java:908\)",

                    "\tjava.lang.Thread.run\(Thread.java:619\)",

                    " ",

                    "\torg.apache.jasper.servlet.JspServletWrapper.handleJspException\(JspServletWrapper.java:568\)",

                    "\torg.apache.jasper.servlet.JspServletWrapper.service\(JspServletWrapper.java:470\)",

                    "\torg.apache.jasper.servlet.JspServlet.serviceJspFile\(JspServlet.java:390\)",

                    "\torg.apache.jasper.servlet.JspServlet.service\(JspServlet.java:334\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:722\)",

                    "\tsun.reflect.GeneratedMethodAccessor695.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:166\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:299\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.invoke\(ApplicationDispatcher.java:684\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.processRequest\(ApplicationDispatcher.java:471\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.doForward\(ApplicationDispatcher.java:402\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.access$0\(ApplicationDispatcher.java:333\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:102\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.forward\(ApplicationDispatcher.java:321\)",

                    "\tnc.uap.lfw.core.PageControlPlugin.handle\(PageControlPlugin.java:90\)",

                    "\tnc.uap.lfw.core.LfwCoreController.handleRequest\(LfwCoreController.java:23\)",

                    "\tnc.uap.portal.ctrl.PortalCoreController.handleRequest\(PortalCoreController.java:32\)",

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.doPost\(LfwDispatcherServlet.java:79\)",

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.doGet\(LfwDispatcherServlet.java:98\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:621\)",

                    "\tnc.uap.lfw.core.servlet.LfwServletBase.service\(LfwServletBase.java:30\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:722\)",

                    "\tsun.reflect.GeneratedMethodAccessor695.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:166\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:299\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.invoke\(ApplicationDispatcher.java:684\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.processRequest\(ApplicationDispatcher.java:471\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.doForward\(ApplicationDispatcher.java:402\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.access$0\(ApplicationDispatcher.java:333\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:102\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.forward\(ApplicationDispatcher.java:321\)",

                    "\tnc.uap.lfw.app.plugin.AppControlPlugin.handle\(AppControlPlugin.java:158\)",

                    "\tnc.uap.lfw.core.LfwCoreController.handleRequest\(LfwCoreController.java:23\)",

                    "\tnc.uap.portal.ctrl.PortalCoreController.handleRequest\(PortalCoreController.java:32\)",

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.doPost\(LfwDispatcherServlet.java:79\)",

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.doGet\(LfwDispatcherServlet.java:98\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:621\)",

                    "\tnc.uap.lfw.core.servlet.LfwServletBase.service\(LfwServletBase.java:30\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:722\)",

                    "\tsun.reflect.GeneratedMethodAccessor695.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:166\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:299\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.invoke\(ApplicationDispatcher.java:684\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.processRequest\(ApplicationDispatcher.java:471\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.doForward\(ApplicationDispatcher.java:402\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.access$0\(ApplicationDispatcher.java:333\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:102\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.forward\(ApplicationDispatcher.java:321\)",

                    "\tnc.uap.lfw.app.filter.AppFilter.doFilter\(AppFilter.java:52\)",

                    "\tnc.uap.portal.servlet.PortalAppFilter.doFilter\(PortalAppFilter.java:28\)",

                    "\tsun.reflect.GeneratedMethodAccessor745.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\tnc.uap.portal.login.filter.AbstractLfwLoginFilter.doFilter\(AbstractLfwLoginFilter.java:103\)",

                    "\tsun.reflect.GeneratedMethodAccessor700.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\tnc.uap.lfw.core.servlet.LfwRequestListener.doFilter\(LfwRequestListener.java:148\)",

                    "\tsun.reflect.GeneratedMethodAccessor697.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\tnc.uap.lfw.core.servlet.filter.compression.CompressingFilter.doFilter\(CompressingFilter.java:257\)",

                    "\tsun.reflect.GeneratedMethodAccessor713.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\tnc.uap.lfw.core.servlet.LogAroundFilter.doFilter\(LogAroundFilter.java:41\)",

                    "\tsun.reflect.GeneratedMethodAccessor692.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\torg.apache.catalina.core.StandardWrapperValve.invoke\(StandardWrapperValve.java:224\)",

                    "\torg.apache.catalina.core.StandardContextValve.invoke\(StandardContextValve.java:169\)",

                    "\torg.apache.catalina.authenticator.AuthenticatorBase.invoke\(AuthenticatorBase.java:472\)",

                    "\torg.apache.catalina.core.StandardHostValve.invoke\(StandardHostValve.java:168\)",

                    "\torg.apache.catalina.valves.ErrorReportValve.invoke\(ErrorReportValve.java:98\)",

                    "\torg.apache.catalina.core.StandardEngineValve.invoke\(StandardEngineValve.java:118\)",

                    "\torg.apache.catalina.connector.CoyoteAdapter.service\(CoyoteAdapter.java:407\)",

                    "\torg.apache.coyote.http11.AbstractHttp11Processor.process\(AbstractHttp11Processor.java:987\)",

                    "\torg.apache.coyote.AbstractProtocol$AbstractConnectionHandler.process\(AbstractProtocol.java:539\)",

                    "\torg.apache.tomcat.util.net.JIoEndpoint$SocketProcessor.run\(JIoEndpoint.java:298\)",

                    "\tjava.util.concurrent.ThreadPoolExecutor$Worker.runTask\(ThreadPoolExecutor.java:886\)",

                    "\tjava.util.concurrent.ThreadPoolExecutor$Worker.run\(ThreadPoolExecutor.java:908\)",

                    "\tjava.lang.Thread.run\(Thread.java:619\)",

                    " ",

                    "\tnc.uap.lfw.core.importer.SmartImporter.genCommonOptimizedImporter\(SmartImporter.java:222\)",

                    "\tnc.uap.lfw.core.importer.SmartImporter.genImporters\(SmartImporter.java:145\)",

                    "\tnc.uap.lfw.core.tags.PageImportTag.doTag\(PageImportTag.java:29\)",

                    "\torg.apache.jsp.sync.websm.pserver.html.nodes.login.uimeta\_jsp.\_jspx\_meth\_lfw\_005fpageImport\_005f0\(uimeta\_jsp.java:218\)",

                    "\torg.apache.jsp.sync.websm.pserver.html.nodes.login.uimeta\_jsp.\_jspService\(uimeta\_jsp.java:140\)",

                    "\torg.apache.jasper.runtime.HttpJspBase.service\(HttpJspBase.java:70\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:722\)",

                    "\torg.apache.jasper.servlet.JspServletWrapper.service\(JspServletWrapper.java:432\)",

                    "\torg.apache.jasper.servlet.JspServlet.serviceJspFile\(JspServlet.java:390\)",

                    "\torg.apache.jasper.servlet.JspServlet.service\(JspServlet.java:334\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:722\)",

                    "\tsun.reflect.GeneratedMethodAccessor695.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:166\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:299\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.invoke\(ApplicationDispatcher.java:684\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.processRequest\(ApplicationDispatcher.java:471\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.doForward\(ApplicationDispatcher.java:402\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.access$0\(ApplicationDispatcher.java:333\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:102\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.forward\(ApplicationDispatcher.java:321\)",

                    "\tnc.uap.lfw.core.PageControlPlugin.handle\(PageControlPlugin.java:90\)",

                    "\tnc.uap.lfw.core.LfwCoreController.handleRequest\(LfwCoreController.java:23\)",

                    "\tnc.uap.portal.ctrl.PortalCoreController.handleRequest\(PortalCoreController.java:32\)",

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.doPost\(LfwDispatcherServlet.java:79\)",

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.doGet\(LfwDispatcherServlet.java:98\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:621\)",

                    "\tnc.uap.lfw.core.servlet.LfwServletBase.service\(LfwServletBase.java:30\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:722\)",

                    "\tsun.reflect.GeneratedMethodAccessor695.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:166\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:299\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.invoke\(ApplicationDispatcher.java:684\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.processRequest\(ApplicationDispatcher.java:471\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.doForward\(ApplicationDispatcher.java:402\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.access$0\(ApplicationDispatcher.java:333\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:102\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.forward\(ApplicationDispatcher.java:321\)",

                    "\tnc.uap.lfw.app.plugin.AppControlPlugin.handle\(AppControlPlugin.java:158\)",

                    "\tnc.uap.lfw.core.LfwCoreController.handleRequest\(LfwCoreController.java:23\)",

                    "\tnc.uap.portal.ctrl.PortalCoreController.handleRequest\(PortalCoreController.java:32\)",

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.doPost\(LfwDispatcherServlet.java:79\)",

                    "\tnc.uap.lfw.core.servlet.LfwDispatcherServlet.doGet\(LfwDispatcherServlet.java:98\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:621\)",

                    "\tnc.uap.lfw.core.servlet.LfwServletBase.service\(LfwServletBase.java:30\)",

                    "\tjavax.servlet.http.HttpServlet.service\(HttpServlet.java:722\)",

                    "\tsun.reflect.GeneratedMethodAccessor695.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:166\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:299\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.invoke\(ApplicationDispatcher.java:684\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.processRequest\(ApplicationDispatcher.java:471\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.doForward\(ApplicationDispatcher.java:402\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.access$0\(ApplicationDispatcher.java:333\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:102\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher$PrivilegedForward.run\(ApplicationDispatcher.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationDispatcher.forward\(ApplicationDispatcher.java:321\)",

                    "\tnc.uap.lfw.app.filter.AppFilter.doFilter\(AppFilter.java:52\)",

                    "\tnc.uap.portal.servlet.PortalAppFilter.doFilter\(PortalAppFilter.java:28\)",

                    "\tsun.reflect.GeneratedMethodAccessor745.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\tnc.uap.portal.login.filter.AbstractLfwLoginFilter.doFilter\(AbstractLfwLoginFilter.java:103\)",

                    "\tsun.reflect.GeneratedMethodAccessor700.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\tnc.uap.lfw.core.servlet.LfwRequestListener.doFilter\(LfwRequestListener.java:148\)",

                    "\tsun.reflect.GeneratedMethodAccessor697.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\tnc.uap.lfw.core.servlet.filter.compression.CompressingFilter.doFilter\(CompressingFilter.java:257\)",

                    "\tsun.reflect.GeneratedMethodAccessor713.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\tnc.uap.lfw.core.servlet.LogAroundFilter.doFilter\(LogAroundFilter.java:41\)",

                    "\tsun.reflect.GeneratedMethodAccessor692.invoke\(Unknown Source\)",

                    "\tsun.reflect.DelegatingMethodAccessorImpl.invoke\(DelegatingMethodAccessorImpl.java:25\)",

                    "\tjava.lang.reflect.Method.invoke\(Method.java:597\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:274\)",

                    "\torg.apache.catalina.security.SecurityUtil$1.run\(SecurityUtil.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\tjavax.security.auth.Subject.doAsPrivileged\(Subject.java:517\)",

                    "\torg.apache.catalina.security.SecurityUtil.execute\(SecurityUtil.java:306\)",

                    "\torg.apache.catalina.security.SecurityUtil.doAsPrivilege\(SecurityUtil.java:246\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.internalDoFilter\(ApplicationFilterChain.java:239\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.access$0\(ApplicationFilterChain.java:214\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:193\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain$1.run\(ApplicationFilterChain.java:1\)",

                    "\tjava.security.AccessController.doPrivileged\(Native Method\)",

                    "\torg.apache.catalina.core.ApplicationFilterChain.doFilter\(ApplicationFilterChain.java:188\)",

                    "\torg.apache.catalina.core.StandardWrapperValve.invoke\(StandardWrapperValve.java:224\)",

                    "\torg.apache.catalina.core.StandardContextValve.invoke\(StandardContextValve.java:169\)",

                    "\torg.apache.catalina.authenticator.AuthenticatorBase.invoke\(AuthenticatorBase.java:472\)",

                    "\torg.apache.catalina.core.StandardHostValve.invoke\(StandardHostValve.java:168\)",

                    "\torg.apache.catalina.valves.ErrorReportValve.invoke\(ErrorReportValve.java:98\)",

                    "\torg.apache.catalina.core.StandardEngineValve.invoke\(StandardEngineValve.java:118\)",

                    "\torg.apache.catalina.connector.CoyoteAdapter.service\(CoyoteAdapter.java:407\)",

                    "\torg.apache.coyote.http11.AbstractHttp11Processor.process\(AbstractHttp11Processor.java:987\)",

                    "\torg.apache.coyote.AbstractProtocol$AbstractConnectionHandler.process\(AbstractProtocol.java:539\)",

                    "\torg.apache.tomcat.util.net.JIoEndpoint$SocketProcessor.run\(JIoEndpoint.java:298\)",

                    "\tjava.util.concurrent.ThreadPoolExecutor$Worker.runTask\(ThreadPoolExecutor.java:886\)",

                    "\tjava.util.concurrent.ThreadPoolExecutor$Worker.run\(ThreadPoolExecutor.java:908\)",

                    "\tjava.lang.Thread.run\(Thread.java:619\)"

                \]

            }

        \],

        "header": {

            "srid": "YtWELYpvZc0164342496",

            "pt": "excp",

            "appid": "ztRUFZRPDK0151963951",

            "tid": "RitGmoBwfw0151671866"

        }

    }

\]

