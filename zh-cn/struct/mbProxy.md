## 语法

``` cpp
typedef struct {
  mbProxyType     type;
  char            hostname[100];
  unsigned short  port;
  char            username[50];
  char            password[50];
} mbProxy;
```

## 成员

- **`type`**

  类型：**mbProxyType**

  指向[mbProxyType](/enum/mbProxyType)枚举

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
