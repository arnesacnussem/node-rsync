# node-rsync

Rsync wrapper

Modified from [@kyleaupton/node-rsync](https://github.com/kyleaupton/node-rsync)

> **_NOTE:_**  Requires rsync version `3.1.0` or greater

# Features
* Progress reporting
* Typed rsync options
* Set custom executable path
* ESM exports
* use [execa](https://github.com/sindresorhus/execa)

# Install

```bash
yarn add node-rsync@
```

# Example

```javascript
import { setPath, copy } from '@kyleupton/node-rsync'

setPath('/opt/homebrew/Cellar/rsync/3.2.7_1/bin/rsync')

const res = await copy({
  source: '/Users/kyleupton/Downloads/',
  destination: '/Users/kyleupton/Documents/dest/',
  options: {
    archive: true
  },
  onProgress: (progress) => {
    console.log(progress)
  }
})
```
