### 重启脚本 (**os\.restart**)


#### 声明
```lua
os.restart([ 脚本文件路径 ])
```


#### 参数及返回值
> - 脚本文件路径 **\*1\.1\.2\-2 新增**
>   - 文本型，可选参数，当这里传入一个有效的脚本文件路径将会重启到目标脚本文件，默认为 `""`


#### 说明
> 在没有 **脚本文件路径** 参数的情况下这个函数调用会直接重启 **当前脚本** 进程，当前脚本会立即结束  
> 传入了有效的 **脚本文件路径** 参数的时脚本会结束并重新启动到 **目标脚本文件**  
> 操作失败的情况下，该函数会返回 false 并附带错误信息，操作失败通常是传入了非法参数  


#### 需要注意  
> **当前脚本** 的定义是启动的那份脚本，脚本文件被更改后使用 os\.restart\(\) **不会** 启动更改之后的脚本文件  
> 如果可能，请 **不要** 在多线程环境使用该函数  
> 无延迟重启会导致的其它逻辑问题也需要作者规避  
> 当前函数暂 **不支持** 重启、启动 xpp **脚本包** 脚本  


#### 示例 1  
```lua
os.restart() -- 重启到 “当前脚本” (不是 “当前脚本文件”) 
```


#### 示例 2  
```lua
os.restart(utils.launch_args().path) -- 重启到 “当前脚本文件”
```
**注**：上述代码中使用了非本章函数 [`utils.launch_args`](/Handbook/utils/utils.launch_args.md)
