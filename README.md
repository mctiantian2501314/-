

# 遇到阅读云
![Screenshot_2024-12-13-01-53-36-69_df198e732186825c8df26e3c5a10d7cd.jpg](http://img.wuaze.com/2024/12/13/675b24e82d244.jpg)
方法一
搜索js
```js
@js:
let url = 'https://www.sososhu.com/?site=m54kanshu&q={{java.encodeURI(key)}}' 
let ck = cookie.getCookie(url);
let head = JSON.stringify({
  headers: { 'Cookie': ck }
})
url + "," + head
```
列表规则js
```js
<js>
if (result.match(/阅读云/)) {
   u = baseUrl.split(',')[0]
   cookie.removeCookie(u)
   java.startBrowserAwait(u, "验证")
   ck = cookie.getCookie(u)
   head = JSON.stringify({ headers: { 'Cookie': ck } })
   url = u + "," + head
   result = java.ajax(url)
}
result
</js>
.block > div > div:nth-child(n+1)
```

方法二

登录认证js
```js
var src = result.body();
if(key && /ge_ua/.test(src)){
	url = java.ruleUrl;
	result = java.startBrowserAwait(url, "验证");
	}
result
```

请求头js
```js
@js:  
JSON.stringify({"Referer": baseUrl,  
"X-Requested-With": "mark.via",  
"Accept-Language": "zh-CN,zh;q=0.9,en-US;q=0.8,en;q=0.7",  
"User-Agent": "Mozilla/5.0 (Linux; Android 10; PACM00 Build/QP1A.190711.020) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/108.0.5359.79 Mobile Safari/537.36"})

```# -
