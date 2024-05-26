## Algorithm

[code](/images/temp/haha-2024-05-24.png)

## Review
[How To Use Change Detection Strategy in Angular](https://www.digitalocean.com/community/tutorials/angular-change-detection-strategy)
[angular changeDetectionStrategy](https://angular.dev/guide/components/advanced-configuration#changedetectionstrategy)

在 CDChildComponent 加了 OnPush 表示，在发生异步事件以后触发变化检测，Angular 会跳过这个组件，不会触发这个组件的变化检测。如果 OnPush 是加在某个父组件上，那么这个父组件和它下面所有的子组件都不会触发变化检测。

以下四种情况还是可以触发该组件的变化检测：
1. 组件的@Input引用发生变化
2. Observable 订阅事件，同时设置 Async pipe
3. An event listener in this component runs

利用以下方式手动触发变化检测：

ChangeDetectorRef.detectChanges
ChangeDetectorRef.markForCheck()
ApplicationRef.tick()

## Tip

## Share
