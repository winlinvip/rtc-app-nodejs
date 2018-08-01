# rtc-app-nodejs

Nodejs AppServer for RTC.

You could also write AppServer by following languages:

* Golang: https://github.com/winlinvip/rtc-app-golang
* Java: https://github.com/winlinvip/rtc-app-java
* Python: https://github.com/winlinvip/rtc-app-python
* C#: https://github.com/winlinvip/rtc-app-csharp
* Nodejs: https://github.com/winlinvip/rtc-app-nodejs
* PHP: https://github.com/winlinvip/rtc-app-php

For RTC deverloper:

* RTC [workflow](https://help.aliyun.com/document_detail/74889.html).
* RTC [token generation](https://help.aliyun.com/document_detail/74890.html).

Use OpenAPI to create channel:

* Golang: https://help.aliyun.com/document_detail/74890.html#channel-golang
* Java: https://help.aliyun.com/document_detail/74890.html#channel-java
* Python: https://help.aliyun.com/document_detail/74890.html#channel-python
* C#: https://help.aliyun.com/document_detail/74890.html#channel-csharp
* Nodejs: https://help.aliyun.com/document_detail/74890.html#channel-nodejs
* PHP: https://help.aliyun.com/document_detail/74890.html#channel-php

Token generation algorithm:

* Golang: https://help.aliyun.com/document_detail/74890.html#token-golang
* Java: https://help.aliyun.com/document_detail/74890.html#token-java
* Python: https://help.aliyun.com/document_detail/74890.html#token-python
* C#: https://help.aliyun.com/document_detail/74890.html#token-csharp
* Nodejs: https://help.aliyun.com/document_detail/74890.html#token-nodejs
* PHP: https://help.aliyun.com/document_detail/74890.html#token-php

> We depends on [@alicloud/rtc-2018-01-11](https://github.com/aliyun/aliyun-openapi-nodejs-sdk),
you can also update to the latest version.

## Usage

1. Generate AK from [here](https://usercenter.console.aliyun.com/#/manage/ak):

```
AccessKeyID: OGAEkdiL62AkwSgs
AccessKeySecret: 4JaIs4SG4dLwPsQSwGAHzeOQKxO6iw
```

2. Create APP from [here](https://rtc.console.aliyun.com/#/manage):

```
AppID: iwo5l81k
```

3. Clone project and generate config:

```
git clone https://github.com/winlinvip/rtc-app-nodejs.git &&
cd rtc-app-nodejs && npm install &&
echo "module.exports = {" > config.js &&
echo "  listen: 8080," >> config.js &&
echo "  appId: 'iwo5l81k'," >> config.js &&
echo "  accessKeyId: 'OGAEkdiL62AkwSgs'," >> config.js &&
echo "  accessKeySecret: '4JaIs4SG4dLwPsQSwGAHzeOQKxO6iw'," >> config.js &&
echo "  endpoint: 'http://rtc.aliyuncs.com'," >> config.js &&
echo "  gslb: 'https://rgslb.rtc.aliyuncs.com'" >> config.js &&
echo "};" >> config.js &&
node index.js
```

4. Verify AppServer by [here](http://localhost:8080/app/v1/login?room=5678&user=nvivy&passwd=12345678).

> Remark: You can setup client native SDK by `http://30.2.228.19:8080/app/v1`.

> Remark: Please use your AppServer IP instead by `ifconfig eth0`.

## History

* [1a11844](https://github.com/winlinvip/rtc-app-nodejs/commit/1a11844b86c568c9bf63c5f7c0c96c873dbb7b2f), Log the request id and cost in ms.
* [a7f4db1](https://github.com/winlinvip/rtc-app-nodejs/commit/a7f4db1498bec34da9dd12daee096ceeeef6ed78), Support recover for some OpenAPI error.
* Support create channel and sign user token.

