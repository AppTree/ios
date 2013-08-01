#Lua 

### lua/C交互

> “ lua通过一个运行时栈来维护参数传递及返 回，使用lua_to*等函数获取lua传递到C函数的参数，使用lua_push*从C函数返回值到lua脚本。此外也可以使用 lua_getglobal从C函数获取lua脚本定义的全局变量。具体参看例子” 之前看的一篇，讲怎么编lua/C交互的

[http://blog.csdn.net/hanhuili/article/details/8496167]()

还有篇是关于C自定义函数嵌入lua运行的

[http://blog.csdn.net/zhangyafengcpp/article/details/6848205]()

### lua/Objective-C交互

本质上和C是相同的，只不过把函数头的风格换成了Objective-C

    - (int) runLuaScript:(NSString *)filename {
    	lua_State *lua = luaL_newstate();
    	assert(lua);
    	luaL_openlibs(lua);
    
    	const int status = luaL_dofile(lua, [filename cStringUsingEncoding:NSUTF8StringEncoding]);
    	if(status)
    		printf("Couldn't execute LUA code: %s\n", lua_tostring(lua, -1));
    		lua_close(lua);
    	return 0;
    } 

### luaJIT


* 一个第三方实现的Just-In-Time解释器，[luaJIT](http://luajit.org/)执行lua脚本在性能上优于lua自己的解释器。

* luaJIT 有对应的iOS framework [LuaJIT-iOS-Framework](https://github.com/DylanSale/LuaJIT-iOS-Framework) , 你可以从这个项目中获取编译好的库文件以及一个可供参考的Demo. 

#### luaJIT ffi library

>The FFI library largely obviates the need to write tedious manual Lua/C bindings in C. No need to learn a separate binding language — it parses plain C declarations! These can be cut-n-pasted from C header files or reference manuals. It's up to the task of binding large libraries without the need for dealing with fragile binding generators. 

简单来说就是，可以让lua直接调用C函数，不用你自己处理函数的预载和参数的出栈入栈 lol  

### FAQ

//待添加 

### Others

![ppt](/imgs/ppt-1.jpg)

[走近Lua.ppt](/attachments/走近Lua.ppt)