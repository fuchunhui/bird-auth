# bird-auth

baidu `passport` or `uuap` auth

## Original

解决 [birdv1](https://github.com/weger/bird) 版本手动取cookie问题

## Examples

```new birdAuth.uuap(options[, callback(cookie)])```

```new birdAuth.passport(options[, callback(cookie)])```

## Demo

### Uuap auth

``` js
var birdAuth = require('bird-auth')
var uuap = new birdAuth.uuap({
    username: 'xxx',
    password: 'xxx',
    uuapServer: 'http://xxx.baidu.com/login', // CAS auth 
    service: 'http://xxx.baidu.com/' // service address, if you don't know this url, you can logout you system, and get `service` parameters
}, function(cookie) {
    console.log(cookie)
});
```

### Passport auth

``` js
var birdAuth = require('bird-auth')
var passport = new birdAuth.passport({
    username: 'xxx',
    password: 'xxx'
}, function(cookie) {
    console.log(cookie)
});
```

## Future

- 账户热切换
- <s>Support Https</s>
- <s>Support online Passport auth</s>
- <s>Set rejectUnauthorized false and fix uuap auth bug.</s> [detail](http://stackoverflow.com/questions/20082893/unable-to-verify-leaf-signature)
- <s>Add bprouting support</s>
- <s>statusCode === 302 judgment</s>

## More

- [] getCookie()

## History

- [1.0.0] Project init