# mbPopupDialogAndDownloadBind

## 语法

``` cpp
typedef struct _mbPopupDialogAndDownloadBind {
  void*                         ptr;
  mbNetJobDataRecvCallback      recvCallback;
  mbNetJobDataFinishCallback    finishCallback;
  mbPopupDialogSaveNameCallback saveNameCallback;
} mbPopupDialogAndDownloadBind;
```

## 成员

- **`ptr`**

  类型：**void\***

  略

- **`recvCallback`**

  类型：**mbNetJobDataRecvCallback**

  略

- **`finishCallback`**

  类型：**mbNetJobDataFinishCallback**

  略

- **`saveNameCallback`**

  类型：**mbPopupDialogSaveNameCallback**

  略
