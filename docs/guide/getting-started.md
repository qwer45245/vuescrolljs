---
sidebarDepth: 1
---

# Getting Started

## Quick Start

### Module System

#### Installation

```bash
 npm i vuescroll -S
 # or use yarn
 # yarn add vuescroll
```

#### Import

1. import globally

In your entry file:

```javascript
import Vue from 'vue';
import vuescroll from 'vuescroll';
import 'vuescroll/dist/vuescroll.css';

Vue.use(vuescroll);
```

2. import locally

```html
<template>
  <vue-scroll> <!-- Your content... --> </vue-scroll>
</template>
<script>
  import vuescroll from 'vuescroll';
  import 'vuescroll/dist/vuescroll.css';

  export default {
    components: {
      vuescroll
    }
  };
</script>
```

#### Only import the mode you need.

**Only import the features of slide mode:**

```javascript
import Vue from 'vue';
import vuescroll from 'vuescroll/dist/vuescroll-slide';
import 'vuescroll/dist/vuescroll.css';

Vue.use(vuescroll);
```

**Only import the features of native mode:**

```javascript
import Vue from 'vue';
import vuescroll from 'vuescroll/dist/vuescroll-native';
import 'vuescroll/dist/vuescroll.css';

Vue.use(vuescroll);
```

### Browser Environment

#### Direct import via CDN

```html
<script src="https://unpkg.com/vue"></script>
<script src="https://unpkg.com/vuescroll"></script>
<!-- import vuescroll-slide -->
<script src="https://unpkg.com/vuescroll/dist/vuescroll-slide.js"></script>
<!-- import vuescroll-native -->
<script src="https://unpkg.com/vuescroll/dist/vuescroll-native.js"></script>
<link
  rel="stylesheet"
  type="text/css"
  href="https://unpkg.com/vuescroll/dist/vuescroll.css"
/>
```

### Usage

> Put it outside the `child element`, inside the `parent element`. Just so easy.

::: warning
If you doesn't see scrollbar show, please open `dev-tool` to checkout whether your child's size is greater than parent's.The condition for the scrollbar to appear is the same as the native scrollbar, that is, **the size of the child element exceeds the parent element**.

:::

```html
<template>
  <div class="parent-element">
    <!-- bind your configurations -->
    <vue-scroll :ops="ops"> <div class="child-element"></div> </vue-scroll>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        ops: {
          vuescroll: {},
          scrollPanel: {},
          rail: {}
          bar: {}
        }
      }
    }
  }
</script>
```

::: tip
If you have an emergency, you can call the `refresh` function.
:::
