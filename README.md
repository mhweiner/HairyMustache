# HM
HM is a JS view component and jQuery plugin for Mustache. Issues callbacks within new scope, so you can encapsulate your view logic, and have it run when it's ready. Each view/component can have its own API, so you can keep your components modular and completely isolated. At only 1.2kb gzipped, it's much more lightweight than any other component/templating library.

welcome.mustache
```HTML
<div data-tplid="{{tplid}}">
Hello, <span>{{noun}}</span>
<button>Refresh</button>
</div>
```
welcome.js
```JS
window.welcome = function($scope, data){

    /**
     * Randomly select a noun from data.nouns.
    */
    function refresh(){
       var noun = data.nouns[Math.rand()];
    }
    
    /* return api */
    return {
      refresh: refresh
    };
    
};
```


