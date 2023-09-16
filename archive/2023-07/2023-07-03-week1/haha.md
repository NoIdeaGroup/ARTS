## Algorithm

[code](/images/temp/haha-2023-07-09.png)

## Review

[pdfmake](https://pdfmake.github.io/docs/0.1/)

做 checkbox 两列 的效果，需要由这样的结构：

```
[
    {
        column: [
            {this.generateCheckbox()}, // 给个固定宽度，margin，使用 svg
            {this.generateText()} // text 如果换行最好给个宽度；如果设置为*，会超出格子
        ]
    }
]
```

## Tip

## Share

[about pdfmake](https://medium.com/@rakeshuce1990/ionic-how-to-create-pdf-file-with-pdfmake-step-by-step-75b25aa541a4)
