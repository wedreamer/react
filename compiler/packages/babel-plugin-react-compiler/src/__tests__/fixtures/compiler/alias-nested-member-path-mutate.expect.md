
## Input

```javascript
function component() {
  let z = [];
  let y = {};
  y.z = z;
  let x = {};
  x.y = y;
  mutate(x.y.z);
  return x;
}

```

## Code

```javascript
import { c as _c } from "react/compiler-runtime";
function component() {
  const $ = _c(1);
  let t0;
  if ($[0] === Symbol.for("react.memo_cache_sentinel")) {
    const z = [];
    const y = {};
    y.z = z;
    const x = {};
    x.y = y;

    t0 = x;
    mutate(x.y.z);
    $[0] = t0;
  } else {
    t0 = $[0];
  }
  return t0;
}

```
      