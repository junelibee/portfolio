<!DOCTYPE HTML>
<html lang="en-US">
<head>
  <meta charset="UTF-8" /><script type="text/javascript">(window.NREUM||(NREUM={})).loader_config={xpid:"VgUFVldbGwEJUlJXBAQDUw==",licenseKey:"e7fb1b89a0",applicationID:"296353545"};window.NREUM||(NREUM={}),__nr_require=function(t,n,e){function r(e){if(!n[e]){var o=n[e]={exports:{}};t[e][0].call(o.exports,function(n){var o=t[e][1][n];return r(o||n)},o,o.exports)}return n[e].exports}if("function"==typeof __nr_require)return __nr_require;for(var o=0;o<e.length;o++)r(e[o]);return r}({1:[function(t,n,e){function r(t){try{s.console&&console.log(t)}catch(n){}}var o,i=t("ee"),a=t(20),s={};try{o=localStorage.getItem("__nr_flags").split(","),console&&"function"==typeof console.log&&(s.console=!0,o.indexOf("dev")!==-1&&(s.dev=!0),o.indexOf("nr_dev")!==-1&&(s.nrDev=!0))}catch(c){}s.nrDev&&i.on("internal-error",function(t){r(t.stack)}),s.dev&&i.on("fn-err",function(t,n,e){r(e.stack)}),s.dev&&(r("NR AGENT IN DEVELOPMENT MODE"),r("flags: "+a(s,function(t,n){return t}).join(", ")))},{}],2:[function(t,n,e){function r(t,n,e,r,s){try{p?p-=1:o(s||new UncaughtException(t,n,e),!0)}catch(f){try{i("ierr",[f,c.now(),!0])}catch(d){}}return"function"==typeof u&&u.apply(this,a(arguments))}function UncaughtException(t,n,e){this.message=t||"Uncaught error with no additional information",this.sourceURL=n,this.line=e}function o(t,n){var e=n?null:c.now();i("err",[t,e])}var i=t("handle"),a=t(21),s=t("ee"),c=t("loader"),f=t("gos"),u=window.onerror,d=!1,l="nr@seenError",p=0;c.features.err=!0,t(1),window.onerror=r;try{throw new Error}catch(h){"stack"in h&&(t(9),t(8),"addEventListener"in window&&t(5),c.xhrWrappable&&t(10),d=!0)}s.on("fn-start",function(t,n,e){d&&(p+=1)}),s.on("fn-err",function(t,n,e){d&&!e[l]&&(f(e,l,function(){return!0}),this.thrown=!0,o(e))}),s.on("fn-end",function(){d&&!this.thrown&&p>0&&(p-=1)}),s.on("internal-error",function(t){i("ierr",[t,c.now(),!0])})},{}],3:[function(t,n,e){t("loader").features.ins=!0},{}],4:[function(t,n,e){function r(t){}if(window.performance&&window.performance.timing&&window.performance.getEntriesByType){var o=t("ee"),i=t("handle"),a=t(9),s=t(8),c="learResourceTimings",f="addEventListener",u="resourcetimingbufferfull",d="bstResource",l="resource",p="-start",h="-end",m="fn"+p,w="fn"+h,v="bstTimer",g="pushState",y=t("loader");y.features.stn=!0,t(7),"addEventListener"in window&&t(5);var x=NREUM.o.EV;o.on(m,function(t,n){var e=t[0];e instanceof x&&(this.bstStart=y.now())}),o.on(w,function(t,n){var e=t[0];e instanceof x&&i("bst",[e,n,this.bstStart,y.now()])}),a.on(m,function(t,n,e){this.bstStart=y.now(),this.bstType=e}),a.on(w,function(t,n){i(v,[n,this.bstStart,y.now(),this.bstType])}),s.on(m,function(){this.bstStart=y.now()}),s.on(w,function(t,n){i(v,[n,this.bstStart,y.now(),"requestAnimationFrame"])}),o.on(g+p,function(t){this.time=y.now(),this.startPath=location.pathname+location.hash}),o.on(g+h,function(t){i("bstHist",[location.pathname+location.hash,this.startPath,this.time])}),f in window.performance&&(window.performance["c"+c]?window.performance[f](u,function(t){i(d,[window.performance.getEntriesByType(l)]),window.performance["c"+c]()},!1):window.performance[f]("webkit"+u,function(t){i(d,[window.performance.getEntriesByType(l)]),window.performance["webkitC"+c]()},!1)),document[f]("scroll",r,{passive:!0}),document[f]("keypress",r,!1),document[f]("click",r,!1)}},{}],5:[function(t,n,e){function r(t){for(var n=t;n&&!n.hasOwnProperty(u);)n=Object.getPrototypeOf(n);n&&o(n)}function o(t){s.inPlace(t,[u,d],"-",i)}function i(t,n){return t[1]}var a=t("ee").get("events"),s=t("wrap-function")(a,!0),c=t("gos"),f=XMLHttpRequest,u="addEventListener",d="removeEventListener";n.exports=a,"getPrototypeOf"in Object?(r(document),r(window),r(f.prototype)):f.prototype.hasOwnProperty(u)&&(o(window),o(f.prototype)),a.on(u+"-start",function(t,n){var e=t[1],r=c(e,"nr@wrapped",function(){function t(){if("function"==typeof e.handleEvent)return e.handleEvent.apply(e,arguments)}var n={object:t,"function":e}[typeof e];return n?s(n,"fn-",null,n.name||"anonymous"):e});this.wrapped=t[1]=r}),a.on(d+"-start",function(t){t[1]=this.wrapped||t[1]})},{}],6:[function(t,n,e){function r(t,n,e){var r=t[n];"function"==typeof r&&(t[n]=function(){var t=i(arguments),n={};o.emit(e+"before-start",[t],n);var a;n[m]&&n[m].dt&&(a=n[m].dt);var s=r.apply(this,t);return o.emit(e+"start",[t,a],s),s.then(function(t){return o.emit(e+"end",[null,t],s),t},function(t){throw o.emit(e+"end",[t],s),t})})}var o=t("ee").get("fetch"),i=t(21),a=t(20);n.exports=o;var s=window,c="fetch-",f=c+"body-",u=["arrayBuffer","blob","json","text","formData"],d=s.Request,l=s.Response,p=s.fetch,h="prototype",m="nr@context";d&&l&&p&&(a(u,function(t,n){r(d[h],n,f),r(l[h],n,f)}),r(s,"fetch",c),o.on(c+"end",function(t,n){var e=this;if(n){var r=n.headers.get("content-length");null!==r&&(e.rxSize=r),o.emit(c+"done",[null,n],e)}else o.emit(c+"done",[t],e)}))},{}],7:[function(t,n,e){var r=t("ee").get("history"),o=t("wrap-function")(r);n.exports=r;var i=window.history&&window.history.constructor&&window.history.constructor.prototype,a=window.history;i&&i.pushState&&i.replaceState&&(a=i),o.inPlace(a,["pushState","replaceState"],"-")},{}],8:[function(t,n,e){var r=t("ee").get("raf"),o=t("wrap-function")(r),i="equestAnimationFrame";n.exports=r,o.inPlace(window,["r"+i,"mozR"+i,"webkitR"+i,"msR"+i],"raf-"),r.on("raf-start",function(t){t[0]=o(t[0],"fn-")})},{}],9:[function(t,n,e){function r(t,n,e){t[0]=a(t[0],"fn-",null,e)}function o(t,n,e){this.method=e,this.timerDuration=isNaN(t[1])?0:+t[1],t[0]=a(t[0],"fn-",this,e)}var i=t("ee").get("timer"),a=t("wrap-function")(i),s="setTimeout",c="setInterval",f="clearTimeout",u="-start",d="-";n.exports=i,a.inPlace(window,[s,"setImmediate"],s+d),a.inPlace(window,[c],c+d),a.inPlace(window,[f,"clearImmediate"],f+d),i.on(c+u,r),i.on(s+u,o)},{}],10:[function(t,n,e){function r(t,n){d.inPlace(n,["onreadystatechange"],"fn-",s)}function o(){var t=this,n=u.context(t);t.readyState>3&&!n.resolved&&(n.resolved=!0,u.emit("xhr-resolved",[],t)),d.inPlace(t,g,"fn-",s)}function i(t){y.push(t),h&&(b?b.then(a):w?w(a):(E=-E,R.data=E))}function a(){for(var t=0;t<y.length;t++)r([],y[t]);y.length&&(y=[])}function s(t,n){return n}function c(t,n){for(var e in t)n[e]=t[e];return n}t(5);var f=t("ee"),u=f.get("xhr"),d=t("wrap-function")(u),l=NREUM.o,p=l.XHR,h=l.MO,m=l.PR,w=l.SI,v="readystatechange",g=["onload","onerror","onabort","onloadstart","onloadend","onprogress","ontimeout"],y=[];n.exports=u;var x=window.XMLHttpRequest=function(t){var n=new p(t);try{u.emit("new-xhr",[n],n),n.addEventListener(v,o,!1)}catch(e){try{u.emit("internal-error",[e])}catch(r){}}return n};if(c(p,x),x.prototype=p.prototype,d.inPlace(x.prototype,["open","send"],"-xhr-",s),u.on("send-xhr-start",function(t,n){r(t,n),i(n)}),u.on("open-xhr-start",r),h){var b=m&&m.resolve();if(!w&&!m){var E=1,R=document.createTextNode(E);new h(a).observe(R,{characterData:!0})}}else f.on("fn-end",function(t){t[0]&&t[0].type===v||a()})},{}],11:[function(t,n,e){function r(){var t=window.NREUM;if(!t.loader_config)return null;var n=(t.loader_config.accountID||"").toString()||null,e=(t.loader_config.agentID||"").toString()||null,r=(t.loader_config.trustKey||"").toString()||null;if(!n||!e)return null;var a=i.generateCatId(),s=i.generateCatId(),c=Date.now(),f=o(a,s,c,n,e,r);return{header:f,guid:a,traceId:s,timestamp:c}}function o(t,n,e,r,o,i){var a="btoa"in window&&"function"==typeof window.btoa;if(!a)return null;var s={v:[0,1],d:{ty:"Browser",ac:r,ap:o,id:t,tr:n,ti:e}};return i&&r!==i&&(s.d.tk=i),btoa(JSON.stringify(s))}var i=t(18);n.exports={generateTracePayload:r,generateTraceHeader:o}},{}],12:[function(t,n,e){function r(t){var n=this.params,e=this.metrics;if(!this.ended){this.ended=!0;for(var r=0;r<p;r++)t.removeEventListener(l[r],this.listener,!1);n.aborted||(e.duration=s.now()-this.startTime,this.loadCaptureCalled||4!==t.readyState?null==n.status&&(n.status=0):a(this,t),e.cbTime=this.cbTime,d.emit("xhr-done",[t],t),c("xhr",[n,e,this.startTime]))}}function o(t,n){var e=t.responseType;if("json"===e&&null!==n)return n;var r="arraybuffer"===e||"blob"===e||"json"===e?t.response:t.responseText;return w(r)}function i(t,n){var e=f(n),r=t.params;r.host=e.hostname+":"+e.port,r.pathname=e.pathname,t.sameOrigin=e.sameOrigin}function a(t,n){t.params.status=n.status;var e=o(n,t.lastSize);if(e&&(t.metrics.rxSize=e),t.sameOrigin){var r=n.getResponseHeader("X-NewRelic-App-Data");r&&(t.params.cat=r.split(", ").pop())}t.loadCaptureCalled=!0}var s=t("loader");if(s.xhrWrappable){var c=t("handle"),f=t(13),u=t(11).generateTracePayload,d=t("ee"),l=["load","error","abort","timeout"],p=l.length,h=t("id"),m=t(16),w=t(15),v=window.XMLHttpRequest;s.features.xhr=!0,t(10),t(6),d.on("new-xhr",function(t){var n=this;n.totalCbs=0,n.called=0,n.cbTime=0,n.end=r,n.ended=!1,n.xhrGuids={},n.lastSize=null,n.loadCaptureCalled=!1,t.addEventListener("load",function(e){a(n,t)},!1),m&&(m>34||m<10)||window.opera||t.addEventListener("progress",function(t){n.lastSize=t.loaded},!1)}),d.on("open-xhr-start",function(t){this.params={method:t[0]},i(this,t[1]),this.metrics={}}),d.on("open-xhr-end",function(t,n){"loader_config"in NREUM&&"xpid"in NREUM.loader_config&&this.sameOrigin&&n.setRequestHeader("X-NewRelic-ID",NREUM.loader_config.xpid);var e=!1;if("init"in NREUM&&"distributed_tracing"in NREUM.init&&(e=!!NREUM.init.distributed_tracing.enabled),e&&this.sameOrigin){var r=u();r&&r.header&&(n.setRequestHeader("newrelic",r.header),this.dt=r)}}),d.on("send-xhr-start",function(t,n){var e=this.metrics,r=t[0],o=this;if(e&&r){var i=w(r);i&&(e.txSize=i)}this.startTime=s.now(),this.listener=function(t){try{"abort"!==t.type||o.loadCaptureCalled||(o.params.aborted=!0),("load"!==t.type||o.called===o.totalCbs&&(o.onloadCalled||"function"!=typeof n.onload))&&o.end(n)}catch(e){try{d.emit("internal-error",[e])}catch(r){}}};for(var a=0;a<p;a++)n.addEventListener(l[a],this.listener,!1)}),d.on("xhr-cb-time",function(t,n,e){this.cbTime+=t,n?this.onloadCalled=!0:this.called+=1,this.called!==this.totalCbs||!this.onloadCalled&&"function"==typeof e.onload||this.end(e)}),d.on("xhr-load-added",function(t,n){var e=""+h(t)+!!n;this.xhrGuids&&!this.xhrGuids[e]&&(this.xhrGuids[e]=!0,this.totalCbs+=1)}),d.on("xhr-load-removed",function(t,n){var e=""+h(t)+!!n;this.xhrGuids&&this.xhrGuids[e]&&(delete this.xhrGuids[e],this.totalCbs-=1)}),d.on("addEventListener-end",function(t,n){n instanceof v&&"load"===t[0]&&d.emit("xhr-load-added",[t[1],t[2]],n)}),d.on("removeEventListener-end",function(t,n){n instanceof v&&"load"===t[0]&&d.emit("xhr-load-removed",[t[1],t[2]],n)}),d.on("fn-start",function(t,n,e){n instanceof v&&("onload"===e&&(this.onload=!0),("load"===(t[0]&&t[0].type)||this.onload)&&(this.xhrCbStart=s.now()))}),d.on("fn-end",function(t,n){this.xhrCbStart&&d.emit("xhr-cb-time",[s.now()-this.xhrCbStart,this.onload,n],n)}),d.on("fetch-before-start",function(t){var n,e=t[1]||{};"string"==typeof t[0]?n=t[0]:t[0]&&t[0].url&&(n=t[0].url),n&&(this.sameOrigin=f(n).sameOrigin);var r=!1;if("init"in NREUM&&"distributed_tracing"in NREUM.init&&(r=!!NREUM.init.distributed_tracing.enabled),r&&this.sameOrigin){var o=u();if(!o||!o.header)return;var i=o.header;if("string"==typeof t[0]){var a={};for(var s in e)a[s]=e[s];a.headers=new Headers(e.headers||{}),a.headers.set("newrelic",i),this.dt=o,t.length>1?t[1]=a:t.push(a)}else t[0]&&t[0].headers&&(t[0].headers.append("newrelic",i),this.dt=o)}})}},{}],13:[function(t,n,e){n.exports=function(t){var n=document.createElement("a"),e=window.location,r={};n.href=t,r.port=n.port;var o=n.href.split("://");!r.port&&o[1]&&(r.port=o[1].split("/")[0].split("@").pop().split(":")[1]),r.port&&"0"!==r.port||(r.port="https"===o[0]?"443":"80"),r.hostname=n.hostname||e.hostname,r.pathname=n.pathname,r.protocol=o[0],"/"!==r.pathname.charAt(0)&&(r.pathname="/"+r.pathname);var i=!n.protocol||":"===n.protocol||n.protocol===e.protocol,a=n.hostname===document.domain&&n.port===e.port;return r.sameOrigin=i&&(!n.hostname||a),r}},{}],14:[function(t,n,e){function r(){}function o(t,n,e){return function(){return i(t,[f.now()].concat(s(arguments)),n?null:this,e),n?void 0:this}}var i=t("handle"),a=t(20),s=t(21),c=t("ee").get("tracer"),f=t("loader"),u=NREUM;"undefined"==typeof window.newrelic&&(newrelic=u);var d=["setPageViewName","setCustomAttribute","setErrorHandler","finished","addToTrace","inlineHit","addRelease"],l="api-",p=l+"ixn-";a(d,function(t,n){u[n]=o(l+n,!0,"api")}),u.addPageAction=o(l+"addPageAction",!0),u.setCurrentRouteName=o(l+"routeName",!0),n.exports=newrelic,u.interaction=function(){return(new r).get()};var h=r.prototype={createTracer:function(t,n){var e={},r=this,o="function"==typeof n;return i(p+"tracer",[f.now(),t,e],r),function(){if(c.emit((o?"":"no-")+"fn-start",[f.now(),r,o],e),o)try{return n.apply(this,arguments)}catch(t){throw c.emit("fn-err",[arguments,this,t],e),t}finally{c.emit("fn-end",[f.now()],e)}}}};a("actionText,setName,setAttribute,save,ignore,onEnd,getContext,end,get".split(","),function(t,n){h[n]=o(p+n)}),newrelic.noticeError=function(t,n){"string"==typeof t&&(t=new Error(t)),i("err",[t,f.now(),!1,n])}},{}],15:[function(t,n,e){n.exports=function(t){if("string"==typeof t&&t.length)return t.length;if("object"==typeof t){if("undefined"!=typeof ArrayBuffer&&t instanceof ArrayBuffer&&t.byteLength)return t.byteLength;if("undefined"!=typeof Blob&&t instanceof Blob&&t.size)return t.size;if(!("undefined"!=typeof FormData&&t instanceof FormData))try{return JSON.stringify(t).length}catch(n){return}}}},{}],16:[function(t,n,e){var r=0,o=navigator.userAgent.match(/Firefox[\/\s](\d+\.\d+)/);o&&(r=+o[1]),n.exports=r},{}],17:[function(t,n,e){function r(t,n){var e=t.getEntries();e.forEach(function(t){"first-paint"===t.name?a("timing",["fp",Math.floor(t.startTime)]):"first-contentful-paint"===t.name&&a("timing",["fcp",Math.floor(t.startTime)])})}function o(t){if(t instanceof c&&!u){var n,e=Math.round(t.timeStamp);n=e>1e12?Date.now()-e:s.now()-e,u=!0,a("timing",["fi",e,{type:t.type,fid:n}])}}if(!("init"in NREUM&&"page_view_timing"in NREUM.init&&"enabled"in NREUM.init.page_view_timing&&NREUM.init.page_view_timing.enabled===!1)){var i,a=t("handle"),s=t("loader"),c=NREUM.o.EV;if("PerformanceObserver"in window&&"function"==typeof window.PerformanceObserver){i=new PerformanceObserver(r);try{i.observe({entryTypes:["paint"]})}catch(f){}}if("addEventListener"in document){var u=!1,d=["click","keydown","mousedown","pointerdown","touchstart"];d.forEach(function(t){document.addEventListener(t,o,!1)})}}},{}],18:[function(t,n,e){function r(){function t(){return n?15&n[e++]:16*Math.random()|0}var n=null,e=0,r=window.crypto||window.msCrypto;r&&r.getRandomValues&&(n=r.getRandomValues(new Uint8Array(31)));for(var o,i="xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx",a="",s=0;s<i.length;s++)o=i[s],"x"===o?a+=t().toString(16):"y"===o?(o=3&t()|8,a+=o.toString(16)):a+=o;return a}function o(){function t(){return n?15&n[e++]:16*Math.random()|0}var n=null,e=0,r=window.crypto||window.msCrypto;r&&r.getRandomValues&&Uint8Array&&(n=r.getRandomValues(new Uint8Array(31)));for(var o=[],i=0;i<16;i++)o.push(t().toString(16));return o.join("")}n.exports={generateUuid:r,generateCatId:o}},{}],19:[function(t,n,e){function r(t,n){if(!o)return!1;if(t!==o)return!1;if(!n)return!0;if(!i)return!1;for(var e=i.split("."),r=n.split("."),a=0;a<r.length;a++)if(r[a]!==e[a])return!1;return!0}var o=null,i=null,a=/Version\/(\S+)\s+Safari/;if(navigator.userAgent){var s=navigator.userAgent,c=s.match(a);c&&s.indexOf("Chrome")===-1&&s.indexOf("Chromium")===-1&&(o="Safari",i=c[1])}n.exports={agent:o,version:i,match:r}},{}],20:[function(t,n,e){function r(t,n){var e=[],r="",i=0;for(r in t)o.call(t,r)&&(e[i]=n(r,t[r]),i+=1);return e}var o=Object.prototype.hasOwnProperty;n.exports=r},{}],21:[function(t,n,e){function r(t,n,e){n||(n=0),"undefined"==typeof e&&(e=t?t.length:0);for(var r=-1,o=e-n||0,i=Array(o<0?0:o);++r<o;)i[r]=t[n+r];return i}n.exports=r},{}],22:[function(t,n,e){n.exports={exists:"undefined"!=typeof window.performance&&window.performance.timing&&"undefined"!=typeof window.performance.timing.navigationStart}},{}],ee:[function(t,n,e){function r(){}function o(t){function n(t){return t&&t instanceof r?t:t?c(t,s,i):i()}function e(e,r,o,i){if(!l.aborted||i){t&&t(e,r,o);for(var a=n(o),s=m(e),c=s.length,f=0;f<c;f++)s[f].apply(a,r);var d=u[y[e]];return d&&d.push([x,e,r,a]),a}}function p(t,n){g[t]=m(t).concat(n)}function h(t,n){var e=g[t];if(e)for(var r=0;r<e.length;r++)e[r]===n&&e.splice(r,1)}function m(t){return g[t]||[]}function w(t){return d[t]=d[t]||o(e)}function v(t,n){f(t,function(t,e){n=n||"feature",y[e]=n,n in u||(u[n]=[])})}var g={},y={},x={on:p,addEventListener:p,removeEventListener:h,emit:e,get:w,listeners:m,context:n,buffer:v,abort:a,aborted:!1};return x}function i(){return new r}function a(){(u.api||u.feature)&&(l.aborted=!0,u=l.backlog={})}var s="nr@context",c=t("gos"),f=t(20),u={},d={},l=n.exports=o();l.backlog=u},{}],gos:[function(t,n,e){function r(t,n,e){if(o.call(t,n))return t[n];var r=e();if(Object.defineProperty&&Object.keys)try{return Object.defineProperty(t,n,{value:r,writable:!0,enumerable:!1}),r}catch(i){}return t[n]=r,r}var o=Object.prototype.hasOwnProperty;n.exports=r},{}],handle:[function(t,n,e){function r(t,n,e,r){o.buffer([t],r),o.emit(t,n,e)}var o=t("ee").get("handle");n.exports=r,r.ee=o},{}],id:[function(t,n,e){function r(t){var n=typeof t;return!t||"object"!==n&&"function"!==n?-1:t===window?0:a(t,i,function(){return o++})}var o=1,i="nr@id",a=t("gos");n.exports=r},{}],loader:[function(t,n,e){function r(){if(!E++){var t=b.info=NREUM.info,n=p.getElementsByTagName("script")[0];if(setTimeout(u.abort,3e4),!(t&&t.licenseKey&&t.applicationID&&n))return u.abort();f(y,function(n,e){t[n]||(t[n]=e)}),c("mark",["onload",a()+b.offset],null,"api");var e=p.createElement("script");e.src="https://"+t.agent,n.parentNode.insertBefore(e,n)}}function o(){"complete"===p.readyState&&i()}function i(){c("mark",["domContent",a()+b.offset],null,"api")}function a(){return R.exists&&performance.now?Math.round(performance.now()):(s=Math.max((new Date).getTime(),s))-b.offset}var s=(new Date).getTime(),c=t("handle"),f=t(20),u=t("ee"),d=t(19),l=window,p=l.document,h="addEventListener",m="attachEvent",w=l.XMLHttpRequest,v=w&&w.prototype;NREUM.o={ST:setTimeout,SI:l.setImmediate,CT:clearTimeout,XHR:w,REQ:l.Request,EV:l.Event,PR:l.Promise,MO:l.MutationObserver};var g=""+location,y={beacon:"bam.nr-data.net",errorBeacon:"bam.nr-data.net",agent:"js-agent.newrelic.com/nr-1153.min.js"},x=w&&v&&v[h]&&!/CriOS/.test(navigator.userAgent),b=n.exports={offset:s,now:a,origin:g,features:{},xhrWrappable:x,userAgent:d};t(14),t(17),p[h]?(p[h]("DOMContentLoaded",i,!1),l[h]("load",r,!1)):(p[m]("onreadystatechange",o),l[m]("onload",r)),c("mark",["firstbyte",s],null,"api");var E=0,R=t(22)},{}],"wrap-function":[function(t,n,e){function r(t){return!(t&&t instanceof Function&&t.apply&&!t[a])}var o=t("ee"),i=t(21),a="nr@original",s=Object.prototype.hasOwnProperty,c=!1;n.exports=function(t,n){function e(t,n,e,o){function nrWrapper(){var r,a,s,c;try{a=this,r=i(arguments),s="function"==typeof e?e(r,a):e||{}}catch(f){l([f,"",[r,a,o],s])}u(n+"start",[r,a,o],s);try{return c=t.apply(a,r)}catch(d){throw u(n+"err",[r,a,d],s),d}finally{u(n+"end",[r,a,c],s)}}return r(t)?t:(n||(n=""),nrWrapper[a]=t,d(t,nrWrapper),nrWrapper)}function f(t,n,o,i){o||(o="");var a,s,c,f="-"===o.charAt(0);for(c=0;c<n.length;c++)s=n[c],a=t[s],r(a)||(t[s]=e(a,f?s+o:o,i,s))}function u(e,r,o){if(!c||n){var i=c;c=!0;try{t.emit(e,r,o,n)}catch(a){l([a,e,r,o])}c=i}}function d(t,n){if(Object.defineProperty&&Object.keys)try{var e=Object.keys(t);return e.forEach(function(e){Object.defineProperty(n,e,{get:function(){return t[e]},set:function(n){return t[e]=n,n}})}),n}catch(r){l([r])}for(var o in t)s.call(t,o)&&(n[o]=t[o]);return n}function l(n){try{t.emit("internal-error",n)}catch(e){}}return t||(t=o),e.inPlace=f,e.flag=a,e}},{}]},{},["loader",2,12,4,3]);</script>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
      <meta name=twitter:card  content="summary_large_image" />
      <meta name=twitter:site  content="@AdobePortfolio" />
      <meta  property=og:title content="June Borgese" />
      <meta  property=og:image content="https://pro2-bar-s3-cdn-cf3.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/eb70dd60-2a31-4a5c-a597-d8b53be79c4a_rw_600.JPG?h=3436a55304a9b0cfaa87f96dac4ab02e" />
      <link rel="icon" href="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQAQMAAAAlPW0iAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAADUExURUxpcU3H2DoAAAABdFJOUwBA5thmAAAADElEQVQI12NgIA0AAAAwAAHHqoWOAAAAAElFTkSuQmCC"  />
      <link rel="stylesheet" href="/dist/css/main.css" type="text/css" />
      <link rel="stylesheet" href="https://pro2-bar-s3-cdn-cf1.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/ce229bef652df00ce8540968c2724d6c1575440011.css?h=0878213c7efc87f1291ee6f5cb6719c7" type="text/css" />
    <link rel="canonical" href="https://juneliborgese32d3.myportfolio.com/artist-bio" />
      <title>June Borgese</title>
    <script type="text/javascript" src="//use.typekit.net/ik/bKFO2hKLeyMffY8aUopcL0cKWju65yRUcU63OdfE3VJfenvgfHYEBsJzwD9oFDIDWhsRjRJD5ejt5QMawA9kZcIkZ2wUwhZqZAjojQSkwDIu52bhwh9Xweb-mkG0dW83da4XZcNC-Av0jhNlOfG0SY4zwKuh-AmaOcuoSeNkieZzde8zOcFzdPUlpWgzS1scdhUTdkoRdhXCSY4zwKuh-AmaOcuoSeNkieZzde8zOcFzdPJIjcT3ZkGHfOYJMsMMeMw6MKGHfH_JMsMMeMb6MKGHfHDJMsMMeMS6MTMgkpP8t69.js?cb=00b201453aebe7bec4659c241122b4ac54bff69e" async onload="
    try {
      window.Typekit.load();
    } catch (e) {
      console.warn('Typekit not loaded.');
    }
    "></script>
