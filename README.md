# WebView
1.创建activity_webview.xml，在其中添加一个webview组件

2.在MainActivity中指定view为activity_browser.xml，并使用getIntent()方法获取Intent，再获取data，通过data.getScheme(), data.getHost(), data.getPath()这三个方法分别获取协议、主机名和路径，并作为Url对象的参数。 还需要重新设置WebViewClien对象，并重写该对象的shouldOverrideUrlLoading()方法来防止再使用第webView以外的第三方浏览器。

3.在AndroidManifest.xml文件中注册BrowserActivity，设置其意图过滤器。还要添加uses-permission来使用网络。category.DEFAULT一定要设置，不然在选择浏览器时看不到该应用。

![image](https://github.com/wuji-coder/WebView/blob/master/image/WebView.png)
