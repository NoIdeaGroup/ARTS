## Algorithm

[code](/images/temp/haha-2024-03-17.png)

## Review

[ViewChild and ViewChildren in angular](https://blog.logrocket.com/understanding-the-viewchild-and-viewchildren-decorators-in-angular-10/)
[ViewChild and contentChild in Angular](https://medium.com/@hish.abdelshafouk/viewchild-and-contentchild-in-angular-57bd48e3e835#:~:text=%40ViewChild%20and%20%40ContentChild%20in%20Angular%20offer%20powerful%20means,a%20parent%20component%20into%20a%20child%20using%20%3Cng-content%3E/)

ContentChild 用来从通过 Content Projection 方式 (ng-content) 设置的视图中获取匹配的元素
ViewChild 用来从模板视图中获取匹配的元素

在父组件的 ngAfterContentInit 生命周期钩子中才能成功获取通过 ContentChild 查询的元素
在父组件的 ngAfterViewInit 生命周期钩子中才能成功获取通过 ViewChild 查询的元素

## Tip

## Share
