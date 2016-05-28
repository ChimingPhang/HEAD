# HEAD

A collection of HTML head elements.

## Recommended Minimum

下面的代码是极简的网站使用的基本必要标签

```html
<!--页面编码--> 
<meta charset="utf-8"> 
<!--防止IE自动触发兼容性文档视图--> 
<!--http://kinglyhum.iteye.com/blog/827807-->
<meta http-equiv="x-ua-compatible" content="ie=edge"> 
<!--指定viewport大小,响应式页面相关--> 
<!--https://segmentfault.com/a/1190000002685485
<meta name="viewport" content="width=device-width, initial-scale=1">
<!--页面标题--> 
<title>Page Title</title>
```

## Elements

``` html
<title>Page Title</title>
<!-- base标签定义了一个基础的URL用于文档中的所有相对链接-->
<base href="https://example.com/page.html">
<style>
  body { color: red; }
</style>
<script src="script.js"></script>
```

## Meta Element

``` html
<meta charset="utf-8">
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<!-- 上面的3个meta标签 !必须! 在head的最开始。其它的任何标签必须都要在这三个标签的下面 -->
<!-- 声明固定站点的元数据 -->
<!-- https://msdn.microsoft.com/library/gg491732(v=vs.85).aspx#application-name -->
<meta name="application-name" content="Application Name">
<!-- 为页面定义关键字 -->
<meta name="keywords" content="your,keywords,here,comma,separated,no,spaces">
<!-- 页面描述 -->
<meta name="description" content="150 chars">
<!-- 页面主题 -->
<meta name="subject" content="your website's subject">
<!-- 搜索引擎爬虫相关 -->
<!-- http://lcx.cc/?i=3066 -->
<meta name="robots" content="index,follow,noodp">
<meta name="googlebot" content="index,follow">
<!-- 當使用者搜尋您的網站時，Google 搜尋結果有時會顯示您網站的專用搜尋框，以及導向您網站的其他直接連結。這個中繼標記會指示 Google 不要顯示網站連結搜尋框。進一步瞭解網站連結搜尋框 -->
<!-- https://developers.google.com/search/docs/guides/enhance-site#add-a-sitelinks-searchbox-for-your-site -->
<meta name="google" content="nositelinkssearchbox">
<!-- 您可以在網站的頂層網頁中使用這個標記，以向 Search Console 驗證您擁有這個網站。請注意，雖然「name」和「content」屬性的值必須完全符合我們提供給您的內容 (包括大小寫)，但是否將標記由 XHTML 改成 HTML，或者標記的格式是否符合您網頁的格式，則不太要緊 -->
<!-- https://support.google.com/webmasters/answer/35179?rd=1 -->
<meta name="google-site-verification" content="verification_token">
<!-- 搜索结果下方的一段非常简短的描述 -->
<meta name="abstract" content="">
<!-- 网页的话题，被搜索引擎使用 -->
<meta name="topic" content="">
<!-- 网页的概要，被某些搜索引擎使用 -->
<meta name="summary" content="">
<!-- 网页的类别 -->
<meta name="classification" content="business">
<!-- 网页路径，被搜索引擎使用 -->
<meta name="url" content="https://example.com/">

<!-- 过时，或者非流行标签 -->
<meta name="identifier-URL" content="https://example.com/">
<meta name="directory" content="submission">
<meta name="category" content="">

<!-- 网页服务的范围（地理） 类似 CN|UK|USA ,某些搜索引擎使用-->
<meta name="coverage" content="Worldwide">
<!-- 网页分配程度 Global 完全公开 Local 本地使用 IU 内部使用，不共享 -->
<meta name="distribution" content="Global">
<!-- 网页分级 general 一般 mature 成年 restricted 限制级 14 years 14岁以上safe for kids 全年龄 -->
<meta name="rating" content="General">
<!-- 在html中控制http请求来源 -->
<!-- https://w3c.github.io/webappsec-referrer-policy/ -->
<meta name="referrer" content="never">
<!-- 阻止不安全的脚本 -->
<!-- http://www.html5rocks.com/en/tutorials/security/content-security-policy/ -->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">
```

### Not Recommended
下面的meta属性是不推荐使用的

