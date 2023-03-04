## Algorithm

![code](/images/temp/haha-2023-03-04.png)

## Review

[How to start zone-less Angular app](https://medium.com/@kamil.galek/mythical-angular-tutorial-how-to-start-zone-less-angular-app-ff19107290bf)

禁用 zone.js

```
import {enableProdMode} from '@angular/core';
import {platformBrowserDynamic} from '@angular/platform-browser-dynamic';

import {AppModule} from './app/app.module';
import {environment} from './environments/environment';

if (environment.production) {
  enableProdMode();
}

const compilerOptions = {
  ngZone: 'noop' as 'noop'
};

platformBrowserDynamic().bootstrapModule(AppModule, compilerOptions)
  .catch(err => console.error(err));
```

这样可以做一个 zone-less application， 可以看到没有 zone 包裹的源码，但是 Async pipe 不能在没有 zone.js 的情况下工作

## Tip

## Share

[improve angular performance share](https://medium.com/@guillaume-ferber/maximizing-performance-with-angular-tips-and-tricks-for-efficient-code-76939fe7333b)