</head>
        <body class="transition-enabled">  <div class='page-background-video page-background-video-with-panel'>
  </div>
  <div class="js-responsive-nav">
    <div class="responsive-nav has-social">
      <div class="close-responsive-click-area js-close-responsive-nav">
        <div class="close-responsive-button"></div>
      </div>
          <nav class="nav-container js-editable-target editable">
      <div class="page-title">
        <a href="/artist-bio-1" >Artist Bio</a>
      </div>
      <div class="page-title">
        <a href="/projects" >Projects</a>
      </div>
          </nav>
        <div class="social pf-nav-social js-editable-target editable" data-context="theme.nav">
          <ul>
          </ul>
        </div>
    </div>
  </div>
    <header class="site-header js-site-header js-editable-target editable  js-fixed-nav js-editable-target editable" data-context="theme.nav">
        <nav class="nav-container js-editable-target editable">
      <div class="page-title">
        <a href="/artist-bio-1" >Artist Bio</a>
      </div>
      <div class="page-title">
        <a href="/projects" >Projects</a>
      </div>
        </nav>
        <div class="logo-wrap js-editable-target editable" data-context="theme.nav">
          <div class="logo logo-text  ">
              <a href="" class="preserve-whitespace">June Borgese</a>

          </div>
        </div>
        <div class="social pf-nav-social js-editable-target editable" data-context="theme.nav">
          <ul>
          </ul>
        </div>
        <div class="hamburger-click-area js-hamburger">
          <div class="hamburger">
            <i></i>
            <i></i>
            <i></i>
          </div>
        </div>
    </header>
    <div class="header-placeholder"></div>
  <div class="site-wrap cfix js-site-wrap">
    <div class="site-container">
      <div class="site-content">
        <main>
  <div class="page-container js-editable-target editable" data-context="page.page.container">
    <section class="page standard-modules">
        <header class="page-header content js-editable-target editable" data-context="pages" data-identity="id:p5de7478a3227d330c16e442b633c49f9067ce84f770e9b174a235" data-menu="Page Header">
            <h1 class="title preserve-whitespace">Portfolio</h1>
            <p class="description"></p>
        </header>
      <div class="page-content js-page-content js-editable-target editable" data-context="pages" data-identity="id:p5de7478a3227d330c16e442b633c49f9067ce84f770e9b174a235" data-menu="Page Content">
        <div id="project-canvas" class="js-project-modules modules content">
          <div id="project-modules">
              
              
              
              
              
              
              
              
              <div class="js-project-module project-module module social_icons project-module-social_icons align- editable js-editable" data-id="m5de749d36bc7643b8c151b059a58164e4b98a3f1cf4932aa1d54a">
  <div class="module-content module-content-social_icons js-module-content">
      <div class="social">
        <ul>
              <li>
                <a href="http://www.linkedin.com/in/june-li-borgese-3a7548177" target="_blank">
                  <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 30 24" style="enable-background:new 0 0 30 24;" xml:space="preserve" class="icon">
                  <path id="path-1_24_" d="M19.6,19v-5.8c0-1.4-0.5-2.4-1.7-2.4c-1,0-1.5,0.7-1.8,1.3C16,12.3,16,12.6,16,13v6h-3.4
                    c0,0,0.1-9.8,0-10.8H16v1.5c0,0,0,0,0,0h0v0C16.4,9,17.2,7.9,19,7.9c2.3,0,4,1.5,4,4.9V19H19.6z M8.9,6.7L8.9,6.7
                    C7.7,6.7,7,5.9,7,4.9C7,3.8,7.8,3,8.9,3s1.9,0.8,1.9,1.9C10.9,5.9,10.1,6.7,8.9,6.7z M10.6,19H7.2V8.2h3.4V19z"/>
                  </svg>
                </a>
              </li>
              <li>
                <a href="http://www.instagram.com/junelibee/?hl=en" target="_blank">
                  <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 30 24" style="enable-background:new 0 0 30 24;" xml:space="preserve" class="icon">
                  <g>
                    <path d="M15,5.4c2.1,0,2.4,0,3.2,0c0.8,0,1.2,0.2,1.5,0.3c0.4,0.1,0.6,0.3,0.9,0.6c0.3,0.3,0.5,0.5,0.6,0.9
                      c0.1,0.3,0.2,0.7,0.3,1.5c0,0.8,0,1.1,0,3.2s0,2.4,0,3.2c0,0.8-0.2,1.2-0.3,1.5c-0.1,0.4-0.3,0.6-0.6,0.9c-0.3,0.3-0.5,0.5-0.9,0.6
                      c-0.3,0.1-0.7,0.2-1.5,0.3c-0.8,0-1.1,0-3.2,0s-2.4,0-3.2,0c-0.8,0-1.2-0.2-1.5-0.3c-0.4-0.1-0.6-0.3-0.9-0.6
                      c-0.3-0.3-0.5-0.5-0.6-0.9c-0.1-0.3-0.2-0.7-0.3-1.5c0-0.8,0-1.1,0-3.2s0-2.4,0-3.2c0-0.8,0.2-1.2,0.3-1.5c0.1-0.4,0.3-0.6,0.6-0.9
                      c0.3-0.3,0.5-0.5,0.9-0.6c0.3-0.1,0.7-0.2,1.5-0.3C12.6,5.4,12.9,5.4,15,5.4 M15,4c-2.2,0-2.4,0-3.3,0c-0.9,0-1.4,0.2-1.9,0.4
                      c-0.5,0.2-1,0.5-1.4,0.9C7.9,5.8,7.6,6.2,7.4,6.8C7.2,7.3,7.1,7.9,7,8.7C7,9.6,7,9.8,7,12s0,2.4,0,3.3c0,0.9,0.2,1.4,0.4,1.9
                      c0.2,0.5,0.5,1,0.9,1.4c0.4,0.4,0.9,0.7,1.4,0.9c0.5,0.2,1.1,0.3,1.9,0.4c0.9,0,1.1,0,3.3,0s2.4,0,3.3,0c0.9,0,1.4-0.2,1.9-0.4
                      c0.5-0.2,1-0.5,1.4-0.9c0.4-0.4,0.7-0.9,0.9-1.4c0.2-0.5,0.3-1.1,0.4-1.9c0-0.9,0-1.1,0-3.3s0-2.4,0-3.3c0-0.9-0.2-1.4-0.4-1.9
                      c-0.2-0.5-0.5-1-0.9-1.4c-0.4-0.4-0.9-0.7-1.4-0.9c-0.5-0.2-1.1-0.3-1.9-0.4C17.4,4,17.2,4,15,4L15,4L15,4z"/>
                    <path d="M15,7.9c-2.3,0-4.1,1.8-4.1,4.1s1.8,4.1,4.1,4.1s4.1-1.8,4.1-4.1S17.3,7.9,15,7.9L15,7.9z M15,14.7c-1.5,0-2.7-1.2-2.7-2.7
                      c0-1.5,1.2-2.7,2.7-2.7s2.7,1.2,2.7,2.7C17.7,13.5,16.5,14.7,15,14.7L15,14.7z"/>
                    <path d="M20.2,7.7c0,0.5-0.4,1-1,1s-1-0.4-1-1s0.4-1,1-1S20.2,7.2,20.2,7.7L20.2,7.7z"/>
                  </g>
                  </svg>
                </a>
              </li>
        </ul>
      </div>
  </div>
