初始化整个mb。<br/>
此句必须在所有mb api前最先调用。<br/>
并且所有mb api必须和调用mbInit的线程为同个线程

## 语法

``` cpp
void mbInit(
  const mbSettings* settings
);
```

## 参数

- **`settings`**

  类型：**const mbSettings\***

  指向[mbSettings](/struct/mbSettings)结构的指针

## 返回值

类型：**void**