```html
<!-- 过去用来确定网页的语言，但是并没有得到良好支持，使用<html lang=""> 来代替更好一点 -->
<meta name="language" content="en">

<!-- 没有任何证据表明有任意一个搜索引擎在使用这个标签 -->
<meta name="revised" content="Sunday, July 18th, 2010, 5:15 pm">

<!-- 一种简单的防范邮箱提取机器人的办法 -->
<meta name="reply-to" content="email@example.com">

<!-- 使用<link rel="author">或者humans.txt文件更好一点 -->
<!-- http://www.zhangxinxu.com/wordpress/2011/01/humans-txt-%E7%BD%91%E7%AB%99%E7%9B%B8%E5%85%B3%E4%BA%BA%E5%91%98%E4%BF%A1%E6%81%AF%E8%AE%B0%E5%BD%95%E7%9A%84idea/?replytocom=10950 -->
<meta name="author" content="name, email@example.com">
<meta name="designer" content="">
<meta name="owner" content="">

<!-- 告诉搜索引擎多长时间以后重新访问该网页，但是这并没有得到支持，因为大多数搜索引擎都是在一段随机时间以后重新访问 -->
<meta name="revisit-after" content="7 days">

<!-- 谷歌强烈建议不使用此标签，而是配置好服务端，类似Apache和nginx -->
<meta http-equiv="refresh" content="300;url=https://example.com/">

<!-- 缓存控制 -->
<!-- 最好在服务端控制缓存 -->
<meta http-equiv="Expires" content="0">
<meta http-equiv="Pragma" content="no-cache">
<meta http-equiv="Cache-Control" content="no-cache">
```

## Link Element

``` html
<!-- 网页的版权声明 -->
<link rel="copyright" href="copyright.html">
<!-- 连接网页使用的CSS文件 -->
<link rel="stylesheet" href="https://example.com/styles.css">
<!-- RSS feed 连接 -->
<!-- https://developer.mozilla.org/en-US/docs/Web/RSS/Getting_Started/Syndicating -->
<link rel="alternate" href="https://feeds.feedburner.com/martini" type="application/rss+xml" title="RSS">
<!-- ATOM feed 连接 -->
<!-- http://www.xml.com/pub/a/2004/06/16/dive.html -->
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">
<!-- 提供正確語言和地區的網址 -->
<!-- https://support.google.com/webmasters/answer/189077?hl=zh-Hant -->
<link rel="alternate" href="https://es.example.com/" hreflang="es">

<!-- 个人主页的连接 -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<!-- 发送邮件给我 -->
<link rel="me" href="mailto:name@example.com">
<!-- 发送短信给我 -->
<link rel="me" href="sms:+15035550125">
<!-- 描述了一些可以归类的内容的集合，需要在服务端自行处理 -->
<link rel="archives" href="https://example.com/2003/05/" title="May 2003">
<!-- SEO相关  -->
<!-- https://www.w3.org/TR/2011/WD-html5-20110113/links.html -->
<link rel="index" href="https://example.com/" title="DeWitt Clinton">
<link rel="start" href="https://example.com/photos/
pattern_recognition_1_about/" title="Pattern Recognition 1">
<link rel="prev" href="https://example.com/opensearch/opensearch-and-openid-a-sure-way-to-get-my-attention/" title="OpenSearch and OpenID? A sure way to get my attention.">
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">
<link rel="self" type="application/atom+xml" href="https://example.com/atomFeed.php?page=3">
<link rel="first" href="https://example.com/atomFeed.php">
<link rel="next" href="https://example.com/atomFeed.php?page=4">
<link rel="previous" href="https://example.com/atomFeed.php?page=2">
<link rel="last" href="https://example.com/atomFeed.php?page=147">
<link rel="shortlink" href="https://example.com/?p=43625">
<link rel="canonical" href="https://example.com/2010/06/9-things-to-do-before-entering-social-media.html">
<link rel="amphtml" href="https://www.example.com/url/to/amp-version.html">
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">
<link rel="pingback" href="https://example.com/xmlrpc.php">
<link rel="webmention" href="https://example.com/webmention">
<link rel="manifest" href="manifest.json">
<link rel="author" href="humans.txt">
<link rel="import" href="component.html">

<!-- 网页预处理 -->
<!-- https://w3c.github.io/resource-hints/ -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="subresource" href="styles.css">
<link rel="preload" href="image.png">
<!-- More info: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
```

### Not Recommended
下面是不推荐使用的link标签:

```html
<link rel="shortcut icon" href="path/to/favicon.ico">
```

### Favicons

``` html
<!-- IE10及以下 -->
<!-- 不需要link标签 , 只需要将favicon.ico文件放在网站的根目录-->

<!-- For IE 11, Chrome, Firefox, Safari, Opera -->
<link rel="icon" href="path/to/favicon-16.png" sizes="16x16" type="image/png">
<link rel="icon" href="path/to/favicon-32.png" sizes="32x32" type="image/png">
<link rel="icon" href="path/to/favicon-48.png" sizes="48x48" type="image/png">
<link rel="icon" href="path/to/favicon-62.png" sizes="62x62" type="image/png">
<!-- More info: https://bitsofco.de/all-about-favicons-and-touch-icons/ -->
```