</div>

              
              
              
              
              
              
              
              
              <div class="project-module module media_collection project-module-media_collection" >
  <div class="grid--main js-grid-main">
    <div class="grid__item-container js-grid-item-container" data-flex-grow="346.66666666667" style="width:346.66666666667px; flex-grow:346.66666666667;" data-width="1920" data-height="1440">
      <script type="text/html" class="js-lightbox-slide-content">
        <div class="grid__image-wrapper">
          <img src="https://pro2-bar-s3-cdn-cf3.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/eb70dd60-2a31-4a5c-a597-d8b53be79c4a_rw_1920.JPG?h=12250f979651a4f811bc3442043aa4f9" srcset="https://pro2-bar-s3-cdn-cf3.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/eb70dd60-2a31-4a5c-a597-d8b53be79c4a_rw_600.JPG?h=3436a55304a9b0cfaa87f96dac4ab02e 600w,https://pro2-bar-s3-cdn-cf3.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/eb70dd60-2a31-4a5c-a597-d8b53be79c4a_rw_1200.JPG?h=4fdc0d6646bd9742397b82e01a1517a6 1200w,https://pro2-bar-s3-cdn-cf3.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/eb70dd60-2a31-4a5c-a597-d8b53be79c4a_rw_1920.JPG?h=12250f979651a4f811bc3442043aa4f9 1920w," sizes="(max-width: 1920px) 100vw, 1920px">
        <div>
      </script>
      <img
        class="grid__item-image js-grid__item-image grid__item-image-lazy js-lazy"
        src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7"
        data-src="https://pro2-bar-s3-cdn-cf3.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/eb70dd60-2a31-4a5c-a597-d8b53be79c4a_rw_1920.JPG?h=12250f979651a4f811bc3442043aa4f9"
        data-srcset="https://pro2-bar-s3-cdn-cf3.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/eb70dd60-2a31-4a5c-a597-d8b53be79c4a_rw_600.JPG?h=3436a55304a9b0cfaa87f96dac4ab02e 600w,https://pro2-bar-s3-cdn-cf3.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/eb70dd60-2a31-4a5c-a597-d8b53be79c4a_rw_1200.JPG?h=4fdc0d6646bd9742397b82e01a1517a6 1200w,https://pro2-bar-s3-cdn-cf3.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/eb70dd60-2a31-4a5c-a597-d8b53be79c4a_rw_1920.JPG?h=12250f979651a4f811bc3442043aa4f9 1920w,"
      >
      <span class="grid__item-filler" style="padding-bottom:75%;"></span>
    </div>
    <div class="grid__item-container js-grid-item-container" data-flex-grow="268.38709677419" style="width:268.38709677419px; flex-grow:268.38709677419;" data-width="640" data-height="620">
      <script type="text/html" class="js-lightbox-slide-content">
        <div class="grid__image-wrapper">
          <img src="https://pro2-bar-s3-cdn-cf1.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/925c6b7e-80a3-4d76-bbf6-244367275d4b_rw_1200.JPG?h=a5303a000a2d46a386400d9501f3c912" srcset="https://pro2-bar-s3-cdn-cf1.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/925c6b7e-80a3-4d76-bbf6-244367275d4b_rw_600.JPG?h=7894804fc7eb452d3441ac123563c067 600w,https://pro2-bar-s3-cdn-cf1.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/925c6b7e-80a3-4d76-bbf6-244367275d4b_rw_1200.JPG?h=a5303a000a2d46a386400d9501f3c912 640w," sizes="(max-width: 640px) 100vw, 640px">
        <div>
      </script>
      <img
        class="grid__item-image js-grid__item-image grid__item-image-lazy js-lazy"
        src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7"
        data-src="https://pro2-bar-s3-cdn-cf1.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/925c6b7e-80a3-4d76-bbf6-244367275d4b_rw_1200.JPG?h=a5303a000a2d46a386400d9501f3c912"
        data-srcset="https://pro2-bar-s3-cdn-cf1.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/925c6b7e-80a3-4d76-bbf6-244367275d4b_rw_600.JPG?h=7894804fc7eb452d3441ac123563c067 600w,https://pro2-bar-s3-cdn-cf1.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/925c6b7e-80a3-4d76-bbf6-244367275d4b_rw_1200.JPG?h=a5303a000a2d46a386400d9501f3c912 640w,"
      >
      <span class="grid__item-filler" style="padding-bottom:96.875%;"></span>
    </div>
    <div class="grid__item-container js-grid-item-container" data-flex-grow="177.89473684211" style="width:177.89473684211px; flex-grow:177.89473684211;" data-width="3840" data-height="5612">
      <script type="text/html" class="js-lightbox-slide-content">
        <div class="grid__image-wrapper">
          <img src="https://pro2-bar-s3-cdn-cf2.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/daae8e0f-a2e3-4d18-85dc-4c75019e05e9_rw_3840.JPG?h=6601348590cd2d9aeefc40d9f55679e4" srcset="https://pro2-bar-s3-cdn-cf2.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/daae8e0f-a2e3-4d18-85dc-4c75019e05e9_rw_600.JPG?h=eaf6cfb002c3ad93c05a1543cc9ede55 600w,https://pro2-bar-s3-cdn-cf2.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/daae8e0f-a2e3-4d18-85dc-4c75019e05e9_rw_1200.JPG?h=f0a2bd88496608f9cdd045a382e48b9f 1200w,https://pro2-bar-s3-cdn-cf2.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/daae8e0f-a2e3-4d18-85dc-4c75019e05e9_rw_1920.JPG?h=b9f6c9206be63e1eedc97439c430f03a 1920w,https://pro2-bar-s3-cdn-cf2.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/daae8e0f-a2e3-4d18-85dc-4c75019e05e9_rw_3840.JPG?h=6601348590cd2d9aeefc40d9f55679e4 3840w," sizes="(max-width: 3840px) 100vw, 3840px">
        <div>
      </script>
      <img
        class="grid__item-image js-grid__item-image grid__item-image-lazy js-lazy"
        src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7"
        data-src="https://pro2-bar-s3-cdn-cf2.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/daae8e0f-a2e3-4d18-85dc-4c75019e05e9_rw_3840.JPG?h=6601348590cd2d9aeefc40d9f55679e4"
        data-srcset="https://pro2-bar-s3-cdn-cf2.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/daae8e0f-a2e3-4d18-85dc-4c75019e05e9_rw_600.JPG?h=eaf6cfb002c3ad93c05a1543cc9ede55 600w,https://pro2-bar-s3-cdn-cf2.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/daae8e0f-a2e3-4d18-85dc-4c75019e05e9_rw_1200.JPG?h=f0a2bd88496608f9cdd045a382e48b9f 1200w,https://pro2-bar-s3-cdn-cf2.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/daae8e0f-a2e3-4d18-85dc-4c75019e05e9_rw_1920.JPG?h=b9f6c9206be63e1eedc97439c430f03a 1920w,https://pro2-bar-s3-cdn-cf2.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/daae8e0f-a2e3-4d18-85dc-4c75019e05e9_rw_3840.JPG?h=6601348590cd2d9aeefc40d9f55679e4 3840w,"
      >
      <span class="grid__item-filler" style="padding-bottom:146.15384615385%;"></span>
    </div>
    <div class="grid__item-container js-grid-item-container" data-flex-grow="195.12195121951" style="width:195.12195121951px; flex-grow:195.12195121951;" data-width="400" data-height="533">
      <script type="text/html" class="js-lightbox-slide-content">
        <div class="grid__image-wrapper">
          <img src="https://pro2-bar-s3-cdn-cf6.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/a77462a1-399f-4601-82b8-eca53324b0c4_rw_600.JPG?h=455875de0346c0b3680e3c3067e67bdf" srcset="https://pro2-bar-s3-cdn-cf6.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/a77462a1-399f-4601-82b8-eca53324b0c4_rw_600.JPG?h=455875de0346c0b3680e3c3067e67bdf 400w," sizes="(max-width: 400px) 100vw, 400px">
        <div>
      </script>
      <img
        class="grid__item-image js-grid__item-image grid__item-image-lazy js-lazy"
        src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7"
        data-src="https://pro2-bar-s3-cdn-cf6.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/a77462a1-399f-4601-82b8-eca53324b0c4_rw_600.JPG?h=455875de0346c0b3680e3c3067e67bdf"
        data-srcset="https://pro2-bar-s3-cdn-cf6.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/a77462a1-399f-4601-82b8-eca53324b0c4_rw_600.JPG?h=455875de0346c0b3680e3c3067e67bdf 400w,"
      >
      <span class="grid__item-filler" style="padding-bottom:133.25%;"></span>
    </div>
    <div class="grid__item-container js-grid-item-container" data-flex-grow="260.61757719715" style="width:260.61757719715px; flex-grow:260.61757719715;" data-width="422" data-height="421">
      <script type="text/html" class="js-lightbox-slide-content">
        <div class="grid__image-wrapper">
          <img src="https://pro2-bar-s3-cdn-cf6.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/a5ab05d2-dfff-4e03-a616-1c9f125d3040_rw_600.png?h=5ecc594e569a50642ea7e108d0fc109d" srcset="https://pro2-bar-s3-cdn-cf6.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/a5ab05d2-dfff-4e03-a616-1c9f125d3040_rw_600.png?h=5ecc594e569a50642ea7e108d0fc109d 422w," sizes="(max-width: 422px) 100vw, 422px">
        <div>
      </script>
      <img
        class="grid__item-image js-grid__item-image grid__item-image-lazy js-lazy"
        src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7"
        data-src="https://pro2-bar-s3-cdn-cf6.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/a5ab05d2-dfff-4e03-a616-1c9f125d3040_rw_600.png?h=5ecc594e569a50642ea7e108d0fc109d"
        data-srcset="https://pro2-bar-s3-cdn-cf6.myportfolio.com/7627ee67-467e-497a-b6f9-2750956a5ef8/a5ab05d2-dfff-4e03-a616-1c9f125d3040_rw_600.png?h=5ecc594e569a50642ea7e108d0fc109d 422w,"
      >
      <span class="grid__item-filler" style="padding-bottom:99.763033175355%;"></span>
    </div>
    <div class="js-grid-spacer"></div>
  </div>
