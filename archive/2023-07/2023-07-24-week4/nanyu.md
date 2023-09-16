## Algorithm

![leetcode](https://file.notion.so/f/s/3835bc83-e112-4ecb-b182-3835674c45e3/Untitled.png?id=9e0e7b0c-e461-4f5b-b8b4-769f32251802&table=block&spaceId=8245be63-084e-4231-9b7f-5a28286bec7b&expirationTimestamp=1690646400000&signature=jhe2oXQRnNy8-DT-7KMhY4CRDh2KOdaAA5R2AphvAhA&downloadName=Untitled.png)

## Review

### **[Decoupling UI and Logic in React: A Clean Code Approach with Headless Components](https://itnext.io/decoupling-ui-and-logic-in-react-a-clean-code-approach-with-headless-components-82e46b5820c)**

## Tip

最近在项目中的一个工具页面上，遇到了 JS 的时区问题。当 Date 类型的数据转为 json 时，默认是 UTC+0 的时区，而我们是 UTC+8 的时区。虽然可以
每次看数据的时候，人为得加 8 个小时，但是始终不太方便。

这里我使用了 [Momentjs](https://momentjs.com/) 来做时间转换，非常得方便。常见时间格式用法如下：
```javascript
let now = new Date()
moment().format(now, 'YYYY-MM-DD HH:mm:ss.SSS')
```

## Share

无