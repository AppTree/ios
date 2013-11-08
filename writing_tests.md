#iOS 笔试题

##说明
根据C、Objc、iOS的基础知识出了30道选择题

##内容

__1-10 C语言 & 计算机基础__

1、请看下面一段代码

	static int a = 1;
	int main(){
    		int b = 2;
     		char *c = NULL; 
     		c = (char *)malloc(100 * sizeof(char));
		return 0;
	}	

请问访问a,b,c 3种类型变量的效率从高到低依次是  
A. cba  
B. abc  
C. acb  
D. bca  


（B）


2、下面四种内部排序算法中哪一种在最差情况下时间复杂度最高？  
A. 快速排序  
B. 冒泡排序  
C. 堆排序  
D. 归并排序  


（B）


3、Shell中，将command1的输出作为command2的输入应该使用的命令是  
A. command1 && command2  
B. command1 > command2  
C. command1 & command2  
D. command1 | command2  


（D）


4、下面的数据结构中不属于线性结构的是  
A. 栈  
B. 链表  
C. 二叉树  
D. 线性表  

（C）


5、在一个二叉树上，第5层最多可以有的节点数是
A. 2  
B. 8  
C. 16  
D. 32  


（C）


6、在长度为n的线性表上进行顺序查找，在最糟糕的情况下需要的比较次数是  
A. n  
B. 2n-1  
C. 2n  
D. n^2  


（A）


7、下面那项不是动态语言的特性  
A. 在运行时替换一个类  
B. 在运行时动态加载lib文件  
C. 在运行时修改对象中的方法  
D. 在运行时增加对象的方法  


（B）


8、已知二叉树后序遍历序列是dabec，中序遍历序列是debac，它的前序遍历序列是  
A. cedba   
B. acbed   
C. decab   
D. deabc  

（A）


9、以下多线程对int型变量x的操作，哪个不需要进行同步：   
A. x=y  
B. x++  
C. ++x  
D. x=1  


（D）


10、多线程中栈与堆是公有的还是私有的  
A. 栈公有, 堆私有  
B. 栈公有，堆公有  
C. 栈私有, 堆公有  
D. 栈私有，堆私有  
（C）


__11-20 Objective-C & Xcode__


11、在Xcode中，需要编译混合Objective-C和C++的源码文件，需要将文件格式的后缀改为  
A. .c  
B. .cpp  
C. .mm  
D. .m  


（C）


12、Objective-C声明一个类所要用到的编译指令是  
A. @interface SomeClass  
B. @protocol SomeClass  
C. @implementation SomeClass  
D. @autorelease SomeClass  


（A）


13、使用Xcode创建工程时，支持同时创建的版本管理库是  
A. Subversion  
B. Mercurial  
C. Git  
D. Concurrent Versions System  


（C）


14、下面那个方法不属于NSObject的内省（Introspection）方法  
A. init  
B. isKindOfClass  
C. responseToSelector  
D. isMemberOfClass  


（A）


15、使用protocol时，声明一组可选择实现与否的函数，需要在声明的前一行加上：  
A. @required  
B. @optional  
C. @interface  
D. @protocol  


（B）


16、需要在手动管理内存分配和释放的Xcode项目中引入和编译用ARC风格编写的文件，需要在文件的Compiler Flags上添加参数：  
A. -shared  
B. -fno-objc-arc  
C. -fobjc-arc  
D. -dynamic  


（C）


17、下面关于Objective-C内存管理的描述错误的是  
A. 当使用ARC来管理内存时，代码中不可以出现autorelease  
B. autoreleasepool 在 drain 的时候会释放在其中分配的对象  
C. 当使用ARC来管理内存时，在线程中大量分配对象而不用autoreleasepool则可能会造成内存泄露  
D. 在使用ARC的项目中不能使用NSZone  


（A）


