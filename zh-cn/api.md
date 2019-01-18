## mbSetMbDllPath

设置mb.dll的全路径+文件名

##### 语法

``` cpp
void mbSetMbDllPath(
  const wchar_t* dllPath
);
```

##### 参数

  <!-- - `dllPath`：dll的全路径，注意是全路径 -->

- **`dllPath`**

  类型：**const wchar_t\***

  dll的全路径，注意是全路径

##### 返回值

类型：**void**


## mbSetMbMainDllPath

设置node.dll的全路径+文件名

##### 语法

``` cpp
void mbSetMbMainDllPath(
  const wchar_t* dllPath
);
```

##### 参数

- **`dllPath`**

  类型：**const wchar_t\***

  dll的全路径，注意是全路径

##### 返回值

类型：**void**

## mbInit

初始化整个mb。<br/>
此句必须在所有mb api前最先调用。<br/>
并且所有mb api必须和调用mbInit的线程为同个线程

##### 语法

``` cpp
void mbInit(
  const mbSettings* settings
);
```

##### 参数

- **`settings`**

  类型：**const mbSettings\***

  指向[mbSettings](#mbSettings)结构的指针

##### 返回值

类型：**void**



## mbSettings

##### 语法

``` cpp
typedef struct {
  mbProxy       proxy;
  mbSettingMask mask;
} mbSettings;
```

##### 成员

- **`proxy`**

  类型：**mbProxy**

  指向[mbProxy](#mbProxy)结构

- **`mask`**

  类型：**unsigned int**

  指向[mbSettingMask](#mbSettingMask)枚举



## mbProxy

##### 语法

``` cpp
typedef struct {
  mbProxyType     type;
  char            hostname[100];
  unsigned short  port;
  char            username[50];
  char            password[50];
} mbProxy;
```

##### 成员

- **`type`**

  类型：**mbProxyType**

  指向[mbProxyType](#mbProxyType)枚举

- **`hostname`**

  类型：**char[100]**

  略

- **`port`**

  类型：**unsigned short**

  略

- **`username`**

  类型：**char[50]**

  略

- **`password`**

  类型：**char[50]**

  略



## mbProxyType

##### 语法

``` cpp
typedef enum {
  MB_PROXY_NONE,
  MB_PROXY_HTTP,
  MB_PROXY_SOCKS4,
  MB_PROXY_SOCKS4A,
  MB_PROXY_SOCKS5,
  MB_PROXY_SOCKS5HOSTNAME
} mbProxyType;
```

##### 枚举

- **`MB_PROXY_NONE`**

  略

- **`MB_PROXY_HTTP`**

  略

- **`MB_PROXY_SOCKS4`**

  略

- **`MB_PROXY_SOCKS4A`**

  略

- **`MB_PROXY_SOCKS5`**

  略

- **`MB_PROXY_SOCKS5HOSTNAME`**

  略



## mbSettingMask

##### 语法

``` cpp
enum mbSettingMask {
  MB_SETTING_PROXY                          = 1,
  MB_SETTING_PAINTCALLBACK_IN_OTHER_THREAD  = 1 << 2,
};
```

##### 枚举

- **`MB_SETTING_PROXY`**

  效果和mbSetProxy一样，通过proxy设置

- **`MB_SETTING_PAINTCALLBACK_IN_OTHER_THREAD`**

  开启时on paint回调会在另外个线程（其实就是渲染线程）。<br/>
  这个是用来实现多线程上屏功能，性能更快。
