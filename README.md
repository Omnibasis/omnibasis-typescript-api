# omnibasis-typescript-api
Access Omnibasis API from javascript or typescript application like Angular.

You can view all [Omnibasis API](https://api.omnibasis.com) here.

You can generate library with all AJAX requests to call server API. It's automatically
generated by [nswag](https://github.com/NSwag/NSwag) tool using
[swagger](http://swagger.io/). 


* Download  nswag directory intor your project
* Add nswag librariry to your node-modules list as described in  [nswag](https://github.com/NSwag/NSwag)
* Run **nswag/refreshall.bat** file  to create all proxies
* Run **nswag/refresh.bat <name-of-interface>** file  to create proxie for that interface, for example 'refresh contentShared' will created proxy for Content Shared interface.

Generated code is located in shared/service-proxies/<name-of-interface>/**service-proxies**.ts file. You should not make manual change in this file since it will be overwritten on the next code
generation. You can change where nswag puts a generated code by updating service.config.nswag

**Refreshing Service Proxies**

While Nswag automatically generate proxy files, it does not refresh
**service-proxies.module**.ts. If you want to use new APIs which has been added since you generated the files, you should run **nswag/refreshall.bat** to update service proxies.