</div>

              
              
          </div>
        </div>
      </div>
    </section>
        <section class="back-to-top js-editable-target editable">
          <a href="#"><span class="arrow">&uarr;</span><span class="preserve-whitespace">Back to Top</span></a>
        </section>
        <a class="back-to-top-fixed js-editable-target editable js-back-to-top back-to-top-fixed-with-panel" href="#">
          <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
           viewBox="0 0 26 26" style="enable-background:new 0 0 26 26;" xml:space="preserve" class="icon icon-back-to-top">
          <g>
            <path d="M13.8,1.3L21.6,9c0.1,0.1,0.1,0.3,0.2,0.4c0.1,0.1,0.1,0.3,0.1,0.4s0,0.3-0.1,0.4c-0.1,0.1-0.1,0.3-0.3,0.4
              c-0.1,0.1-0.2,0.2-0.4,0.3c-0.2,0.1-0.3,0.1-0.4,0.1c-0.1,0-0.3,0-0.4-0.1c-0.2-0.1-0.3-0.2-0.4-0.3L14.2,5l0,19.1
              c0,0.2-0.1,0.3-0.1,0.5c0,0.1-0.1,0.3-0.3,0.4c-0.1,0.1-0.2,0.2-0.4,0.3c-0.1,0.1-0.3,0.1-0.5,0.1c-0.1,0-0.3,0-0.4-0.1
              c-0.1-0.1-0.3-0.1-0.4-0.3c-0.1-0.1-0.2-0.2-0.3-0.4c-0.1-0.1-0.1-0.3-0.1-0.5l0-19.1l-5.7,5.7C6,10.8,5.8,10.9,5.7,11
              c-0.1,0.1-0.3,0.1-0.4,0.1c-0.2,0-0.3,0-0.4-0.1c-0.1-0.1-0.3-0.2-0.4-0.3c-0.1-0.1-0.1-0.2-0.2-0.4C4.1,10.2,4,10.1,4.1,9.9
              c0-0.1,0-0.3,0.1-0.4c0-0.1,0.1-0.3,0.3-0.4l7.7-7.8c0.1,0,0.2-0.1,0.2-0.1c0,0,0.1-0.1,0.2-0.1c0.1,0,0.2,0,0.2-0.1
              c0.1,0,0.1,0,0.2,0c0,0,0.1,0,0.2,0c0.1,0,0.2,0,0.2,0.1c0.1,0,0.1,0.1,0.2,0.1C13.7,1.2,13.8,1.2,13.8,1.3z"/>
          </g>
          </svg>
        </a>
  </div>
              <footer class="site-footer js-editable-target editable">
                <div class="footer-text">
                  
                </div>
              </footer>
        </main>
      </div>
    </div>
  </div>
