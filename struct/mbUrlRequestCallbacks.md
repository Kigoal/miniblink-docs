# mbUrlRequestCallbacks

## 语法

``` cpp
typedef struct _mbUrlRequestCallbacks {
  mbOnUrlRequestWillRedirectCallback        willRedirectCallback;
  mbOnUrlRequestDidReceiveResponseCallback  didReceiveResponseCallback;
  mbOnUrlRequestDidReceiveDataCallback      didReceiveDataCallback;
  mbOnUrlRequestDidFailCallback             didFailCallback;
  mbOnUrlRequestDidFinishLoadingCallback    didFinishLoadingCallback;
} mbUrlRequestCallbacks;
```

## 成员

- **`willRedirectCallback`**

  类型：**mbOnUrlRequestWillRedirectCallback**

  略

- **`didReceiveResponseCallback`**

  类型：**mbOnUrlRequestDidReceiveResponseCallback**

  略

- **`didReceiveDataCallback`**

  类型：**mbOnUrlRequestDidReceiveDataCallback**

  略

- **`didFailCallback`**

  类型：**mbOnUrlRequestDidFailCallback**

  略

- **`didFinishLoadingCallback`**

  类型：**mbOnUrlRequestDidFinishLoadingCallback**

  略
