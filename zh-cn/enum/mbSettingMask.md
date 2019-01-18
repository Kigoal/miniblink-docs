## 语法

``` cpp
enum mbSettingMask {
  MB_SETTING_PROXY                          = 1,
  MB_SETTING_PAINTCALLBACK_IN_OTHER_THREAD  = 1 << 2,
};
```

## 枚举

- **`MB_SETTING_PROXY`**

  效果和mbSetProxy一样，通过proxy设置

- **`MB_SETTING_PAINTCALLBACK_IN_OTHER_THREAD`**

  开启时on paint回调会在另外个线程（其实就是渲染线程）。<br/>
  这个是用来实现多线程上屏功能，性能更快。
