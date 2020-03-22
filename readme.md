# September UI

For more info check the official site: http://september-ui.herokuapp.com/

**September UI** is a set of Vue components created to be customized to adapt to the unique design for your application.

It uses [TailwindCss](https://tailwindcss.com/) classes by default. No more Bootstrap like sites.

# Installation &amp; Usage

### 1. Install the dependencies

```bash
npm install septemberui --save
```

::: tip
If you using the default theme you need to install TailwindCSS first
:::

### 2. Configure your project to use septemberui in your sfc (single file component)

```vue
<template>
  <div>
    <alert>This is a alert</alert>
  </div>
</template>

<script>
import { Alert } from "septemberui";

export default {
  components: {
    Alert
  }
};
</script>
```

### Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

### Security

If you discover any security related issues, please email [abhisheksarmah660@gmail.com](mailto:abhisheksarmah660@gmail.com) instead of using the issue tracker.

## Credits

- [Abhishek Sarmah](https://github.com/abhisheksarmah)
- [Mithicher Baro](https://github.com/mithicher)
