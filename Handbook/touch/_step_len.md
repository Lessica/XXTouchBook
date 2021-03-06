### 设置触摸事件对象移动步长 \(**:step\_len**\)


#### 声明
```lua
触摸事件 = 触摸事件:step_len(步长)
```


#### 参数及返回值
- 步长
    - 整数型，可选参数，默认为 2
- 触摸事件
    - 触摸事件对象，通过调用 [touch.on](/Handbook/touch/touch.on.md) 函数可以获得一个用于操控当前触摸的事件对象


#### 说明
> 设置当前触摸事件对象使用 move 方法滑动的步长  


#### 示例  
```lua
-- 模拟一个手指于点 100, 100 的位置接触屏幕，以步长为 3 、每步延迟为 0.2 毫秒的速度滑动到点 200, 200 的位置离开屏幕
touch.on(100, 100):step_len(3):step_delay(0.2):move(200, 200):off()
```

