# mbNetSetData

调用此函数后,网络层收到数据会存储在一buf内,接收数据完成后响应OnLoadUrlEnd事件.#此调用严重影响性能,慎用<br/>
此函数和mbNetSetData的区别是，mbNetHookRequest会在接受到真正网络数据后再调用回调，并允许回调修改网络数据。<br/>
而mbNetSetData是在网络数据还没发送的时候修改

## 语法

``` cpp
void mbNetSetData(
  mbNetJob  job,
  void*     buf,
  int       len
);
```

## 参数

- **`job`**

  类型：**mbNetJob**

  略

- **`buf`**

  类型：**void\***

  略

- **`len`**

  类型：**int**

  略

## 返回值

类型：**void**
