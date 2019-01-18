## MiniBlink

> 全球最小的基于chromium的浏览器控件，没有之一

接口是纯C导出，只要使用mb.h、mb.dll、node.dll即可加载，无需.lib。

## 付费版
> **mb.dll**是基于mb的主dll（通常为**node.dll**）之上的一个封装层

在拥有原版主dll的所有能力之外，额外增加了：

- [x] 高性能多线程渲染
- [x] 不同页面独立cookie支持
- [x] MP3\MP4支持
- [x] 加载ActiveX控件
- [x] 网页内开启nodejs能力
- [x] 打印
- [ ] 资源打包
- [ ] 硬件加速

若要使用mb.dll，可以向weolar@qq.com购买，详情可见：[http://miniblink.net/pricing/pricing.htm](http://miniblink.net/pricing/pricing.htm)

另外mb.dll必须依赖node.dll。

升级到新接口注意事项：

- 所有申明改成了`stdcall`
- 其他接口和回调都是在窗口UI线程（以下称主线程）调用，
- 唯独mbOnLoadUrlBegin、mbOnLoadUrlEnd、onDownloadCallback是在另外个线程被回调，请注意保护变量
- 老js相关接口全部被移除，现在统一改成mbRunJs和mbOnJsQuery。
- 打开mtmb.sln后，mtmb\mb.h是mb.dll的导出头文件，Testdll工程是测试工程，需要翻译成c#的代码可以参考这里的代码
- mbGetLockedViewDC后需要调用mbUnlockViewDC
- WM_IME_STARTCOMPOSITION消息直接调用mbFireWindowsMessage派发过去即可
- wkeString等相关结构全部删除
- W相关接口全部删除
- mbOnURLChanged默认就是主frame的url
- URLChanged 回调增加了几个参数

!> 请勿跨线程调用所有接口（除非接口有特殊申明）所有接口如果返回的是**const utf8\***，**const wchar_t\***类型的字符串，均不需要手动释放

## SDK

> MiniBLink 支持使用 `stdcall` 方式调用，可以支持其他语言开发。

**已支持的语言**：
  - [C/C++](https://github.com/weolar/miniblink49/releases) by weolar
  - [C#](https://github.com/E024/MiniBlinkPinvoke) by E024

!> MiniBlink暂时只支持windows系统
