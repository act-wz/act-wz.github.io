# ffmpeg

## 视频转码

```
ffmpeg -i input.mp4 output.avi
```

## 分辨率调整
```
ffmpeg -i input.mp4 -s 1280x720 -c:a copy output.mp4
```
上面的命令将设置所给定视频文件的分辨率到 1280×720


aspect 标志设置一个视频文件的屏幕高宽比，常用16:9、 4:3。
```
ffmpeg -i input.mp4 -aspect 16:9 output.mp4
```


## 视频转JPEG
```
ffmpeg -i input.mp4 -r 1 -f image2 image-%3d.jpeg
```


## 视频转gif
```
ffmpeg -i input.mp4 -ss 00:00:00 -t 10 out.gif
```


## 图片转视频
```
ffmpeg  -f image2 -i image-%3d.jpeg images.mp4
```


## 视频剪辑

使用开始和停止时间来剪辑视频 –s 表示开始时间 -t 表示总的持续时间
```
ffmpeg -i input.mp4 -ss 00:00:10 -codec copy -t 50 output.mp4
```

截取视频前 10 秒
```
ffmpeg -i input.mp4 -t 10 output.mp4
```
或 以 hh.mm.ss 格式
```
ffmpeg -i input.mp4 -t 00:00:10 output.mp4
```


## 音频处理

将转换 input.mp4 视频文件到 output.mp3 音频文件
```
ffmpeg -i input.mp4 -vn output.mp3
```


如果你不想要一个视频文件中的音频，使用 -an 标志
```
ffmpeg -i input.mp4 -an output.mp4
```


## 剪辑音频
```
ffmpeg -i input.mp3 -ss 00:01:54 -to 00:02:53 -c copy output.mp3
```

## 播放视频
```
ffplay video.mp4
```

## 播放音频
```
ffplay audio.mp3
```

## 直播相关

推流
```
ffmpeg -re -i input.mp4 -c copy -f flv rtmp://server/live/streamName

```

拉流
```
ffmpeg -i rtmp://server/live/streamName -c copy dump.mp4
```