- [All About Favicons (And Touch Icons)](https://bitsofco.de/all-about-favicons-and-touch-icons/)

## Social

### OEmbed

``` html
<link rel="alternate" type="application/json+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
  title="oEmbed Profile: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
  title="oEmbed Profile: XML">
```

- [oEmbed format](http://oembed.com/)

### Facebook / Open Graph

``` html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
<!-- Facebook: https://developers.facebook.com/docs/sharing/webmasters#markup -->
<!-- Open Graph: http://ogp.me/ -->
```

- [Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup)
- [Open Graph protocol](http://ogp.me/)

### Facebook / Instant Articles

``` html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- The URL of the web version of your article -->
<link rel="canonical" href="http://example.com/article.html">

<!-- The style to be used for this article -->
<meta property="fb:article_style" content="myarticlestyle">
```

- [Facebook Instant Articles: Creating Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- [Instant Articles: Format Reference](https://developers.facebook.com/docs/instant-articles/reference)  

### Twitter

``` html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
<!-- More info: https://dev.twitter.com/cards/getting-started -->
<!-- Validate: https://dev.twitter.com/docs/cards/validation/validator -->
```

- [Twitter Cards: Getting Started Guide](https://dev.twitter.com/cards/getting-started)
- [Twitter Card Validator](https://dev.twitter.com/docs/cards/validation/validator)

### Google+ / Schema.org

``` html
<link href="https://plus.google.com/+YourPage" rel="publisher">
<meta itemprop="name" content="Content Title">
<meta itemprop="description" content="Content description less than 200 characters">
<meta itemprop="image" content="https://example.com/image.jpg">
```

## Browser/Platform


### Apple iOS

``` html
<!-- 在网页中，显示你的iOS应用的信息 -->
<!-- http://smartappbanners.com/ -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- 禁止自动检测格式 -->
<meta name="format-detection" content="telephone=no">

<!-- 添加到桌面  -->
<!-- https://developer.apple.com/library/ios/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="apple-mobile-web-app-title" content="App Title">

<!-- 图标 -->
<link rel="apple-touch-icon" href="apple-touch-icon.png">
<link rel="apple-touch-icon-precomposed" href="apple-touch-icon-precomposed.png">
<!-- 一般情况下, 一个 180×180px的图标就够了 -->
<!-- 如果你需要在每种设备中使用不同的图标的话，那么你可以在这里添加更多 -->

<!-- 启动时显示的图片 -->
<link rel="apple-touch-startup-image" href="startup.png">

<!-- More info: https://developer.apple.com/safari/library/documentation/appleapplications/reference/safarihtmlref/articles/metatags.html -->
```

- [Apple Meta Tags](https://developer.apple.com/library/safari/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

### Apple Safari

```html
<!-- 在Safari浏览器中显示网站图标 -->
<!-- https://yoast.com/dev-blog/safari-pinned-tab-icon-mask-icon/ -->
<link rel="mask-icon" href="icon.svg" color="red">
```

### Google Android

``` html
<!-- 设置Android系统中的工具栏颜色 -->
<!-- https://developers.google.com/web/updates/2014/11/Support-for-theme-color-in-Chrome-39-for-Android -->
<meta name="theme-color" content="#E64545">

<!-- 可以添加到桌面 -->
<meta name="mobile-web-app-capable" content="yes">
<!-- More info: https://developer.chrome.com/multidevice/android/installtohomescreen -->
```

### Google Chrome

``` html
<!-- 链接到Chrome应用商店里面的应用 -->
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- 禁止自动提示翻译 -->
<meta name="google" value="notranslate">
```

### Microsoft Internet Explorer

``` html
<!--防止自动触发兼容性文档视图--> 
<!--http://kinglyhum.iteye.com/blog/827807-->
<meta http-equiv="x-ua-compatible" content="ie=edge">
<!-- 禁用windows的cleartype -->
<meta http-equiv="cleartype" content="on">
<!-- 启用skype的工具栏 -->
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- 在Windows Phone的IE 10中 禁用链接高亮显示(https://blogs.windows.com/buildingapps/2012/11/15/adapting-your-webkit-optimized-site-for-internet-explorer-10/) -->
<meta name="msapplication-tap-highlight" content="no">

<!-- IE的webapp 配置 (https://msdn.microsoft.com/en-us/library/dn255024(v=vs.85).aspx) -->
<meta name="application-name" content="Contoso Pinned Site Caption">
<meta name="msapplication-tooltip" content="Example Tooltip Text">
<meta name="msapplication-starturl" content="/">

<meta name="msapplication-config" content="http://example.com/browserconfig.xml">

<meta name="msapplication-allowDomainApiCalls" content="true">
<meta name="msapplication-allowDomainMetaTags" content="true">
<meta name="msapplication-badge" content="frequency=30; polling-uri=http://example.com/id45453245/polling.xml">
<meta name="msapplication-navbutton-color" content="#FF3300">
<meta name="msapplication-notification" content="frequency=60;polling-uri=http://example.com/livetile">
<meta name="msapplication-square150x150logo" content="images/logo.png">
<meta name="msapplication-square310x310logo" content="images/largelogo.png">
<meta name="msapplication-square70x70logo" content="images/tinylogo.png">
<meta name="msapplication-wide310x150logo" content="images/widelogo.png">
<meta name="msapplication-task" content="name=Check Order Status;action-uri=./orderStatus.aspx?src=IE9;icon-uri=./favicon.ico">
<meta name="msapplication-task-seperator" content="1">
<meta name="msapplication-TileColor" content="#FF3300">
<meta name="msapplication-TileImage" content="images/tileimage.jpg">
<meta name="msapplication-window" content="width=1024;height=768">
```

### Microsoft Internet Explorer (远古遗物，请勿使用)

``` html
<!-- 在ie6中禁用图片工具栏当你的鼠标指针在图片之上 (https://msdn.microsoft.com/en-us/library/ms532986(v=vs.85).aspx) -->
<meta http-equiv="imagetoolbar" content="no">

<!-- 禁用输入框和按钮的windows主题化 (https://support.microsoft.com/en-us/kb/322240) -->
<meta name="MSThemeCompatible" content="no">

<!-- 禁用只有在IE 6 beta中的功能 (https://stackoverflow.com/q/2167301) -->
<meta name="MSSmartTagsPreventParsing" content="true">

<!-- 页面跳转 (https://msdn.microsoft.com/en-us/library/ms532847(v=vs.85).aspx) -->
<meta http-equiv="Page-Enter" content="revealtrans(duration=2,transition=2)">
<meta http-equiv="Page-Exit" content="revealtrans(duration=3,transition=12)">
<meta http-equiv="Site-Enter" content="revealtrans(duration=2,transition=2)">
<meta http-equiv="Site-Exit" content="revealtrans(duration=3,transition=12)">
```

### 360 Browser

``` html
<!-- 选择需要使用的渲染引擎 -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### UC Mobile Browser

``` html
<!-- 锁定屏幕显示方向 -->
<meta name="screen-orientation" content="landscape/portrait">
<!-- 全屏显示此页面 -->
<meta name="full-screen" content="yes">
<!-- 即使在文字模式下也显示图片 -->
<meta name="imagemode" content="force">
<!-- 页面将以应用模式显示 比方说(全屏,手势, 等等) -->
<meta name="browsermode" content="application">
<!-- 在页面中禁用UC浏览器的夜间模式 -->
<meta name="nightmode" content="disable">
<!-- Layoutmode的取值为fitscreen(对应适应屏幕)或standard(对应标准模式)
Onlayoutchange函数将在用户通过菜单切换排版方式时被调用，对每个窗口通知其网页排版发生了变化。
当时用meta标签定义了该页面的排版方式后，该页面的排版将不再受用户的菜单排版方式选择影响。 -->
<meta name="layoutmode" content="fitscreen">
<!-- 在页面中有很多文字时，禁用UC浏览器的自动调整字体功能 -->
<meta name="wap-font-scale" content="no">
```

- [UC Browser Docs](http://www.uc.cn/download/UCBrowser_U3_API.doc)

### QQ Mobile Browser

``` html
<!-- 锁定屏幕显示方向 -->
<meta name="x5-orientation" content="landscape/portrait">
<!-- 全屏显示此页面 -->
<meta name="x5-fullscreen" content="true">
<!-- 页面将以应用模式显示 比方说(全屏,手势, 等等) -->
<meta name="x5-page-mode" content="app">
```

## App Links

``` html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">
<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">
<!-- Web Fallback -->
<meta property="al:web:url" content="http://applinks.org/documentation">
<!-- More info: http://applinks.org/documentation/ -->
```

- [App Links Docs](http://applinks.org/documentation/)

## Other Resources

- [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

## Contributing

Open an issue or a pull request to suggest changes or additions.

## Author

**[Josh Buchea](http://joshbuchea.com/)**

**[Esimorp](https://github.com/Esimorp)**

## License

[MIT License](LICENSE)
