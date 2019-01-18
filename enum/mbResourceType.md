# mbResourceType

## 语法

``` cpp
typedef enum {
    MB_RESOURCE_TYPE_MAIN_FRAME     = 0,
    MB_RESOURCE_TYPE_SUB_FRAME      = 1,
    MB_RESOURCE_TYPE_STYLESHEET     = 2,
    MB_RESOURCE_TYPE_SCRIPT         = 3,
    MB_RESOURCE_TYPE_IMAGE          = 4,
    MB_RESOURCE_TYPE_FONT_RESOURCE  = 5,
    MB_RESOURCE_TYPE_SUB_RESOURCE   = 6,
    MB_RESOURCE_TYPE_OBJECT         = 7,
    MB_RESOURCE_TYPE_MEDIA          = 8,
    MB_RESOURCE_TYPE_WORKER         = 9,
    MB_RESOURCE_TYPE_SHARED_WORKER  = 10,
    MB_RESOURCE_TYPE_PREFETCH       = 11,
    MB_RESOURCE_TYPE_FAVICON        = 12,
    MB_RESOURCE_TYPE_XHR            = 13,
    MB_RESOURCE_TYPE_PING           = 14,
    MB_RESOURCE_TYPE_SERVICE_WORKER = 15,
    MB_RESOURCE_TYPE_LAST_TYPE
} mbResourceType;
```

## 枚举

- **`MB_RESOURCE_TYPE_MAIN_FRAME`**

  top level page

- **`MB_RESOURCE_TYPE_SUB_FRAME`**

  frame or iframe

- **`MB_RESOURCE_TYPE_STYLESHEET`**

  a CSS stylesheet

- **`MB_RESOURCE_TYPE_SCRIPT`**

  an external script

- **`MB_RESOURCE_TYPE_IMAGE`**

  an image (jpg/gif/png/etc)

- **`MB_RESOURCE_TYPE_FONT_RESOURCE`**

  a font

- **`MB_RESOURCE_TYPE_SUB_RESOURCE`**

  an "other" subresource.

- **`MB_RESOURCE_TYPE_OBJECT`**

  an object (or embed) tag for a plugin,or a resource that a plugin requested.

- **`MB_RESOURCE_TYPE_MEDIA`**

  a media resource.

- **`MB_RESOURCE_TYPE_WORKER`**

  the main resource of a dedicated worker.

- **`MB_RESOURCE_TYPE_SHARED_WORKER`**

  the main resource of a shared worker.

- **`MB_RESOURCE_TYPE_PREFETCH`**

  an explicitly requested prefetch

- **`MB_RESOURCE_TYPE_FAVICON`**

  a favicon

- **`MB_RESOURCE_TYPE_XHR`**

  a XMLHttpRequest

- **`MB_RESOURCE_TYPE_PING`**

  a ping request for <a ping>

- **`MB_RESOURCE_TYPE_SERVICE_WORKER`**

  the main resource of a service worker.

- **`MB_RESOURCE_TYPE_LAST_TYPE`**

  略
