ToSDR-bookmarklet
=================

Bookmarklet that shows you ToSDR's rating for a given site's Terms of Service.

##  Usage

Save the following code as a bookmark, then click the bookmark on any site!

``` javascript
javascript:(function(){var c=function(d,e,f){var f=f||{};var i=f.obj||window;var h=f.path||((i==window)?"window":"");var g=Object.keys(i);g.forEach(function(j){if((b[d]||d)(e,i,j)){console.log([h,".",j].join(""),"->",["(",typeof i[j],")"].join(""),i[j])}if(Object.prototype.toString.call(i[j])=="[object Object]"&&(i[j]!=i)&&h.split(".").indexOf(j)==-1){c(d,e,{obj:i[j],path:[h,j].join(".")})}})};var a=function(d,g,e,f){(!g||typeof e==g)?c(d,e,f):console.error([e,"must be",g].join(" "))};var b={name:function(d,e,f){return d==f},nameContains:function(d,e,f){return f.indexOf(d)>-1},type:function(d,e,f){return e[f] instanceof d},value:function(d,e,f){return e[f]===d},valueCoerced:function(d,e,f){return e[f]==d}};window.find={byName:function(d,e){a("name","string",d,e)},byNameContains:function(d,e){a("nameContains","string",d,e)},byType:function(d,e){a("type","function",d,e)},byValue:function(d,e){a("value",null,d,e)},byValueCoerced:function(d,e){a("valueCoerced",null,d,e)},custom:function(e,d){c(e,null,d)}}})();
```
