# dytt-reptitle-v2

>dytt8.net reptile

[![npm](https://img.shields.io/badge/npm-v1.0.3-brightgreen.svg)](https://www.npmjs.com/package/dytt-reptitle-v2)

[![NPM](https://nodei.co/npm/dytt-reptitle-v2.png?downloads=true&stars=true)](https://nodei.co/npm/dytt-reptitle-v2)

## Tip 
[原作者项目地址](https://github.com/HuangXiZhou/dytt-reptitle)  

本版本是Fork原作者过来的,我发现这个版本有bug时,已经提交了PR给原作者,但原作者一直没有处理,可能是没有时间吧。所以我修复后更新了一个新的包。感谢原作者[HuangXiZhou](https://github.com/HuangXiZhou)的贡献。  
  
1.修复了设置page无效的bug  
2.修复了获取的链接不是真正的下载链接的bug  
3.增加了跳页(skip)扒取数据的功能  

## Demo
[Demo请勿商用](http://www.zi-yuan.club)

## Install

```bash
npm install dytt-reptitle-v2
```

## Usage

```js
const dyttReptitle = require('dytt-reptitle-v2');
dyttReptitle().then(res => {
  // do what you want...
});
```

## Configure

```js
// example
const config = {
  page: 1,
  skip: 0,
  include: [ 'title', 'imgUrl', 'desc', 'downloadLink', 'descPageLink' ]
};

dyttReptitle(config).then(res => {
  // do what you want...
});
```

### config

| param | Description | Type | Required
| --- | --- | --- | --- |
| page | crawl page number | Number | true |
| skip | skip page number | Number | false |
| include | needed data | Array | false |

### include

| param | Description | Type | Required
| --- | --- | --- | --- |
| title | movie title | String | false |
| imgUrl | movie poster | String | false |
| desc | movie description | String | false |
| downloadLink | movie download link | String | false |
| descPageLink | movie description page link | String | false |

### Response example

```js
[{ title: '2019年剧情战争《兰开斯特的天空》BD中英双字幕',
  imgUrl: 'https://extraimage.net/images/2019/05/25/aea98d0038576db1158830d3c82cc888.jpg',
  downloadLink: 'magnet:?xt=urn:btih:8dd1ccb0dedeaaacf78e4ae0d97bf88dfca8d060&dn=%e9%98%b3%e5%85%89%e7%94%b5%e5%bd%b1www.ygdy8.com.%e5%85%b0%e5%bc%80%e6%96%af%e7%89%b9%e7%9a%84%e5%a4%a9%e7%a9%ba.BD.720p.%e4%b8%ad%e8%8b%b1%e5%8f%8c%e5%ad%97%e5%b9%95.mkv&tr=udp%3a%2f%2ftracker.opentrackr.org%3a1337%2fannounce&tr=udp%3a%2f%2fthetracker.org%3a80%2fannounce&tr=http%3a%2f%2fretracker.telecom.by%2fannounce',
  descPageLink: 'https://www.dytt8.net/html/gndy/dyzz/20190525/58637.html'
}]
```

## Uninstall

```bash
npm uninstall dytt-reptitle-v2
```

## License

MIT
