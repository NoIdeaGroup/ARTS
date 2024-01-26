## Algorithm

[code](/images/temp/haha-2024-01-21.png)

## Review

[use inject in angular](https://medium.com/netanelbasal/understanding-angular-injection-context-18a0780ede2d)
[Inject different Service into a Service](https://medium.com/@kelly-kh-woo/angular-inject-different-service-to-service-522abbcc960a)

```
//  We can use this function if we have code that relies on the inject() function and we want to verify that the consumer is using it where an injector is available


export function injectNativeElement<T extends Element>(): T {
  assertInInjectionContext(injectNativeElement);

  return inject(ElementRef).nativeElement;
}
```

## Tip

## Share
