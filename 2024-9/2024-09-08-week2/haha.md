## Algorithm

[code](/images/temp/haha-2024-09-08.png)

## Review

[defer in angular](https://angular.dev/guide/templates/defer)

```
@defer (on hover) {
  <large-component />
} @loading {
  <img alt="loading..." src="loading.gif" />
} @placeholder {
  <p>Placeholder content</p>
} @error {
  <p>Failed to load large component.</p>
}
```

By default, defer blocks do not render any content before they are triggered.

The @placeholder is an optional block that declares what content to show before the @defer block is triggered.

The idle trigger loads the deferred content once the browser has reached an idle state, based on requestIdleCallback. This is the default behavior with a defer block.

@defer blocks are compatible with both standalone and NgModule-based components, directives and pipes. However, only standalone components, directives and pipes can be deferred. NgModule-based dependencies are not deferred and are included in the eagerly loaded bundle.

## Tip

## Share
