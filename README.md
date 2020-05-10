# TPYBoardDevelopment
使用TPYBoard V202进行Micro Python开发，板载ESP-12F

尽管板载ESP，但是在REPL中使用`Ctrl+B`查看固件，提示

```
MicroPython v1.8.7-7-gb5a1a20a3 on 2017-01-09; ESP module with ESP8266
```

似乎出场的时候搭载的固件不太对，但是还能正常使用。官方的文档请参考：http://docs.tpyboard.com/zh/latest/ 。尽管网络上能够找到各种软广，但是感觉实际的使用还是相当小众。

不清楚是因为自己买到了仿制的伪劣板子所以刷到了错误的固件，还是因为官方的文档没有更新，在使用的过程中会出现比较麻烦的问题。

如在使用过程中我遇到了无法进行`import pyb`的问题，查询之后找到了这样一个Issue：https://github.com/micropython/micropython/issues/2085 。在这里，有人回答ESP8266不包含pyb，应使用`macine`进行替代。

目前的计划是开发一个能够记录光强、温湿度并能定时将数据上传到腾讯云COS的工具。
