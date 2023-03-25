
<h1> Modules:</h1> 
Use of native JavaScript modules is dependent on the <b>import and export</b> statements; these are supported in browsers as shown in the compatibility table below.

Exporting module features
The first thing you do to get access to module features is export them. This is done using the export statement.

The easiest way to use it is to place it in front of any items you want exported out of the module, for example:

```javascript
export const name = "square";

export function draw(ctx, length, x, y, color) {
  ctx.fillStyle = color;
  ctx.fillRect(x, y, length, length);

  return { length, x, y, color };
}
```

You can export functions, var, let, const, and — as we'll see later — classes. They need to be top-level items; you can't use export inside a function, for example.

A more convenient way of exporting all the items you want to export is to use a single export statement at the end of your module file, followed by a comma-separated list of the features you want to export wrapped in curly braces. For example:

```javascript
export { name, draw, reportArea, reportPerimeter };
```

Once you've exported some features out of your module, you need to import them into your script to be able to use them. The simplest way to do this is as follows:
```javascript
import { name, draw, reportArea, reportPerimeter } from "./modules/square.js";
```
You use the import statement, followed by a comma-separated list of the features you want to import wrapped in curly braces, followed by the keyword from, followed by the module specifier.
