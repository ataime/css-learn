# 项目名称

这是一个关于如何在 GitHub README 中添加动画的示例。

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        * {
            padding: 0;
            margin: 0;
        }

        body {
            width: 100vw;
            height: 100vh;
            background: #34495e;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        main {
            width: 100px;
            height: 100px;
            background: white;
            /*使用关键帧*/
            animation-name: hd;
            animation-duration: 10s;
        }

        /* 定义关键帧 */
        @keyframes hd {
            from {
                background: white;
            }

            10% {
                transform: scale(2);
            }

            to {
                background: red;
            }
        }
    </style>
</head>

<body>
    <main></main>
</body>

</html>
```
演示：
![演示动画](css1.gif)
