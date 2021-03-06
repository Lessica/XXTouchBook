### 输入文字 \(**sys\.input\_text**\)


#### 声明
```lua
sys.input_text(文字内容 [, 输入完成按回车 ])
```


#### 参数及返回值
- 文字内容
    - 文本型，需要输入的文字，**不支持** `"\b"` (退格键) 
- 输入完成按回车
    - 布尔型，是否在输入完毕后按下键盘上的回车键 (发送、搜索等) ，默认 false


#### 说明  
> 在前台程序的可以输入文本的地方输入文字  
> 该函数原理为先将文本写入剪贴板，然后调用粘贴快捷键 (**command \+ v**) 粘贴文本  
> **该函数的调用会影响公共剪贴板，请注意在调用之前备份好剪贴板中的重要数据**   
> **在系统公共剪贴板损坏的情况下，该函数的文字输入会失效。也就是不能复制粘贴文字，就不能用**    
> **与此函数已知的冲突插件：Background Manager**  
> 如果遇到无法作用的情况可以参考 [`app.input_text`](/Handbook/app/app.input_text.md) 或许能解决  


#### 示例  
```lua
sys.input_text("我爱你") -- 在当前光标所在文本框输入“我爱你”
--
sys.input_text("我爱你", true) -- 在QQ聊天界面输入“我爱你”然后按下回车发送出去
```