<div class="cookie-banner js-cookie-banner">
  <p>Insert copy here, which should vary depending on your region. <a class="consent-link" href="#">Accept</a></p>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="-6458 -2604 16 16" class='close-btn'>
    <g id="Group_1479" data-name="Group 1479" transform="translate(-8281.367 -3556.368)">
      <rect id="Rectangle_6401" data-name="Rectangle 6401" class="stroke" width="1.968" height="20.66" transform="translate(1823.367 953.759) rotate(-45)"/>
      <rect id="Rectangle_6402" data-name="Rectangle 6402" class="stroke" width="1.968" height="20.66" transform="translate(1824.758 968.368) rotate(-135)"/>
    </g>
  </svg>
</div>
<script type="text/javascript">window.NREUM||(NREUM={});NREUM.info={"beacon":"bam.nr-data.net","licenseKey":"e7fb1b89a0","applicationID":"296353545","transactionName":"ZwZaYkJVDERXUxULCV5Me0NDQA1aGWsmJzJtQ1JDXlEOXlRfEwUDQwYLBFQHTFpPQA4QElYMVF9fGgFYWw==","queueTime":0,"applicationTime":8,"atts":"S0FNFApPHxsUUUNYHU0e","errorBeacon":"bam.nr-data.net","agent":""}</script></body>
<script type="text/javascript">
  // fix for Safari's back/forward cache
  window.onpageshow = function(e) {
    if (e.persisted) { window.location.reload(); }
  };
</script>
  <script type="text/javascript">var __config__ = {"page_id":"p5de7478a3227d330c16e442b633c49f9067ce84f770e9b174a235","theme":{"name":"marta"},"pageTransition":true,"linkTransition":true,"disableDownload":false,"localizedValidationMessages":{"required":"This field is required","Email":"This field must be a valid email address"},"lightbox":{"enabled":true,"color":{"opacity":0.94,"hex":"#fff"}},"cookie_banner":{"enabled":false}};</script>
  <script type="text/javascript" src="/site/translations?cb=00b201453aebe7bec4659c241122b4ac54bff69e"></script>
  <script type="text/javascript" src="/dist/js/main.js?cb=00b201453aebe7bec4659c241122b4ac54bff69e"></script>
</html>
