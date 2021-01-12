# Require.js integration with a Font Awesome Kit

To run the example:

```
npm install
npm run serve
```

Open `http://127.0.0.1:8080/` (unless it detects a different port to use)

## How does this work?

The Font Awesome Kit defines a module named "kit-loader".

So we first configure Require.js to map this name to a Kit.

In this example our Kit token is 'https://kit.fontawesome.com/1173dadc54'

```html
<script>
  requirejs.config({
    paths: {
      'kit-loader': 'https://kit.fontawesome.com/1173dadc54'
    }
  })
</script>
```

Note that there is no ".js" at the end of the Kit URL. Require.js adds this
automatically so you don't need to.

To load the Kit we need to reference "kit-loader" somewhere in your app:

```
requirejs(["kit-loader", "helper/util"], function(_, util) {
  util.hello();
});
```
