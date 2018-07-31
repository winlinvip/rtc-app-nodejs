# rtc-app-nodejs

Nodejs AppServer for RTC.

AppServer writen by other languages:

* Python: https://github.com/winlinvip/rtc-app-python
* Java: https://github.com/winlinvip/rtc-app-java
* Golang: https://github.com/winlinvip/rtc-app-golang
* PHP: https://github.com/winlinvip/rtc-app-php
* C#: https://github.com/winlinvip/rtc-app-csharp
* Nodejs: https://github.com/winlinvip/rtc-app-nodejs

For RTC deverloper:

* RTC [workflow](https://help.aliyun.com/document_detail/74889.html).
* RTC [token generation](https://help.aliyun.com/document_detail/74890.html).

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
echo "  endpoint: 'https://rtc.aliyuncs.com'," >> config.js &&
echo "  gslb: 'https://rgslb.rtc.aliyuncs.com'" >> config.js &&
echo "};" >> config.js &&
node index.js
```

4. Verify AppServer by [here](http://localhost:8080/app/v1/login?room=5678&user=nvivy&passwd=12345678).

> Remark: You can setup client native SDK by `http://30.2.228.19:8080/app/v1`.

> Remark: Please use your AppServer IP instead by `ifconfig eth0`.

