# Growl-Notification

- 内置漂亮的 UI 效果和多种主题、
- 轻量级，压缩后只有 18K。
- 纯 js 编写，没有任何依赖。
- 支持 IE11+, Safari, Google Chrome, Yandex Browser, Opera, Firefox。

## 预览

https://c3p7f2.github.io/pages/growl-notification

## 使用方法

在页面中引入下面的文件。

```
<link href="light-theme.min.css" rel="stylesheet">
<script src='growl-notification.min.js'></script>
```

CDN

```
<link href="https://cdn.jsdelivr.net/gh/c3p7f2/growl-notification@main/light-theme.min.css" rel="stylesheet">
<script src='https://cdn.jsdelivr.net/gh/c3p7f2/growl-notification@main/growl-notification.min.js'></script>
```

## 创建通知

```
GrowlNotification.notify({
    title: 'This is title',
    description: 'My Description'
});
```

### 配置参数

```
GrowlNotification.notify({
    margin: 20,
    type: 'default',
    title: '',
    description: '',
    image: {
        visible: false,
        customImage: ''
    },
    closeTimeout: 0,
    closeWith: ['click', 'button'],
    animation: {
        open: 'slide-in',
        close: 'slide-out'
    },
    animationDuration: .2,
    position: 'top-right',
    showBorder: false,
    showButtons: false,
    buttons: {
        action: {
            text: 'Ok',
            callback: function() {}
        },
        cancel: {
            text: 'Cancel',
            callback: function() {}
        }
    },
    showProgress: false
});
```

 <table class="table">
            <thead>
            <tr>
                <th>Option</th>
                <th>Default</th>
                <th>Info</th>
            </tr>
            </thead>
            <tbody>
            <tr>
                <td><strong>width</strong>: number|string</td>
                <td>null</td>
                <td>Custom width for notification 100px, 50% and etc.</td>
            </tr>
            <tr>
                <td><strong>zIndex</strong>: number</td>
                <td>1056</td>
                <td>Custom z-index for notifications</td>
            </tr>
            <tr>
                <td><strong>type</strong>: string</td>
                <td>'alert'</td>
                <td>alert, success, error, warning, info</td>
            </tr>
            <tr>
                <td><strong>position</strong>: string</td>
                <td>'top-right'</td>
                <td>top-left, top-right, bottom-left, bottom-right, top-center, bottom-center</td>
            </tr>
            <tr>
                <td><strong>title</strong>: string</td>
                <td>''</td>
                <td>This string can contain HTML too. But be careful and don't pass user inputs to this parameter.</td>
            </tr>
            <tr>
                <td><strong>description</strong>: string</td>
                <td>''</td>
                <td>This string can contain HTML too. But be careful and don't pass user inputs to this parameter.</td>
            </tr>
            <tr>
                <td><strong>image.visible</strong>: boolean</td>
                <td>false</td>
                <td>Show/Hide image</td>
            </tr>
            <tr>
                <td><strong>image.customImage</strong>: string</td>
                <td>''</td>
                <td>Path to custom image</td>
            </tr>
            <tr>
                <td><strong>closeTimeout</strong>: boolean,int</td>
                <td>false</td>
                <td>false, 1000, 3000, 3500, etc. Delay for closing event in milliseconds (ms). Set 'false' for sticky notifications.</td>
            </tr>
            <tr>
                <td><strong>closeWith</strong>: [...string]</td>
                <td>['click']</td>
                <td>click, button</td>
            </tr>
            <tr>
                <td><strong>animation.open</strong>: string,null,false</td>
                <td>'slide-in'</td>
                <td>If <strong>string</strong>, assumed to be CSS class name. If <strong>false|null|'none'</strong>, no animation at all. 'slide-in', 'fade-in'</td>
            </tr>
            <tr>
                <td><strong>animation.close</strong>: string,null,false</td>
                <td>'slide-out'</td>
                <td>If <strong>string</strong>, assumed to be CSS class name. If <strong>false|null|'none'</strong>, no animation at all. 'slide-out', 'fade-out'</td>
            </tr>
            <tr>
                <td><strong>showButtons</strong>: true,false</td>
                <td>false</td>
                <td>Show or hide buttons</td>
            </tr>
            <tr>
                <td><strong>buttons</strong>: object</td>
<td><pre><code>buttons: {
    action: {
        text: 'Ok',
        callback: function {} // callback
    },
    cancel: {
        text: 'Cancel',
        callback: function {} // callback
    }
}</code></pre>
                </td>
                <td>Buttons configuration</td>
            </tr>
            <tr>
                <td><strong>showProgress</strong>: true,false</td>
                <td>false</td>
                <td>Show or hide progress bar</td>
            </tr>
            <tr>
                <td><strong>GrowlNotification.setGlobalOptions</strong>: object</td>
                <td>{}</td>
                <td>Set global options for all notifications</td>
            </tr>
            <tr>
                <td><strong>GrowlNotification.closeAll</strong></td>
                <td>-</td>
                <td>Close all notifications</td>
            </tr>
            </tbody>
        </table>
