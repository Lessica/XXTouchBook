### 获取图片对象的尺寸 \(**:size**\)


#### 声明
```lua
宽, 高 = 图像:size()
```


#### 参数及返回值
- 图像
    - 图片对象，当前操作的图片对象
- 宽, 高
    - 整数型，当前操作的图片对象的 宽、高


#### 说明
> 获取图片对象的尺寸，注意这里返回的 w 不一定比 h 短，旋转会发生改变  


#### 示例  
```lua
local img = image.load_file("/var/mobile/1.png")
local w, h = img:size()
sys.alert("图像的宽："..w.."\n图像的高："..h)
```

