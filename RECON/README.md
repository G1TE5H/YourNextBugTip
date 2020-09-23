*[Tweet](https://twitter.com/krizzsk/status/1287405881441755139) By [Joel Verghese](https://twitter.com/krizzsk)*  
```
Big companies often use their own CDN network and some of them are used to serve internal static files
such as JavaScript. You can use the below-mentioned steps to get some internal subdomains or juicy

JavaScript files to increase your attack surface.
1. Do a passive or active enumeration of the CDN domain (in this case the domain is bigcompanycdn.com).
2. For whatever subdomain found search that on shodan using the "http.html" filter.
3. Example: You found dev-int.bigcompanycdn.com, Shodan query will be like this
http.html: "dev-int.bigcomanycdn.com" or http.html: "https://dev-int.bigcompanycdn.com" etc.
```
