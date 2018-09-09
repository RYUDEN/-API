
##使用vue-jsonp插件解决跨域问题
npm install vue-jsonp --save  

```javascript
import Vue from 'vue'
import VueJsonp from 'vue-jsonp'
Vue.use(VueJsonp)
 
// If you want to setup the global timeout, just:
Vue.use(VueJsonp, 5000)
// Now all requests will be expired after 5000ms.
 
// Use it in Vue Component.
const SomeComponent = Vue.extend({
  methods: {
    getData () {
      this.$jsonp('http://m.maoyan.com/ajax/movieOnInfoList', { token: ''}).then(json => {
        // Success.
      }).catch(err => {
        // Failed.
      })
    }
  }
})
 
```
##使用jQury的jsonp请求

```javascript
 $.ajax({
     url: 'http://localhost:9090/student',
     type: 'GET',
     success: function (data) {
         $(text).val(data);
     }
 });
```  
