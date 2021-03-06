> A tiny vueJS plugin to intercept every ajax request.

The component intercept every ajax requisition, it doesn't matter which component you use *[Axios, Vue-resourse, vanilla JS or any other]*.

With that you can implement any kind of control you need, validate users, [control progress](https://github.com/vanderleisilva/vue-auto-progress), or give an easy feedback for the users.

# Requirements

- [Vue.js](https://github.com/vuejs/vue) `^2.0.0`
- Module bundler: [webpack](https://github.com/webpack/webpack)

# Installation

``` bash
$ npm install vue-ajax-intercept --save
```

# Usage

```javascript
<script>
import ajaxIntercept from 'vue-ajax-intercept'

export default {
  name: 'app',
  methods: {
    start(status){
      console.log(status); //XMLHttpRequest object
    },
    finish(status){
      console.log(status); //XMLHttpRequest object
    }
  },
  components: { ajaxIntercept }
}

</script>
```

``` html
<template>
  <div>
    <ajax-intercept @start="start" @finish="finish" ></ajax-intercept>  
	<router-view></router-view>
  </div>
</template>
```

# License

[The MIT License](http://opensource.org/licenses/MIT)