18、下面关于#import和#include的描述正确的是
A. #import 是 #include 的替代指令，防止重复引用  
B. #import 和 #include 不可以混合使用  
C. #import 只用于引用 Objective-C的文件， #include 只用于引用C和C++的文件  
D. #import 和 #include 的使用效果完全相同  


（A）


19、下面的代码问题在哪？  

	@implementation xxx
	…
	…
	- (void) setVar:(int)i {
	     self.var = i;
	}


A. 应该将var synthesize  
B. 调用会出现死循环  
C. 正常  
D. 返回值错误  


（B）


20、下面那个方法可以比较两个NSString *str1, *str2 的异同  
A. if(str1 = str2) xxx ;  
B. if([str1 isEqualToString:str2]) xxx ;  
C. if(str1 && str2) xxx ;  
D. if([str1 length] == [str2 length]) xxx;  


（B）

__21-30 iOS__ 


21、下面哪个不属于对象数据序列化方法
A. JSON  
B. Property List  
C. XML  
D. HTTP  


（D）


22、在UIKit中，frame与bounds的区别是  
A. frame 是 bounds 的别名  
B. frame 是 bounds 的继承类  
C. frame 的参考系是父视图坐标，bounds 的参考系是自身的坐标  
D. frame 的参考系是自身坐标，bounds 的参考系是父视图的坐标  


（C）


23、Objective-C有私有方法吗？有私有变量吗？  
A. 有私有方法和私有变量  
B. 没有私有方法也没有私有变量  
C. 没有私有方法，有私有变量  
D. 有私有方法，没有私有变量  


（C）


24、下面关于线程管理错误的是  
A. GCD所用的开销要比NSThread大    
B. 可以在子线程中修改UI元素  
C. NSOperationQueue是比NSthread更高层的封装  
D. GCD可以根据不同优先级分配线程  


（B）


25、下面代码的作用是让doSomeThing函数每隔1秒被调用1次。请问哪里有问题

	NSTimer *myTimer = [NSTimer timerWithTimeInterval:1.0 target:self selector:@selector(doSomeThing:) 	userInfo:nil repeats:YES]; 

	[myTimer fire]
  

A. 没有将timer加入runloop  
B. doSomeThing缺少参数  
C. 忘记传递数据给userInfo  
D. myTimer对象未通过[[myTimer alloc] init]方法初始化  


（A）


26、UIViewController在显示过程中，各个方法的调用顺序是  
A. init -> viewDidLoad -> viewDidAppear -> viewDidUnload  
B. init -> viewDidAppear -> viewDidLoad -> viewDidUnload  
C. init -> viewDidLoad -> viewDidUnload -> viewDidAppear  
D. init -> viewDidAppear -> viewDidUnload -> viewDidLoad  

（A）


27、使用imageNamed方法创建UIImage对象时，与普通的init方法有什么区别？  
A. 没有区别，只是为了方便  
B. imageNamed方法只是创建了一个指针，没有分配其他内存  
C. imageNamed方法将图片加载到内存中后不再释放  
D. imageNamed方法将使用完图片后立即释放  

（C）


28、一个类的delegate（代理）的作用不正确的是  
A. delegate中的函数在其他类中实现  
B. 主要用于不同类型的对象之间一对一传递消息  
C. 没有指派则不会触发  
D. 可以一个对象的delegate指派给多个其他类型的对象  

（D）


29、在没有navigationController的情况下，要从一个ViewController切换到另一个ViewController应该  
A. [self.navigationController pushViewController:nextViewController animated:YES];  
B. [self.view addSubview:nextViewController.view];  
C. [self pushViewController:nextViewController animated:YES];  
D. [self presentModalViewController:nextViewController animated:YES];  

（D）


30、什么是key window？  
A. App中唯一的那个UIWindow对象  
B. 可以指定一个key的UIWindow  
C. 可接收到键盘输入等事件的UIWindow  
D. 不可以隐藏的那个UIWindow对象  

（C）
