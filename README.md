# janus-cas [![MIT](https://img.shields.io/github/license/xuyuanxiang/janus-server-sdk?style=plastic)](https://github.com/xuyuanxiang/janus-server-sdk/blob/master/LICENSE) 

[![spring-boot](https://img.shields.io/badge/Spring%20Boot-2.2.5.RELEASE-brightgreen.svg)](https://docs.spring.io/spring-boot/docs/2.2.5.RELEASE/reference/html/) 

## Janus

### janus-server-sdk

Maven依赖，聚合登录SDK。

### janus-cas

统一聚合登录服务（单点登录），依赖janus-server-sdk。

### janus-cas-client

统一登录服务客户端SDK，对接janus-cas。

### 关系

单服务部署集成janus-server-sdk即完成支付宝/微信用户授权登录的对接。

当存在多个微服务共用同一个支付宝应用/微信公众号ID的情况时，需要有唯一的中控服务：janus-cas来统一和支付宝与微信接口交互，维护和分发access_token、分享用户信息和会话等。

微服务集成janus-cas-client即完成与janus-cas的对接，实现同一个支付宝/微信用户在所有服务集群中统一登录，统一退出。
