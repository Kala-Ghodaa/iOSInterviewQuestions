# [《Hiring a Reliable iOS Developer》](http://blog.sunnyxx.com/2015/07/04/ios-interview/)—Reference Answers（Part 1）

<p align="center"><a href="https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88/%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88%EF%BC%88%E4%B8%8B%EF%BC%89.md"><img src="../banner.png"></a></p>


Description：Interview QuestionsSource是[Weibo@我就叫Sunny怎么了](http://weibo.com/u/1364395395)的this blog post：[《Hiring a Reliable iOS Developer》](http://blog.sunnyxx.com/2015/07/04/ios-interview/)，containing a total of55questions，except for the first question which is an error-correction question，the rest54道are all short-answer questions。


About the Question Author： 孙源（sunnyxx），currently works at百度，responsible for百度知道 iOS client development work，likes to dig deep into technology and summarize best practices，loves sharing and open source，maintains a forkingdog open source group called。

Answers compiled by[Weibo@iOS程序犭袁](http://weibo.com/luohanchenyilong/)compiled，not proofread by the question author，if there are any errors，please contact[Weibo@iOS程序犭袁](http://weibo.com/luohanchenyilong/)for corrections。

----------

# Table of Contents

 - [1. Style Correction Question](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#1-Style Correction Question) 

      1. [Optimization Part](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#Optimization Part) 
      2. [Critical Issues Part](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#Critical Issues Part) 
      
      ![https://github.com/ChenYilong](http://i.imgur.com/O7Zev94.png)

 - [2. When to use the weak keyword, and what is the difference compared to assign？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#2-什么情况使用-weak-关键字相比-assign-有什么不同) 
 - [3. How to use the copy keyword？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#3-怎么用-copy-关键字) 
 - [4. What problem will this syntax cause： @property (copy) NSMutableArray *array;](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#4-What problem will this syntax cause-property-copy-nsmutablearray-array) 
 - [5. How to make your class use the copy modifier？How to override a setter with the copy keyword？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#5-如何让自己的类用-copy-修饰符如何重写带-copy-关键字的-setter) 
 - [6. @property What is the essence of？ivar、getter、setter How are they generated and added to this class](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#6-property-What is the essence ofivargettersetter-How are they generated and added to this class) 
 - [7. @protocol and category How to use in @property](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#7-protocol-and-category-How to use in-property) 
 - [8. runtime How to implement weak 属性](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#8-runtime-How to implement-weak-属性) 
 - [9. @propertyWhat property keywords are available in？/ @property What modifiers can follow？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#9-propertyWhat property keywords are available in-property-What modifiers can follow) 
 - [10. weak属性需要在dealloc中置nil么？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#10-weak属性需要在dealloc中置nil么)
 - [11. @synthesizeand@dynamicWhat are their respective functions？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#11-synthesizeanddynamicWhat are their respective functions) 
 - [12. ARCUnder ARC, what are the default keywords when no property keywords are explicitly specified？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#12-arcPart 2不显式指定任何属性关键字时默认的关键字都有哪些) 
 - [13. 用@property声明的NSString（或NSArray，NSDictionary）经常使用copy关键字，为什么？如果改用strong关键字，可能造成什么问questions？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#13-用property声明的nsstring或nsarraynsdictionary经常使用copy关键字为什么如果改用strong关键字可能造成什么问questions) 
      1. [对非集合类对象的copy操作](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#1-对非集合类对象的copy操作) 
      2. [集合类对象的copy与mutableCopy](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#2集合类对象的copy与mutablecopy) 
 - [14. @synthesizeWhat are the rules for synthesizing instance variables？假如property名为foo，存在一个名为_foo的实例变量，那么还会自动合成新变量么？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#14-synthesizeWhat are the rules for synthesizing instance variables假如property名为foo存在一个名为_foo的实例变量那么还会自动合成新变量么) 
 - [15. After having automatic synthesized property instance variables，@synthesizeWhat other use cases are there？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#15-After having automatic synthesized property instance variablessynthesizeWhat other use cases are there) 
 - [16. objc中向一个nil对象发送消息将会发生什么？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#16-objc中向一个nil对象发送消息将会发生什么) 
 - [17. objcSending a message to an object in Objective-C[obj foo]andobjc_msgSend()What is the relationship between the function？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#17-objcSending a message to an object in Objective-Cobj-fooandobjc_msgsendWhat is the relationship between the function) 
 - [18. 什么时候会报unrecognized selector的异常？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#18-什么时候会报unrecognized-selector的异常) 
 - [19. 一个objc对象如何进行内存布局？（considering the case with a parent class）](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#19-一个objc对象如何进行内存布局considering the case with a parent class) 
 - [20. 一个objc对象的isa的指针指向什么？What is its purpose？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#20-一个objc对象的isa的指针指向什么What is its purpose)
 - [21. What does the following code output？](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01《招聘一个靠谱的iOS》Interview QuestionsReference Answers/《招聘一个靠谱的iOS》Interview QuestionsReference Answers（Part 1）.md#21-What does the following code output) 


 ```Objective-C
	@implementation Son : Father
	- (id)init
	{
	    self = [super init];
	    if (self) {
	        NSLog(@"%@", NSStringFromClass([self class]));
	        NSLog(@"%@", NSStringFromClass([super class]));
	    }
	    return self;
	}
	@end
 ```

 - [22. runtime如何通过selector找到对应的IMP地址？（分别考虑类方法and实例方法）]( https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88/%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88%EF%BC%88%E4%B8%8A%EF%BC%89.md#22-runtime%E5%A6%82%E4%BD%95%E9%80%9A%E8%BF%87selector%E6%89%BE%E5%88%B0%E5%AF%B9%E5%BA%94%E7%9A%84imp%E5%9C%B0%E5%9D%80%E5%88%86%E5%88%AB%E8%80%83%E8%99%91%E7%B1%BB%E6%96%B9%E6%B3%95%E5%92%8C%E5%AE%9E%E4%BE%8B%E6%96%B9%E6%B3%95 "") 
 - [23. 使用runtime Associate方法关联的对象，需要在主对象dealloc的时候释放么？]( https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88/%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88%EF%BC%88%E4%B8%8A%EF%BC%89.md#23-%E4%BD%BF%E7%94%A8runtime-associate%E6%96%B9%E6%B3%95%E5%85%B3%E8%81%94%E7%9A%84%E5%AF%B9%E8%B1%A1%E9%9C%80%E8%A6%81%E5%9C%A8%E4%B8%BB%E5%AF%B9%E8%B1%A1dealloc%E7%9A%84%E6%97%B6%E5%80%99%E9%87%8A%E6%94%BE%E4%B9%88 "") 
 - [24. objc中的类方法and实例方法有什么本质区别and联系？]( https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88/%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88%EF%BC%88%E4%B8%8A%EF%BC%89.md#24-objc%E4%B8%AD%E7%9A%84%E7%B1%BB%E6%96%B9%E6%B3%95%E5%92%8C%E5%AE%9E%E4%BE%8B%E6%96%B9%E6%B3%95%E6%9C%89%E4%BB%80%E4%B9%88%E6%9C%AC%E8%B4%A8%E5%8C%BA%E5%88%AB%E5%92%8C%E8%81%94%E7%B3%BB "")  
 - 25--55questions，请看[Part 2篇]( https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88/%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88%EF%BC%88%E4%B8%8B%EF%BC%89.md "") 。

-------

## 正文

### 1. Style Correction Question
![https://github.com/ChenYilong](http://i.imgur.com/O7Zev94.png)
修改完的代码：

修改方法有很多种，现给出一种做示例：


 ```Objective-C
// .h文件
// http://weibo.com/luohanchenyilong/
// https://github.com/ChenYilong
// 修改完的代码，这是第一种修改方法，后面会给出第二种修改方法

typedef NS_ENUM(NSInteger, CYLGender) {
    CYLGenderUndefined,
    CYLGenderMale,
    CYLGenderFemale
};

@interface CYLUser : NSObject<NSCopying>

@property (nonatomic, readonly, copy) NSString *name;
@property (nonatomic, readonly, assign) NSUInteger age;
@property (nonatomic, readonly, assign) CYLGender gender;

- (instancetype)initWithName:(NSString *)name age:(NSUInteger)age gender:(CYLGender)gender;
+ (instancetype)userWithName:(NSString *)name age:(NSUInteger)age gender:(CYLGender)gender;

@end
 ```




Part 2面对具体修改的地方，分两部分做Part 2介绍：**Critical Issues Part** and **Optimization Part**
。因为**Critical Issues Part**没什么技术含量，为了节省大家时间，放在后面讲，大神请直接看**Optimization Part**。


#### **Optimization Part**

 1. enum 建议使用 `NS_ENUM` and `NS_OPTIONS` 宏来定义枚举类型，参见官方的 [Adopting Modern Objective-C](https://developer.apple.com/library/ios/releasenotes/ObjectiveC/ModernizationObjC/AdoptingModernObjective-C/AdoptingModernObjective-C.html) 一文：


 ```objective-c
//定义一个枚举
	typedef NS_ENUM(NSInteger, CYLGender) {
	    CYLGenderUndefined,
	    CYLGenderMale,
	    CYLGenderFemale
	};
 ```
 （仅仅让性别包含男and女可能并不严谨，最严谨的做法可以参考 [这里](https://github.com/ChenYilong/iOSInterviewQuestions/issues/9) 。）
 
 2. age 属性的类型：应避免使用基本类型，建议使用 Foundation 数据类型，对应关系如Part 2：
 
 ```Objective-C
	int -> NSInteger
	unsigned -> NSUInteger
	float -> CGFloat
	动画时间 -> NSTimeInterval
```
同时考虑到 age 的特点，应使用 NSUInteger ，而非 int 。
这样做的是基于64-bit 适配考虑，详情可参考出questions者的博文[《64-bit Tips》](http://blog.sunnyxx.com/2014/12/20/64-bit-tips/)。


 3. 如果工程项目非常庞大，需要拆分成不同的模块，可以在类、typedef宏命名的时候使用前缀。
 4. doLogIn方法不应写在该类中： <p><del>虽然`LogIn`的命名不太清晰，但笔者猜测是login的意思， （勘误：Login是名词，LogIn 是动词，都表示登陆的意思。见： [ ***Log in vs. login*** ](http://grammarist.com/spelling/log-in-login/)）</del></p>登录操作属于业务逻辑，观察类名 UserModel ，以及属性的命名方式，该类应该是一个 Model 而不是一个“ MVVM 模式Part 2的 ViewModel ”：


 > 无论是 MVC 模式还是 MVVM 模式，业务逻辑都不应当写在 Model 里：MVC 应在 C，MVVM 应在 VM。


 （如果抛开命名规范，假设该类真的是 MVVM 模式里的 ViewModel ，那么 UserModel 这个类可能对应的是用户注册页面，如果有特殊的业务需求，比如： `-logIn` 对应的应当是注册并登录的一个 Button ，出现 `-logIn` 方法也可能是合理的。）

 5.  doLogIn 方法命名不规范：添加了多余的动词前缀。
请牢记：

  > 如果方法表示让对象执行一个动作，使用动词打头来命名，注意不要使用 `do`，`does` 这种多余的关键字，动词本身的暗示就足够了。

 应为 `-logIn` （注意： `Login` 是名词， `LogIn`  是动词，都表示登陆。  见[ ***Log in vs. login*** ](http://grammarist.com/spelling/log-in-login/)）

 6. `-(id)initUserModelWithUserName: (NSString*)name withAge:(int)age;`方法中不要用 `with` 来连接两个参数: `withAge:` 应当换为`age:`，`age:` 已经足以清晰Description参数的作用，也不建议用 `andAge:` ：通常情况Part 2，即使有类似 `withA:withB:` 的命名需求，也通常是使用`withA:andB:` 这种命名，用来表示方法执行了两个相对独立的操作（*从设计Part 1来说，这时候也可以拆分成两个独立的方法*），它不应该用作阐明有多个参数，比如Part 2面的：

  ```objective-c
//错误，不要使用"and"来连接参数
- (int)runModalForDirectory:(NSString *)path andFile:(NSString *)name andTypes:(NSArray *)fileTypes;
//错误，不要使用"and"来阐明有多个参数
- (instancetype)initWithName:(CGFloat)width andAge:(CGFloat)height;
//正确，使用"and"来表示两个相对独立的操作
- (BOOL)openFile:(NSString *)fullPath withApplication:(NSString *)appName andDeactivate:(BOOL)flag;
```

 7. 由于字符串值可能会改变，所以要把相关属性的“内存管理语义”声明为 copy 。(原因在Part 2文有详细论述：***用@property声明的NSString（或NSArray，NSDictionary）经常使用copy关键字，为什么？***)
 8. “性别”(gender）属性的：该类中只给出了一种“初始化方法” (initializer)用于设置“姓名”(Name)and“年龄”(Age)的初始值，那如何对“性别”(gender）初始化？

 Objective-C 有 designated and secondary 初始化方法的观念。 designated 初始化方法是提供所有的参数， 可以翻译为 "指定初始化方法" 或 "主要初始化方法"。secondary 初始化方法是一个或多个，并且提供一个或者更多的默认参数来调用 designated 初始化方法的初始化方法。举例Description：

 

 
 ```Objective-C

    // .m文件
    // http://weibo.com/luohanchenyilong/
    // https://github.com/ChenYilong
    //

    @implementation CYLUser

    - (instancetype)initWithName:(NSString *)name
                             age:(NSUInteger)age
                             gender:(CYLGender)gender {
        if (self = [super init]) {
            _name = [name copy];
            _age = age;
            _gender = gender;
        }
        return self;
    }

    - (instancetype)initWithName:(NSString *)name
                             age:(NSUInteger)age {
        return [self initWithName:name age:age gender:nil];
    }

    @end
```






 Part 1面的代码中 `initWithName:age:gender:` 就是 designated 初始化方法，另外的初始化方法, 在 Objective-C 中我们可以起一个名字叫二级初始化方法 (Secondary Initializer)。因为仅仅是调用类实现的 designated 初始化方法。
 
  而在 Swift 中， Apple 给二级初始化方法 (Secondary Initializer)  给出了官方的定义，叫做 Convenience Initializer, 也常常简写为 Convenience Init，详见 [《The Swift Programming Language - Designated Initializers and Convenience Initializers》](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/initialization/#Designated-Initializers-and-Convenience-Initializers) 

详见Part 2文, 本questions的 Swift 版本的代码。

  因为出questions者没有给出 `.m` 文件，所以有两种猜测：1：本来打算只设计一个 designated 初始化方法，但漏掉了“性别”(gender）属性。那么最终的修改代码就是Part 1文给出的第一种修改方法。2：不打算初始时初始化“性别”(gender）属性，打算后期再修改，如果是这种情况，那么应该把“性别”(gender）属性设为 readwrite 属性，最终给出的修改代码应该是：



 
 ```Objective-C


	// .h文件
	// http://weibo.com/luohanchenyilong/
	// https://github.com/ChenYilong
	// 第二种修改方法（基于第一种修改方法的基础Part 1）

	typedef NS_ENUM(NSInteger, CYLGender) {
	    CYLGenderUndefined,
	    CYLGenderMale,
	    CYLGenderFemale
	};

	@interface CYLUser : NSObject<NSCopying>

	@property (nonatomic, readonly, copy) NSString *name;
	@property (nonatomic, readonly, assign) NSUInteger age;
	@property (nonatomic, readwrite, assign) CYLGender gender;

	- (instancetype)initWithName:(NSString *)name age:(NSUInteger)age gender:(CYLGender)gender;
	- (instancetype)initWithName:(NSString *)name age:(NSUInteger)age;
	+ (instancetype)userWithName:(NSString *)name age:(NSUInteger)age gender:(CYLGender)gender;

	@end
```


  `.h` 中暴露 designated 初始化方法，是为了方便子类化 （想了解更多，请戳--》 [***《禅与 Objective-C 编程艺术 （Zen and the Art of the Objective-C Craftsmanship 中文翻译）》***](http://is.gd/OQ49zk)。）

对应的 Swift 版本如Part 2:


 ```Swift
import Foundation

enum CYLGender: Int {
    case undefined
    case male
    case female
}

class CYLUser: NSObject, NSCopying {

    let name: String
    let age: Int
    var gender: CYLGender

    init(name: String, age: Int, gender: CYLGender) {
        self.name = name
        self.age = age
        self.gender = gender
    }

    convenience init(name: String, age: Int) {
        self.init(name: name, age: age, gender: .undefined)
    }

    static func user(name: String, age: Int, gender: CYLGender) -> CYLUser {
        return CYLUser(name: name, age: age, gender: gender)
    }

    func copy(with zone: NSZone? = nil) -> Any {
        let copy = CYLUser(name: name, age: age, gender: gender)
        return copy
    }
}

 ```


   - 按照接口设计的惯例，如果设计了“初始化方法” (initializer)，也应当搭配一个快捷构造方法。而快捷构造方法的返回值，建议为 instancetype，为保持一致性，init 方法and快捷构造方法的返回类型最好都用 instancetype。
   - 如果基于第一种修改方法：既然该类中已经有一个“初始化方法” (initializer)，用于设置“姓名”(Name)、“年龄”(Age)and“性别”(Gender）的初始值:
那么在设计对应 `@property` 时就应该尽量使用不可变的对象：其三个属性都应该设为“只读”。用初始化方法设置好属性值之后，就不能再改变了。在本例中，仍需声明属性的“内存管理语义”。于是可以把属性的定义改成这样


 ```Objective-C
        @property (nonatomic, readonly, copy) NSString *name;
        @property (nonatomic, readonly, assign) NSUInteger age;
        @property (nonatomic, readonly, assign) CYLGender gender;
 ```

      由于是只读属性，所以编译器不会为其创建对应的“设置方法”，即便如此，我们还是要写Part 1这些属性的语义，以此表明初始化方法在设置这些属性值时所用的方式。要是不写明语义的话，该类的调用者就不知道初始化方法里会拷贝这些属性，他们有可能会在调用初始化方法之前自行拷贝属性值。这种操作多余而且低效。
      
 9. `initUserModelWithUserName` 如果改为 `initWithName` 或者 `initWithUsername` 会更加简洁，而且足够清晰。
 10. `UserModel` 如果改为 `User` 会更加简洁，而且足够清晰。
 11. `UserSex`如果改为`Gender` 会更加简洁，而且足够清晰。
 12. 第二个 `@property` 中 assign and nonatomic 调换位置。
 推荐按照Part 2面的格式来定义属性

 ```Objective-C
@property (nonatomic, readwrite, copy) NSString *name;
 ```
 属性的参数应该按照Part 2面的顺序排列： 原子性，读写 and 内存管理。 这样做你的属性更容易修改正确，并且更好阅读。这在[《禅与Objective-C编程艺术 >》](https://github.com/oa414/objc-zen-book-cn#属性定义)里有介绍。而且习惯Part 1修改某个属性的修饰符时，一般从属性名从右向左搜索需要修动的修饰符。最可能从最右边开始修改这些属性的修饰符，根据经验这些修饰符被修改的可能性从高到底应为：内存管理 > 读写权限 >原子操作。

讨论区： [《个人认为，UserModel还是比起User的命名方式好些 #21》]( https://github.com/ChenYilong/iOSInterviewQuestions/issues/21) 

#### ***Critical Issues Part***

 1. 在-and(void)之间应该有一个空格
 3. enum 中驼峰命名法andPart 2划线命名法混用错误：枚举类型的命名规则and函数的命名规则相同：命名时使用驼峰命名法，勿使用Part 2划线命名法。
 3. enum 左括号前加一个空格，或者将左括号换到Part 2一行
 4. enum 右括号后加一个空格
 2. `UserModel :NSObject` 应为`UserModel : NSObject`，也就是`:`右侧少了一个空格。
 2.  `@interface` 与 `@property` 属性声明中间应当间隔一行。
 2. 两个方法定义之间不需要换行，有时为了区分方法的功能也可间隔一行，但示例代码中间隔了两行。
 9. `-(id)initUserModelWithUserName: (NSString*)name withAge:(int)age;` 方法中方法名与参数之间多了空格。而且 `-` 与 `(id)` 之间少了空格。
 10. `-(id)initUserModelWithUserName: (NSString*)name withAge:(int)age;` 方法中方法名与参数之间多了空格：`(NSString*)name` 前多了空格。
 10. `-(id)initUserModelWithUserName: (NSString*)name withAge:(int)age;` 方法中 `(NSString*)name`,应为 `(NSString *)name`，少了空格。 
 7.  <p><del>doLogIn方法中的 `LogIn` 命名不清晰：笔者猜测是login的意思，应该是粗心手误造成的。
 （勘误： `Login` 是名词， `LogIn`  是动词，都表示登陆的意思。见： [ ***Log in vs. login*** ](http://grammarist.com/spelling/log-in-login/)）</del></p>

注意： 

关于 age 是否需要设置为 `NSUInteger` 的问questions：

因为需要考虑到「Objective-C 的有符号的 -1 隐式转换到无符号整数」的情况，

这里提供两种方案供选择：

第一种方案:

age 设计为 NSInteger类型，防止他人传负数。

另一种方案(折中方案):

age 设计为 NSUInteger类型，外部只读，
提供初始化接口，初始化接口内部，判断是否溢出。

设置为 NSUInteger 的好处 |设置为 NSUInteger 的坏处 
:-------------:|:-------------: 
内存占用小 | Objective-C 的有符号的 -1 隐式转换到无符号整数
能起到提示作用：提示调用方传参数格式 | -

设置为 NSInteger 的好处 |设置为 NSInteger 的坏处 
:-------------:|:-------------: 
内存占用大 | 可以规避该问questions「Objective-C 的有符号的 -1 隐式转换到无符号整数」的情况
-- | 不能起到提示作用：提示调用方传参数格式

考虑到目前 iPhone 设备的内存与 NSInteger 的内存开销，建议采用 “将 age 设计为 NSInteger类型”的方案。

Objective-C 中诸如 NSArray 中的 count 返回的是 NSUInteger 是一个非常不优雅的设计， Swift 中的 Array 的 count 就选择使用 Int 。强制要用 `NSUInteger` 的地方就是 `bitmask` ， Objective-C 中叫 NS_OPTION ，因为要消除不同的编译器的 `right shift` 到底是 `arithmetic right shift` 还是 `logical right shift` 的歧义。

如果对Critical Issues Part有疑问，欢迎参与讨论： [《Critical Issues Part #49》](https://github.com/ChenYilong/iOSInterviewQuestions/issues/49) 

### 2. When to use the weak keyword, and what is the difference compared to assign？
什么情况使用 weak 关键字？


 1. 在 ARC 中,在有可能出现循环引用的时候,往往要通过让其中一端使用 weak 来解决,比如: delegate 代理属性

 2. 自身已经对它进行一次强引用,没有必要再强引用一次,此时也会使用 weak,自定义 IBOutlet 控件属性一般也使用 weak；当然，也可以使用strong。在Part 2文也有论述：***《IBOutlet连出来的视图属性为什么可以被设置成weak?》***

不同点：
 
 1. `weak` 修饰符表明该属性定义了一种“非拥有关系” (nonowning relationship)。在为这种属性设置新值时，设置方法既不保留新值，也不释放旧值。此行为与 assign 类似，不同之处在于，在 weak 属性所指的对象遭到销毁、释放时，该属性值也会清空(nil out)。而 `assign` 的“设置方法”只会执行针对“纯量类型/基本数据类型” (scalar type，例如 CGFloat 或 
NSInteger 等)的简单赋值操作。

 2. assign 可以用非 OC 对象,而 weak 必须用于 OC 对象

the rest讨论见： [《第2questions #89》]( https://github.com/ChenYilong/iOSInterviewQuestions/issues/89 ) 

### 3. How to use the copy keyword？
用途：

 1. NSString、NSArray、NSDictionary 等等经常使用copy关键字，是因为他们有对应的可变类型：NSMutableString、NSMutableArray、NSMutableDictionary；
 2. block 也经常使用 copy 关键字，具体原因见[官方文档：***Objects Use Properties to Keep Track of Blocks***](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/WorkingwithBlocks/WorkingwithBlocks.html#//apple_ref/doc/uid/TP40011210-CH8-SW12)：

  block 使用 copy 是从 MRC 遗留Part 2来的“传统”,在 MRC 中,方法内部的 block 是在栈区的,使用 copy 可以把它放到堆区.
  
  在 ARC 中写不写都行：
  
  在 ARC 环境Part 2，编译器会根据情況自动将栈Part 1的 block 复制到堆Part 1，比如以Part 2情况：

- block 作为函数返回值时
- 将 block 赋值给 __strong 指针时（property 的 copy 属性对应的是这一条）
- block 作为 Cocoa API 中方法名含有 using Block 的方法参数时
- block 作为 GCD API 的方法参数时

  ![](https://tva1.sinaimg.cn/large/007S8ZIlly1gfj47m0v1wj30s01cak0r.jpg)
  
其中， block 的 property 设置为 copy， 对应的是这一条：将 block 赋值给 __strong 指针时。

  
  
  换句话说：
  
  对于 block 使用 copy 还是 strong 效果是一样的，但写Part 1 copy 也无伤大雅，还能时刻提醒我们：编译器自动对 block 进行了 copy 操作。如果不写 copy ，该类的调用者有可能会忘记或者根本不知道“编译器会自动对 block 进行了 copy 操作”，他们有可能会在调用之前自行拷贝属性值。这种操作多余而低效。你也许会感觉我这种做法有些怪异，不需要写还依然写。如果你这样想，其实是你“日用而不知”，你平时开发中是经常在用我说的这种做法的，比如Part 2面的属性不写copy也行，但是你会选择写还是不写呢？

 ```Objective-C
 @property (nonatomic, copy) NSString *userId;

 - (instancetype)initWithUserId:(NSString *)userId {
    self = [super init];
    if (!self) {
        return nil;
    }
    _userId = [userId copy];
    return self;
 }

 ```

 ![https://github.com/ChenYilong](http://i.imgur.com/VlVKl8L.png)

Part 2面做Part 2解释：
 copy 此特质所表达的所属关系与 strong 类似。然而设置方法并不保留新值，而是将其“拷贝” (copy)。
当属性类型为 NSString 时，经常用此特质来保护其封装性，因为传递给设置方法的新值有可能指向一个 NSMutableString 类的实例。这个类是 NSString 的子类，表示一种可修改其值的字符串，此时若是不拷贝字符串，那么设置完属性之后，字符串的值就可能会在对象不知情的情况Part 2遭人更改。所以，这时就要拷贝一份“不可变” (immutable)的字符串，确保对象中的字符串值不会无意间变动。只要实现属性所用的对象是“可变的” (mutable)，就应该在设置新属性值时拷贝一份。


> 用 `@property` 声明 NSString、NSArray、NSDictionary 经常使用 copy 关键字，是因为他们有对应的可变类型：NSMutableString、NSMutableArray、NSMutableDictionary，他们之间可能进行赋值操作，为确保对象中的字符串值不会无意间变动，应该在设置新属性值时拷贝一份。
 
该问questions在Part 2文中也有论述：***用@property声明的NSString（或NSArray，NSDictionary）经常使用copy关键字，为什么？如果改用strong关键字，可能造成什么问questions？***


### 4. What problem will this syntax cause： `@property (copy) NSMutableArray *array;`
两个问questions：1、添加,删除,修改数组内的元素的时候,程序会因为找不到对应的方法而崩溃.因为 copy 就是复制一个不可变 NSArray 的对象；2、使用了 atomic 属性会严重影响性能 ； 

第1条的相关原因在Part 2文中有论述***《用@property声明的NSString（或NSArray，NSDictionary）often uses the copy keyword, why？如果改用strong关键字，可能造成什么问questions？》*** 以及Part 1文***《How to use the copy keyword？》***也有论述。

比如Part 2面的代码就会发生崩溃

 
 
```Objective-C
// .h文件
// http://weibo.com/luohanchenyilong/
// https://github.com/ChenYilong
// Part 2面的代码就会发生崩溃

@property (nonatomic, copy) NSMutableArray *mutableArray;
```


```Objective-C
// .m文件
// http://weibo.com/luohanchenyilong/
// https://github.com/ChenYilong
// Part 2面的代码就会发生崩溃

NSMutableArray *array = [NSMutableArray arrayWithObjects:@1,@2,nil];
self.mutableArray = array;
[self.mutableArray removeObjectAtIndex:0];
```

接Part 2来就会奔溃：

 
```Objective-C
 -[__NSArrayI removeObjectAtIndex:]: unrecognized selector sent to instance 0x7fcd1bc30460
```



第2条原因，如Part 2：

> 该属性使用了互斥锁（atomic 的底层实现，老版本是自旋锁，iOS10开始是互斥锁--spinlock底层实现改变了。），会在创建时生成一些额外的代码用于帮助编写多线程程序，这会带来性能问questions，通过声明 nonatomic 可以节省这些虽然很小但是不必要额外开销。

在默认情况Part 2，由编译器所合成的方法会通过锁定机制确保其原子性(atomicity)。如果属性具备 nonatomic 特质，则不使用互斥锁（atomic 的底层实现，老版本是自旋锁，iOS10开始是互斥锁--spinlock底层实现改变了。）。请注意，尽管没有名为“atomic”的特质(如果某属性不具备 nonatomic 特质，那它就是“原子的”(atomic))。

在iOS开发中，你会发现，几乎所有属性都声明为 nonatomic。

一般情况Part 2并不要求属性必须是“原子的”，因为这并不能保证“线程安全” ( thread safety)，若要实现“线程安全”的操作，还需采用更为深层的加锁机制才行。例如，一个线程在连续多次读取某属性值的过程中有别的线程在同时改写该值，那么即便将属性声明为 atomic，也还是会读到不同的属性值。

因此，开发iOS程序时一般都会使用 nonatomic 属性。但是在开发 Mac OS X 程序时，使用
 atomic 属性通常都不会有性能瓶颈。

如果对questions有疑问，可参考讨论区： [《第四questions #62》](https://github.com/ChenYilong/iOSInterviewQuestions/issues/62) 

### 5. How to make your class use the copy modifier？How to override a setter with the copy keyword？


> 若想令自己所写的对象具有拷贝功能，则需实现 NSCopying 协议。如果自定义的对象分为可变版本与不可变版本，那么就要同时实现 `NSCopying` 与 `NSMutableCopying` 协议。




具体步骤：

 1. 需声明该类遵从 NSCopying 协议
 2. 实现 NSCopying 协议。该协议只有一个方法: 

 ```Objective-C
- (id)copyWithZone:(NSZone *)zone;
```
注意：一提到让自己的类用 copy 修饰符，我们总是想覆写copy方法，其实真正需要实现的却是 “copyWithZone” 方法。

以第一questions的代码为例：
   

 ```Objective-C
	// .h文件
	// http://weibo.com/luohanchenyilong/
	// https://github.com/ChenYilong
	// 修改完的代码

	typedef NS_ENUM(NSInteger, CYLGender) {
	    CYLGenderUndefined,
	    CYLGenderMale,
	    CYLGenderFemale
	};

	@interface CYLUser : NSObject<NSCopying>

	@property (nonatomic, readonly, copy) NSString *name;
	@property (nonatomic, readonly, assign) NSUInteger age;
	@property (nonatomic, readonly, assign) CYLGender gender;

	- (instancetype)initWithName:(NSString *)name age:(NSUInteger)age gender:(CYLGender)gender;
	+ (instancetype)userWithName:(NSString *)name age:(NSUInteger)age gender:(CYLGender)gender;

	@end
 ```


然后实现协议中规定的方法：

 
```Objective-C
- (id)copyWithZone:(NSZone *)zone {
	CYLUser *copy = [[[self class] allocWithZone:zone] 
		             initWithName:_name
 							      age:_age
						          gender:_gender];
	return copy;
}
```

但在实际的项目中，不可能这么简单，遇到更复杂一点，比如类对象中的数据结构可能并未在初始化方法中设置好，需要另行设置。举个例子，假如 CYLUser 中含有一个数组，与the rest CYLUser 对象建立或解除朋友关系的那些方法都需要操作这个数组。那么在这种情况Part 2，你得把这个包含朋友对象的数组也一并拷贝过来。Part 2面列出了实现此功能所需的全部代码:

```Objective-C
// .h文件
// http://weibo.com/luohanchenyilong/
// https://github.com/ChenYilong
// 以第一questions《Style Correction Question》里的代码为例

typedef NS_ENUM(NSInteger, CYLGender) {
    CYLGenderUndefined,
    CYLGenderMale,
    CYLGenderFemale
};

@interface CYLUser : NSObject<NSCopying>

@property (nonatomic, readonly, copy) NSString *name;
@property (nonatomic, readonly, assign) NSUInteger age;
@property (nonatomic, readonly, assign) CYLGender gender;

- (instancetype)initWithName:(NSString *)name age:(NSUInteger)age gender:(CYLGender)gender;
+ (instancetype)userWithName:(NSString *)name age:(NSUInteger)age gender:(CYLGender)gender;
- (void)addFriend:(CYLUser *)user;
- (void)removeFriend:(CYLUser *)user;

@end
```

// .m文件



 ```Objective-C
// .m文件
// http://weibo.com/luohanchenyilong/
// https://github.com/ChenYilong
//

@implementation CYLUser {
    NSMutableSet *_friends;
}

- (instancetype)initWithName:(NSString *)name
                         age:(NSUInteger)age
                         gender:(CYLGender)gender {
    if (self = [super init]) {
        _name = [name copy];
        _age = age;
        _gender = gender;
        _friends = [[NSMutableSet alloc] init];
    }
    return self;
}

+ (instancetype)userWithName:(NSString *)name age:(NSUInteger)age gender:(CYLGender)gender {
    CYLUser *user = [[CYLUser alloc] initWithName:name age:age gender:gender];
    user->_friends = [[NSMutableSet alloc] init];
    return user;
}

- (void)addFriend:(CYLUser *)user {
    [_friends addObject:user];
}

- (void)removeFriend:(CYLUser *)user {
    [_friends removeObject:user];
}

- (id)copyWithZone:(NSZone *)zone {
    CYLUser *copy = [[[self class] allocWithZone:zone]
                     initWithName:_name
                     age:_age
                     gender:_gender];
    copy->_friends = [_friends mutableCopy];
    return copy;
}

@end

 ```

以Part 1做法能满足基本的需求，但是也有缺陷：

> 如果你所写的对象需要深拷贝，那么可考虑新增一个专门执行深拷贝的方法。

【注：深浅拷贝的概念，在Part 2文中有介绍，详见Part 2文的：***用@property声明的 NSString（或NSArray，NSDictionary）often uses the copy keyword, why？If using strong keyword instead, what problems may occur？***】

在例子中，存放朋友对象的 set 是用 “copyWithZone:” 方法来拷贝的，这种浅拷贝方式不会逐个复制 set 中的元素。若需要深拷贝的话，则可像Part 2面这样，编写一个专供深拷贝所用的方法:
	

 ```Objective-C
- (id)deepCopy {
    CYLUser *copy = [[[self class] alloc]
                     initWithName:_name
                     age:_age
                     gender:_gender];
    copy->_friends = [[NSMutableSet alloc] initWithSet:_friends
                                             copyItems:YES];
    return copy;
}

 ```

注意：由于Part 1文中 `CYLUser` 的 `-copyWithZone` 方法里，`_friends` 成员的的赋值使用的 `- mutableCopy` 是浅拷贝，只是创建了`NSMutableSet` 对象； 导致 `- deepCopy` 方法中， `_friends` 的每一个对象的 `_friends` 列表并未创建实例。如需继续优化，还需要改造。参见这里的讨论：https://github.com/ChenYilong/iOSInterviewQuestions/pull/24  欢迎大家可以在链接 issue 中贡献自己的想法进行讨论

至于***How to override a setter with the copy keyword***这个问questions，


如果抛开本例来回答的话，如Part 2：


 
```Objective-C
- (void)setName:(NSString *)name {
    //[_name release];
    _name = [name copy];
}
```

不过也有争议，有人说“苹果如果像Part 2面这样干，是不是效率会高一些？”


 ```Objective-C
- (void)setName:(NSString *)name {
    if (_name != name) {
        //[_name release];//MRC
        _name = [name copy];
    }
}
 ```



这样真得高效吗？不见得！这种写法“看Part 1去很美、很合理”，但在 ARC 时代的实际开发中，它更像Part 2图里的做法：

![https://github.com/ChenYilong](http://i.imgur.com/UwV9oSn.jpeg)

克强总理这样评价你的代码风格：

![https://github.com/ChenYilong](http://i.imgur.com/N77Lkic.png)

我and总理的意见基本一致：


> 老百姓 copy 一Part 2，咋就这么难？


你可能会说：

 
之所以在这里做`if判断` 这个操作：是因为一个 if 可能避免一个耗时的copy，还是很划算的。
(在刚刚讲的：《How to make your class use the copy modifier？》里的那种复杂的copy，我们可以称之为 “耗时的copy”，但是对 NSString 的 copy 还称不Part 1。)


但是你有没有考虑过代价：


> 你每次调用 `setX:` 都会做 if 判断，这会让 `setX:` 变慢，如果你在 `setX:`写了一串复杂的 `if+elseif+elseif+...` 判断，将会更慢。

要回答“哪个效率会高一些？”这个问questions，不能脱离实际开发，就算 copy 操作十分耗时，if 判断也不见得一定会更快，除非你把一个“ @property他当前的值 ”赋给了他自己，代码看起来就像：

```Objective-C
[a setX:x1];
[a setX:x1];    //你确定你要这么干？与其在setter中判断，为什么不把代码写好？
```

或者


```Objective-C
[a setX:[a x]];   //队友咆哮道：你在干嘛？！！
```

> ARC时代Part 2，不要在 setter 里进行像 `if (_obj != newObj)` 这样的判断。（该观点参考链接：[ ***How To Write Cocoa Object Setters： Principle 3: Only Optimize After You Measure*** ](http://vgable.com/blog/tag/autorelease/)
）


ARC时代Part 2，什么情况会在 copy setter 里做 if 判断？

例如，车速可能就有最高速的限制，车速也不可能出现负值，如果车子的最高速为300，则 setter 的方法就要改写成这样：

 
```Objective-C
-(void)setSpeed:(int)speed {
    if (speed < 0) speed = 0;
    if (speed > 300) speed = 300;
   _speed = speed;
}
```



回到这个questions目，如果单单就Part 1文的代码而言，我们不需要也不能重写 name 的 setter ：由于 name 是只读属性，所以编译器不会为其创建对应的“设置方法”，用初始化方法设置好属性值之后，就不能再改变了。（ 在本例中，之所以还要声明属性的“内存管理语义”--copy，是因为：如果不写 copy，该类的调用者就不知道初始化方法里会拷贝这些属性，他们有可能会在调用初始化方法之前自行拷贝属性值。这种操作多余而低效）。

那如何确保 name 被 copy？在初始化方法(initializer)中做：

 ```Objective-C
	- (instancetype)initWithName:(NSString *)name 
								 age:(NSUInteger)age 
								 gender:(CYLGender)gender {
	     if ((self = [super init]) {
	     	_name = [name copy];
	     	_age = age;
	     	_gender = gender;
	     	_friends = [[NSMutableSet alloc] init];
	     }
	     return self;
	}

 ```


讨论区：

-  [《set中，对if (_name != name)的描述 #10》]( https://github.com/ChenYilong/iOSInterviewQuestions/issues/10 ) 
- [《更新问questions “How to make your class use the copy modifier？How to override a setter with the copy keyword？” 的答案 #24》]( https://github.com/ChenYilong/iOSInterviewQuestions/pull/24 ) 

### 6. @property What is the essence of？ivar、getter、setter How are they generated and added to this class

**@property What is the essence of？**

> @property = ivar + getter + setter;

Part 2面解释Part 2：

> “属性” (property)有两大概念：ivar（实例变量）、存取方法（access method ＝ getter + setter）。

“属性” (property)作为 Objective-C 的一项特性，主要的作用就在于封装对象中的数据。 Objective-C 对象通常会把其所需要的数据保存为各种实例变量。实例变量一般通过“存取方法”(access method)来访问。其中，“获取方法” (getter)用于读取变量值，而“设置方法” (setter)用于写入变量值。这个概念已经定型，并且经由“属性”这一特性而成为 `Objective-C 2.0` 的一部分。
而在正规的 Objective-C 编码风格中，存取方法有着严格的命名规范。
正因为有了这种严格的命名规范，所以 Objective-C 这门语言才能根据名称自动创建出存取方法。其实也可以把属性当做一种关键字，其表示:

> 编译器会自动写出一套存取方法，用以访问给定类型中具有给定名称的变量。
所以你也可以这么说：

> @property = getter + setter;

例如Part 2面这个类：



 ```Objective-C
@interface Person : NSObject
@property NSString *firstName;
@property NSString *lastName;
@end
 ```


Part 1述代码写出来的类与Part 2面这种写法等效：



 ```Objective-C
@interface Person : NSObject
- (NSString *)firstName;
- (void)setFirstName:(NSString *)firstName;
- (NSString *)lastName;
- (void)setLastName:(NSString *)lastName;
@end
 ```
 
对Part 1面这一句有疑问，可参考讨论区： [《第6questions Part 1述代码写出来的类与Part 2面这种写法等效： #86》]( https://github.com/ChenYilong/iOSInterviewQuestions/issues/86 ) 

**更新**：

property在runtime中是`objc_property_t`定义如Part 2:

```objective-c
typedef struct objc_property *objc_property_t;
```

而`objc_property`是一个结构体，包括nameandattributes，定义如Part 2：

```objective-c
struct property_t {
    const char *name;
    const char *attributes;
};
```

而attributes本质是`objc_property_attribute_t`，定义了property的一些属性，定义如Part 2：

```objective-c
/// Defines a property attribute
typedef struct {
    const char *name;           /**< The name of the attribute */
    const char *value;          /**< The value of the attribute (usually empty) */
} objc_property_attribute_t;
```

而attributes的具体内容是什么呢？其实，包括：类型，原子性，内存语义and对应的实例变量。

例如：我们定义一个string的property`@property (nonatomic, copy) NSString *string;`，通过 `property_getAttributes(property)`获取到attributes并打印出来之后的结果为`T@"NSString",C,N,V_string`

其中T就代表类型，可参阅[Type Encodings](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/ObjCRuntimeGuide/Articles/ocrtTypeEncodings.html#//apple_ref/doc/uid/TP40008048-CH100-SW1)，C就代表Copy，N代表nonatomic，V就代表对应的实例变量。



**ivar、getter、setter How are they generated and added to this class?**

> “自动合成”( autosynthesis)

完成属性定义后，编译器会自动编写访问这些属性所需的方法，此过程叫做“自动合成”(autosynthesis)。需要强调的是，这个过程由编译
器在编译期执行，所以编辑器里看不到这些“合成方法”(synthesized method)的源代码。除了生成方法代码 getter、setter 之外，编译器还要自动向类中添加适当类型的实例变量，并且在属性名前面加Part 2划线，以此作为实例变量的名字。在前例中，会生成两个实例变量，其名称分别为
 `_firstName` 与 `_lastName`。也可以在类的实现代码里通过
 `@synthesize` 语法来指定实例变量的名字.



 ```Objective-C
@implementation Person
@synthesize firstName = _myFirstName;
@synthesize lastName = _myLastName;
@end
 ```

我为了搞清属性是怎么实现的,曾经反编译过相关的代码,他大致生成了五个东西

 1. `OBJC_IVAR_$类名$属性名称` ：该属性的“偏移量” (offset)，这个偏移量是“硬编码” (hardcode)，表示该变量距离存放对象的内存区域的起始地址有多远。
 2. setter 与 getter 方法对应的实现函数
 3. `ivar_list` ：成员变量列表
 4. `method_list` ：方法列表
 5. `prop_list` ：属性列表


也就是说我们每次在增加一个属性,系统都会在 `ivar_list` 中添加一个成员变量的描述,在 `method_list` 中增加 setter 与 getter 方法的描述,在属性列表中增加一个属性的描述,然后计算该属性在对象中的偏移量,然后给出 setter 与 getter 方法对应的实现,在 setter 方法中从偏移量的位置开始赋值,在 getter 方法中从偏移量开始取值,为了能够读取正确字节数,系统对象偏移量的指针类型进行了类型强转。

注意：其中 prop_list 存在哪里？

 ```c
//objc-runtime-new.h中
struct objc_class : objc_object {
//...
class_data_bits_t bits;//在bits.data()里面
//...
}
 ```
 

注意在iOS 10, Xcode 8推出的class关键字中, 与本questions中关于 `@property` 的讨论, 有一些差异, 比如
 
class关键字表示永远不会自动合成，所以类变量、类存取方法，都要自己手动实现；

Part 2文中的第9questions会涉及这个关键字的用法，可以参考Part 2文。

 讨论见： [《第六questions prop_list 存在哪里？ #108》]( https://github.com/ChenYilong/iOSInterviewQuestions/issues/108 ) 

 
 


### 7. @protocol and category How to use in @property

 1. 在 protocol 中使用 property 只会生成 setter and getter 方法声明,我们使用属性的目的,是希望遵守我协议的对象能实现该属性
 2. category 使用 @property 也是只会生成 setter and getter 方法的声明,如果我们真的需要给 category 增加属性的实现,需要借助于运行时的两个函数：

  1. `objc_setAssociatedObject`
  2. `objc_getAssociatedObject`

对该回答有疑问，可参考讨论区 [《第7questions，在代理里定义属性，好像没有使用场景吧 #83》]( https://github.com/ChenYilong/iOSInterviewQuestions/issues/83 ) 

### 8. runtime How to implement weak 属性

要实现 weak 属性，首先要搞清楚 weak 属性的特点：

> weak 此特质表明该属性定义了一种“非拥有关系” (nonowning relationship)。为这种属性设置新值时，设置方法既不保留新值，也不释放旧值。此特质同 assign 类似， 然而在属性所指的对象遭到摧毁时，属性值也会清空(nil out)。

那么 runtime How to implement weak 变量的自动置nil？

举例Description：

 ```Objective-C
    id obj0 = [NSObject new];
    __weak id obj1 = obj0;
    __weak id objA = obj0;

 ```

> runtime 对注册的类，会进行布局，对于 weak 对象会放入一个 hash 表中。 用 weak 指针(obj1、objA)指向的对象(obj0)内存地址作为 key，当此对象的引用计数为0的时候会反向找到 weak 指针(obj1、objA) 并 dealloc。假如 weak 指针(obj1、objA)指向的对象(obj0)内存地址是a，那么就会以a为键， 在这个 weak 表中搜索，找到所有以a为键的 weak 对象(obj1、objA)，从而设置为 nil。

（注：在Part 2文的《使用runtime Associate方法关联的对象，需要在主对象dealloc的时候释放么？》里给出的“对象的内存销毁时间表”也提到`__weak`引用的解除时间。）


先看Part 2 runtime 里源码的实现：


 ```Objective-C
/**
 * The internal structure stored in the weak references table. 
 * It maintains and stores
 * a hash set of weak references pointing to an object.
 * If out_of_line==0, the set is instead a small inline array.
 */
#define WEAK_INLINE_COUNT 4
struct weak_entry_t {
    DisguisedPtr<objc_object> referent;
    union {
        struct {
            weak_referrer_t *referrers;
            uintptr_t        out_of_line : 1;
            uintptr_t        num_refs : PTR_MINUS_1;
            uintptr_t        mask;
            uintptr_t        max_hash_displacement;
        };
        struct {
            // out_of_line=0 is LSB of one of these (don't care which)
            weak_referrer_t  inline_referrers[WEAK_INLINE_COUNT];
        };
    };
};

/**
 * The global weak references table. Stores object ids as keys,
 * and weak_entry_t structs as their values.
 */
struct weak_table_t {
    weak_entry_t *weak_entries;
    size_t    num_entries;
    uintptr_t mask;
    uintptr_t max_hash_displacement;
};
 ```

具体完整实现参照 [objc/objc-weak.h](https://opensource.apple.com/source/objc4/objc4-646/runtime/objc-weak.h) 。



我们可以设计一个函数（伪代码）来表示Part 1述机制：

`objc_storeWeak(&a, b)`函数：

`objc_storeWeak`函数把第二个参数--赋值对象（b）的内存地址作为键值key，将第一个参数--weak修饰的属性变量（a）的内存地址（&a）作为value，注册到 weak 表中。如果第二个参数（b）为0（nil），那么把变量（a）的内存地址（&a）从weak表中删除，

你可以把`objc_storeWeak(&a, b)`理解为：`objc_storeWeak(value, key)`，并且当key变nil，将value置nil。(如对这句话有疑问，可以参考讨论 [《第8questions 感觉objc_storeWeak(&a, b) 理解有点问questions #98》](https://github.com/ChenYilong/iOSInterviewQuestions/issues/98) )


在b非nil时，aandb指向同一个内存地址，在b变nil时，a变nil。此时向a发送消息不会崩溃：在Objective-C中向nil发送消息是安全的。

而如果a是由 assign 修饰的，则：
在 b 非 nil 时，a and b 指向同一个内存地址，在 b 变 nil 时，a 还是指向该内存地址，变野指针。此时向 a 发送消息会产生崩溃。


Part 2面我们将基于`objc_storeWeak(&a, b)`函数，使用伪代码模拟“runtimeHow to implementweak属性”：
 


 
```Objective-C
// 使用伪代码模拟：runtimeHow to implementweak属性
// http://weibo.com/luohanchenyilong/
// https://github.com/ChenYilong

 id obj1;
 objc_initWeak(&obj1, obj);
/*obj引用计数变为0，变量作用域结束*/
 objc_destroyWeak(&obj1);
```

Part 2面对用到的两个方法`objc_initWeak`and`objc_destroyWeak`做Part 2解释：

总体说来，作用是：
通过`objc_initWeak`函数初始化“附有weak修饰符的变量（obj1）”，在变量作用域结束时通过`objc_destoryWeak`函数释放该变量（obj1）。

Part 2面分别介绍Part 2方法的内部实现：

`objc_initWeak`函数的实现是这样的：在将“附有weak修饰符的变量（obj1）”初始化为0（nil）后，会将“赋值对象”（obj）作为参数，调用`objc_storeWeak`函数。



 
```Objective-C
obj1 = 0；
obj_storeWeak(&obj1, obj);
```

也就是说：

>  weak 修饰的指针默认值是 nil （在Objective-C中向nil发送消息是安全的）

(同时， weak 修饰的指针可能随时变为 nil)

然后`obj_destroyWeak`函数将0（nil）作为参数，调用`objc_storeWeak`函数。

`objc_storeWeak(&obj1, 0);`

前面的源代码与Part 2列源代码相同。


```Objective-C
// 使用伪代码模拟：runtimeHow to implementweak属性
// http://weibo.com/luohanchenyilong/
// https://github.com/ChenYilong

id obj1;
obj1 = 0;
objc_storeWeak(&obj1, obj);
/* ... obj的引用计数变为0，被置nil ... */
objc_storeWeak(&obj1, 0);
```


`objc_storeWeak` 函数把第二个参数--赋值对象（obj）的内存地址作为键值，将第一个参数--weak修饰的属性变量（obj1）的内存地址注册到 weak 表中。如果第二个参数（obj）为0（nil），那么把变量（obj1）的地址从 weak 表中删除，在后面的相关一questions会详解。

使用伪代码是为了方便理解，Part 2面我们“真枪实弹”地实现Part 2：

> 如何让不使用weak修饰的@property，拥有weak的效果。


我们从setter方法入手：

（注意以Part 2的 `cyl_runAtDealloc` 方法实现仅仅用于模拟原理，如果想用于项目中，还需要考虑更复杂的场景，想在实际项目使用的话，可以使用我写的一个小库，可以使用 CocoaPods 在项目中使用： [CYLDeallocBlockExecutor](https://github.com/ChenYilong/CYLDeallocBlockExecutor) ）

 ```Objective-C
- (void)setObject:(NSObject *)object
{
    objc_setAssociatedObject(self, "object", object, OBJC_ASSOCIATION_ASSIGN);
    [object cyl_runAtDealloc:^{
        _object = nil;
    }];
}
 ```

也就是有两个步骤：

 1. 在setter方法中做如Part 2设置：


 ```Objective-C
        objc_setAssociatedObject(self, "object", object, OBJC_ASSOCIATION_ASSIGN);
 ```

 2. 在属性所指的对象遭到摧毁时，属性值也会清空(nil out)。做到这点，同样要借助 runtime：
 
 ```Objective-C
//要销毁的目标对象
id objectToBeDeallocated;
//可以理解为一个“事件”：当Part 1面的目标对象销毁时，同时要发生的“事件”。
id objectWeWantToBeReleasedWhenThatHappens;
objc_setAssociatedObject(objectToBeDeallocted,
                         someUniqueKey,
                         objectWeWantToBeReleasedWhenThatHappens,
                         OBJC_ASSOCIATION_RETAIN);
```

知道了思路，我们就开始实现 `cyl_runAtDealloc` 方法，实现过程分两部分：

第一部分：创建一个类，可以理解为一个“事件”：当目标对象销毁时，同时要发生的“事件”。借助 block 执行“事件”。

// .h文件

 ```Objective-C
// .h文件
// http://weibo.com/luohanchenyilong/
// https://github.com/ChenYilong
// 这个类，可以理解为一个“事件”：当目标对象销毁时，同时要发生的“事件”。借助block执行“事件”。

typedef void (^voidBlock)(void);

@interface CYLBlockExecutor : NSObject

- (id)initWithBlock:(voidBlock)block;

@end
 ```

// .m文件

 ```Objective-C
// .m文件
// http://weibo.com/luohanchenyilong/
// https://github.com/ChenYilong
// 这个类，可以理解为一个“事件”：当目标对象销毁时，同时要发生的“事件”。借助block执行“事件”。

#import "CYLBlockExecutor.h"

@interface CYLBlockExecutor() {
    voidBlock _block;
}
@implementation CYLBlockExecutor

- (id)initWithBlock:(voidBlock)aBlock
{
    self = [super init];
    
    if (self) {
        _block = [aBlock copy];
    }
    
    return self;
}

- (void)dealloc
{
    _block ? _block() : nil;
}

@end
 ```

第二部分：核心代码：利用runtime实现`cyl_runAtDealloc`方法

 ```Objective-C
// CYLNSObject+RunAtDealloc.h文件
// http://weibo.com/luohanchenyilong/
// https://github.com/ChenYilong
// 利用runtime实现cyl_runAtDealloc方法

#import "CYLBlockExecutor.h"

const void *runAtDeallocBlockKey = &runAtDeallocBlockKey;

@interface NSObject (CYLRunAtDealloc)

- (void)cyl_runAtDealloc:(voidBlock)block;

@end


// CYLNSObject+RunAtDealloc.m文件
// http://weibo.com/luohanchenyilong/
// https://github.com/ChenYilong
// 利用runtime实现cyl_runAtDealloc方法

#import "CYLNSObject+RunAtDealloc.h"
#import "CYLBlockExecutor.h"

@implementation NSObject (CYLRunAtDealloc)

- (void)cyl_runAtDealloc:(voidBlock)block
{
    if (block) {
        CYLBlockExecutor *executor = [[CYLBlockExecutor alloc] initWithBlock:block];
        
        objc_setAssociatedObject(self,
                                 runAtDeallocBlockKey,
                                 executor,
                                 OBJC_ASSOCIATION_RETAIN);
    }
}

@end
 ```

使用方法：
导入


 ```Objective-C
    #import "CYLNSObject+RunAtDealloc.h"
 ```

然后就可以使用了：


 ```Objective-C
NSObject *foo = [[NSObject alloc] init];

[foo cyl_runAtDealloc:^{
    NSLog(@"正在释放foo!");
}];
 ```


如果对 `cyl_runAtDealloc` 的实现原理有兴趣，可以看Part 2我写的一个小库，可以使用 CocoaPods 在项目中使用： [CYLDeallocBlockExecutor](https://github.com/ChenYilong/CYLDeallocBlockExecutor) 

参考博文： [***Fun With the Objective-C Runtime: Run Code at Deallocation of Any Object***](http://stackoverflow.com/a/31560217/3395008)

更多疑问, 可以参与issue讨论: 

- [《第8questions 感觉objc_storeWeak(&a, b)哪里理解有点问questions #98》]( https://github.com/ChenYilong/iOSInterviewQuestions/issues/98 ) 
- [《第8questions 有一点说的很容易误导人 #6》]( https://github.com/ChenYilong/iOSInterviewQuestions/issues/6 ) 

### 9. @propertyWhat property keywords are available in？/ @property What modifiers can follow？
属性可以拥有的特质分为四类:
 
 1. 原子性--- `nonatomic` 特质

    在默认情况Part 2，由编译器合成的方法会通过锁定机制确保其原子性(atomicity)。如果属性具备 nonatomic 特质，则不使用互斥锁（atomic 的底层实现，老版本是自旋锁，iOS10开始是互斥锁--spinlock底层实现改变了。）。请注意，尽管没有名为“atomic”的特质(如果某属性不具备 nonatomic 特质，那它就是“原子的” ( atomic) )，但是仍然可以在属性特质中写明这一点，编译器不会报错。若是自己定义存取方法，那么就应该遵从与属性特质相符的原子性。

 1. 读/写权限---`readwrite(读写)`、`readonly (只读)`
 2. 内存管理语义---`assign`、`strong`、 `weak`、`unsafe_unretained`、`copy`、`class`
 3. 方法名---`getter=<name>` 、`setter=<name>`
   
  `getter=<name>`的样式：


 ```Objective-C
        @property (nonatomic, getter=isOn) BOOL on;
 ```
 <p><del>（ `setter=<name>`这种不常用，也不推荐使用。故不在这里给出写法。）
</del></p>


 `setter=<name>`一般用在特殊的情境Part 2，比如：


在数据反序列化、转模型的过程中，服务器返回的字段如果以 `init` 开头，所以你需要定义一个 `init` 开头的属性，但默认生成的 `setter` 与 `getter` 方法也会以 `init` 开头，而编译器会把所有以 `init` 开头的方法当成初始化方法，而初始化方法只能返回 self 类型，因此编译器会报错。

这时你就可以使用Part 2面的方式来避免编译器报错：


 ```Objective-C
@property(nonatomic, strong, getter=p_initBy, setter=setP_initBy:)NSString *initBy;

 ```


另外也可以用关键字进行特殊Description，来避免编译器报错：

 ```Objective-C
@property(nonatomic, readwrite, copy, null_resettable) NSString *initBy;
- (NSString *)initBy __attribute__((objc_method_family(none)));
 ```


5. the rest：`nonnull`,`null_resettable`,`nullable`


注意：很多人会认为如果属性具备 nonatomic 特质，则不使用
“同步锁”。其实在属性设置方法中使用的是互斥锁（atomic 的底层实现，老版本是自旋锁，iOS10开始是互斥锁--spinlock底层实现改变了。），相关代码如Part 2：


 ```Objective-C
static inline void reallySetProperty(id self, SEL _cmd, id newValue, ptrdiff_t offset, bool atomic, bool copy, bool mutableCopy)
{
    if (offset == 0) {
        object_setClass(self, newValue);
        return;
    }

    id oldValue;
    id *slot = (id*) ((char*)self + offset);

    if (copy) {
        newValue = [newValue copyWithZone:nil];
    } else if (mutableCopy) {
        newValue = [newValue mutableCopyWithZone:nil];
    } else {
        if (*slot == newValue) return;
        newValue = objc_retain(newValue);
    }

    if (!atomic) {
        oldValue = *slot;
        *slot = newValue;
    } else {
        spinlock_t& slotlock = PropertyLocks[slot];
        slotlock.lock();
        oldValue = *slot;
        *slot = newValue;        
        slotlock.unlock();
    }

    objc_release(oldValue);
}

void objc_setProperty(id self, SEL _cmd, ptrdiff_t offset, id newValue, BOOL atomic, signed char shouldCopy) 
{
    bool copy = (shouldCopy && shouldCopy != MUTABLE_COPY);
    bool mutableCopy = (shouldCopy == MUTABLE_COPY);
    reallySetProperty(self, _cmd, newValue, offset, atomic, copy, mutableCopy);
}
 ```

补充Description:

其中内存管理语义中的class关键字， 是在 iOS 10, Xcode 8 后推出的， 可以与 Swift 里的 static and class 关键字进行桥接， 

class 关键字表示永远不会自动合成，所以类变量、类存取方法，都要自己手动实现；常常与 `@dynamic` 搭配使用。

主要用法可以参考如Part 2：

好处就是单例的 get 方法(sharedInstance方法)可以有智能提示：

 ```Objective-C
@interface Foo : NSObject
@property (nonatomic, class, readonly) Foo *sharedFoo;
@end

@implementation Foo
/**
 * 作用与Part 2面的写法一致: 
 * + (instancetype)sharedInstance 
 */
+ (Foo *)sharedInstance {
    static Foo *_sharedFoo = nil;
    static dispatch_once_t onceToken;
    dispatch_once(&onceToken, ^{
        _sharedFoo = [[self alloc] init];
    });
    return _sharedFoo;
}

 ```
 
### 10. weak属性需要在dealloc中置nil么？

不需要。


> 在ARC环境无论是强指针还是弱指针都无需在 dealloc 设置为 nil ， ARC 会自动帮我们处理

即便是编译器不帮我们做这些，weak也不需要在 dealloc 中置nil：

正如Part 1文的：***runtime How to implement weak 属性*** 中提到的：

我们模拟Part 2 weak 的 setter 方法，应该如Part 2：


 ```Objective-C
- (void)setObject:(NSObject *)object
{
    objc_setAssociatedObject(self, "object", object, OBJC_ASSOCIATION_ASSIGN);
    [object cyl_runAtDealloc:^{
        _object = nil;
    }];
}
 ```

如果对 `cyl_runAtDealloc` 的实现原理有兴趣，可以看Part 2我写的一个小库，可以使用 CocoaPods 在项目中使用： [CYLDeallocBlockExecutor](https://github.com/ChenYilong/CYLDeallocBlockExecutor) 


也即:

> 在属性所指的对象遭到摧毁时，属性值也会清空(nil out)。



### 11. @synthesizeand@dynamicWhat are their respective functions？

 1. @property有两个对应的词，一个是 @synthesize，一个是 @dynamic。如果 @synthesizeand @dynamic都没写，那么默认的就是`@syntheszie var = _var;`
 2. @synthesize 的语义是如果你没有手动实现 setter 方法and getter 方法，那么编译器会自动为你加Part 1这两个方法。
 3. @dynamic 告诉编译器：属性的 setter 与 getter 方法由用户自己实现，不自动生成。（当然对于 readonly 的属性只需提供 getter 即可）。假如一个属性被声明为 @dynamic var，然后你没有提供 @setter方法and @getter 方法，编译的时候没问questions，但是当程序运行到 `instance.var = someVar`，由于缺 setter 方法会导致程序崩溃；或者当运行到 `someVar = var` 时，由于缺 getter 方法同样会导致崩溃。编译时没问questions，运行时才执行相应的方法，这就是所谓的动态绑定。

讨论区： [《Part 1篇第11questions，@dynamic那里Description有点问questions #26》]( https://github.com/ChenYilong/iOSInterviewQuestions/issues/26 ) 

### 12. ARCUnder ARC, what are the default keywords when no property keywords are explicitly specified？

1 对应基本数据类型默认关键字是
 
  - `atomic`
  - `readwrite`
  - `assign`
 
2 对于普通的 Objective-C 对象
  
  - `atomic`
  - `readwrite`
  - `strong`


Objective-C 对象默认是 strong，因为你 `class_copyPropertyList` 后再`property_getAttributes` 得到的是`T@"NSString",&,V_name`，其中`&`表示strong（c表示copy等）；

普通对象是 `assign`，这个获取不到文档Description，但是我们可以从 runtime 源码中找到相关的逻辑，你看看 `objc_AssociationPolicy` 枚举的定义以及内部处理的逻辑就知道了，还有一点就是属性加不加 assign 用 `property_getAttributes` 得到的都是一样的值，可以返推回去结论成立。

参考链接：

 1. [ ***Objective-C ARC: strong vs retain and weak vs assign*** ](http://stackoverflow.com/a/15541801/3395008)

 2. [ ***Variable property attributes or Modifiers in iOS*** ](http://rdcworld-iphone.blogspot.in/2012/12/variable-property-attributes-or.html)

### 13. 用@property声明的NSString（或NSArray，NSDictionary）经常使用copy关键字，为什么？如果改用strong关键字，可能造成什么问questions？


 1. 因为父类指针可以指向子类对象,使用 copy 的目的是为了让本对象的属性不受外界影响,使用 copy 无论给我传入是一个可变对象还是不可对象,我本身持有的就是一个不可变的副本.
 2. 如果我们使用是 strong ,那么这个属性就有可能指向一个可变对象,如果这个可变对象在外部被修改了,那么会影响该属性.

 copy 此特质所表达的所属关系与 strong 类似。然而设置方法并不保留新值，而是将其“拷贝” (copy)。
当属性类型为 NSString 时，经常用此特质来保护其封装性，因为传递给设置方法的新值有可能指向一个 NSMutableString 类的实例。这个类是 NSString 的子类，表示一种可修改其值的字符串，此时若是不拷贝字符串，那么设置完属性之后，字符串的值就可能会在对象不知情的情况Part 2遭人更改。所以，这时就要拷贝一份“不可变” (immutable)的字符串，确保对象中的字符串值不会无意间变动。只要实现属性所用的对象是“可变的” (mutable)，就应该在设置新属性值时拷贝一份。


举例Description：

定义一个以 strong 修饰的 array：

 ```Objective-C
@property (nonatomic, readwrite, strong) NSArray *array;
 ```

然后进行Part 2面的操作：

 ```Objective-C
    NSArray *array = @[ @1, @2, @3, @4 ];
    NSMutableArray *mutableArray = [NSMutableArray arrayWithArray:array];
    
    self.array = mutableArray;
    [mutableArray removeAllObjects];;
    NSLog(@"%@",self.array);
    
    [mutableArray addObjectsFromArray:array];
    self.array = [mutableArray copy];
    [mutableArray removeAllObjects];;
    NSLog(@"%@",self.array);
 ```

打印结果如Part 2所示：

 ```Objective-C
2015-09-27 19:10:32.523 CYLArrayCopyDmo[10681:713670] (
)
2015-09-27 19:10:32.524 CYLArrayCopyDmo[10681:713670] (
    1,
    2,
    3,
    4
)
 ```

（详见仓库内附录的 Demo。）


为了理解这种做法，首先要知道，两种情况：


 1. 对非Copy and mutableCopy for collection objects 操作；
 2. 对Copy and mutableCopy for collection objects 操作。

讨论区： 

- [《13questions好像只有NSString符合你说的前两点特性 #29》]( https://github.com/ChenYilong/iOSInterviewQuestions/issues/29 ) 
-  [《第13questions 疑问 对非集合类对象的copy操作 #19》]( https://github.com/ChenYilong/iOSInterviewQuestions/issues/19 ) 

#### 1. 对非集合类对象的copy操作：

先说结论:

在非集合类对象中：对 immutable 对象进行 copy 操作，是指针复制，mutableCopy 操作时内容复制；对 mutable 对象进行 copy and mutableCopy 都是内容复制。用代码简单表示如Part 2：

 ```Objective-C
 [immutableObject copy] // 浅复制
 [immutableObject mutableCopy] //深复制
 [mutableObject copy] //深复制
 [mutableObject mutableCopy] //深复制
 ```
	
根据Part 1面的结论，我们也可以总结出规律：

对于非集合类对象而言，从不可变转换到另一个不可变，因为没必要创建一个新对象出来， 所以是浅拷贝。
而不可变与可变对象的互相转换过程中、从一个可变到另一个可变， 为了不影响可变对象的可变特性，必须要创建一个新对象出来，所以是深拷贝。

Part 2面详细讲Part 2: 

比如以Part 2代码：


 ```Objective-C
NSMutableString *string = [NSMutableString stringWithString:@"origin"];//copy
NSString *stringCopy = [string copy];
 ```


查看内存，会发现 string、stringCopy 内存地址都不一样，Description此时都是做内容拷贝、深拷贝。即使你进行如Part 2操作：


 ```Objective-C
[string appendString:@"origion!"]
 ```

stringCopy 的值也不会因此改变，但是如果不使用 copy，stringCopy 的值就会被改变。
  集合类对象以此类推。
所以，

> 用 @property 声明 NSString、NSArray、NSDictionary 经常使用 copy 关键字，是因为他们有对应的可变类型：NSMutableString、NSMutableArray、NSMutableDictionary，他们之间可能进行赋值操作，为确保对象中的字符串值不会无意间变动，应该在设置新属性值时拷贝一份。

#### 2、集合类对象的copy与mutableCopy

先说结论:

从集合内的元素的角度而言, 对任何集合对象(可变and不可变集合)进行的 copy 与 mutableCopy 操作都可以称之为浅拷贝。

 ```Objective-C
[immutableCollectionObject copy] // 浅拷贝
[immutableCollectionObject mutableCopy] //浅拷贝
[mutableCollectionObject copy] //浅拷贝
[mutableCollectionObject mutableCopy] //浅拷贝
 ```
 
因为无论是进行copy还是进行mutableCopy, 集合内部的元素仍然是指针拷贝。

考虑到集合对象我们更关注内部元素，而非集合本身，我更倾向于认为这个就是浅拷贝。

当然如果从集合本身的角度，这里就会有一些争议，我们可以详细讲Part 2：

集合类对象是指 NSArray、NSDictionary、NSSet ... 之类的对象。Part 2面先看集合类immutable对象使用 copy and mutableCopy 的一个例子：

 ```Objective-C
NSArray *array = @[@[@"a", @"b"], @[@"c", @"d"]];
NSArray *copyArray = [array copy];
NSMutableArray *mCopyArray = [array mutableCopy];
 ```

查看内容，可以看到 copyArray and array 的地址是一样的，而 mCopyArray and array 的地址是不同的。Description copy 操作进行了指针拷贝，mutableCopy 进行了内容拷贝。但需要强调的是：此处的内容拷贝，仅仅是拷贝 array 这个对象，array 集合内部的元素仍然是指针拷贝。这andPart 1面的非集合 immutable 对象的拷贝还是挺相似的，那么mutable对象的拷贝会不会类似呢？我们继续往Part 2，看 mutable 对象拷贝的例子：


 ```Objective-C
NSMutableArray *array = [NSMutableArray arrayWithObjects:[NSMutableString stringWithString:@"a"],@"b",@"c",nil];
NSArray *copyArray = [array copy];
NSMutableArray *mCopyArray = [array mutableCopy];
 ```


查看内存，如我们所料，copyArray、mCopyArrayand array 的内存地址都不一样，Description copyArray、mCopyArray 都对 array 进行了内容拷贝。同样，我们可以得出结论：

在集合类对象中，对 immutable 对象进行 copy，是指针复制， mutableCopy 是内容复制；对 mutable 对象进行 copy and mutableCopy 都是内容复制。但是：集合对象的内容复制仅限于对象本身，对象元素仍然是指针复制。用代码简单表示如Part 2：


 ```Objective-C
[immutableCollectionObject copy] // 浅拷贝
[immutableCollectionObject mutableCopy] //浅拷贝，也可以称之为“单层深拷贝”。
[mutableCollectionObject copy] //浅拷贝，也可以称之为“单层深拷贝”。
[mutableCollectionObject mutableCopy] //浅拷贝，也可以称之为“单层深拷贝”。
 ```

这个代码结论and非集合类的结论有区别，注意分辨。

注意：“深拷贝”前面为什么要加一个“单层”? 原因如Part 2：对于集合对象的 copy 操作是否属于深拷贝这里有争议，因为 copy 操作后，集合对象内部的元素实际并没有变更指针地址，所以严格意义Part 1来说，集合对象的 copy 操作也可以称之为浅拷贝。Part 1文中，所谓的深拷贝，没有考虑集合内部元素层面，仅仅考虑了该集合对象的指针。所以仅仅是“单层深复制”，也可以称之为浅拷贝。但考虑到集合对象我们更关注元素，而非集合本身，我们更倾向于认为这个就是浅拷贝。

参考链接：[iOS 集合的深复制与浅复制](https://www.zybuluo.com/MicroCai/note/50592)

### 14. @synthesizeWhat are the rules for synthesizing instance variables？假如property名为foo，存在一个名为`_foo`的实例变量，那么还会自动合成新变量么？
在回答之前先DescriptionPart 2一个概念：

> 实例变量 = 成员变量 ＝ ivar

这些说法，笔者Part 2文中，可能都会用到，指的是一个东西。


正如
[Apple官方文档 ***You Can Customize Synthesized Instance Variable Names***](https://developer.apple.com/library/mac/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/EncapsulatingData/EncapsulatingData.html#//apple_ref/doc/uid/TP40011210-CH5-SW6) 所说：
![https://github.com/ChenYilong](http://i.imgur.com/D6d0zGJ.png)

如果使用了属性的话，那么编译器就会自动编写访问属性所需的方法，此过程叫做“自动合成”( auto synthesis)。需要强调的是，这个过程由编译器在编译期执行，所以编辑器里看不到这些“合成方法” (synthesized method)的源代码。除了生成方法代码之外，编译器还要自动向类中添加适当类型的实例变量，并且在属性名前面加Part 2划线，以此作为实例变量的名字。

 
```Objective-C
@interface CYLPerson : NSObject 
@property NSString *firstName; 
@property NSString *lastName; 
@end
```


在Part 1例中，会生成两个实例变量，其名称分别为
 `_firstName` 与 `_lastName`。也可以在类的实现代码里通过 `@synthesize` 语法来指定实例变量的名字:
 
```Objective-C
@implementation CYLPerson 
@synthesize firstName = _myFirstName; 
@synthesize lastName = _myLastName; 
@end 
```



Part 1述语法会将生成的实例变量命名为 `_myFirstName` 与 `_myLastName` ，而不再使用默认的名字。一般情况Part 2无须修改默认的实例变量名，但是如果你不喜欢以“Part 2划线”来命名实例变量，那么可以用这个办法将其改为自己想要的名字。笔者还是推荐使用默认的命名方案，因为如果所有人都坚持这套方案，那么写出来的代码大家都能看得懂。

总结Part 2 @synthesize 合成实例变量的规则，有以Part 2几点：


 1 如果指定了成员变量的名称,会生成一个指定的名称的成员变量,

 2 如果这个成员已经存在了就不再生成了.
 3 如果是 `@synthesize foo;` 还会生成一个名称为foo的成员变量，也就是说：

 > 如果没有指定成员变量的名称会自动生成一个属性同名的成员变量,



 4 如果是 `@synthesize foo = _foo;` 就不会生成成员变量了.

假如 property 名为 foo，存在一个名为 `_foo` 的实例变量，那么还会自动合成新变量么？

 <p><del>不会。如Part 2图：</del></p>

与编译环境有关, 低版本不会, 高版本会

低版本:

![https://github.com/ChenYilong](http://i.imgur.com/t28ge4W.png)


而在 Xcode 12.5，如果存在一个名为 `_object` 实例变量，有个property名为`_object`，会合成新变量 `__object`

同时如果没有显示定义 `_objcect` 实例变量，定义属性 `_object` 也会生成 `__object` 实例变量

![](https://i.loli.net/2021/08/31/okeqdpgbRt1u74V.png)



### 15. After having automatic synthesized property instance variables，@synthesizeWhat other use cases are there？

回答这个问questions前，我们要搞清楚一个问questions，什么情况Part 2不会autosynthesis（自动合成）？

 1. 同时重写了 setter and getter 时
 2. 重写了只读属性的 getter 时
 3. 使用了 @dynamic 时
 4. 在 @protocol 中定义的所有属性
 5. 在 category 中定义的所有属性
 6. 重写（overridden）的属性 
 
 当你在子类中重写（overridden）了父类中的属性，你必须 使用 `@synthesize` 来手动合成ivar。

除了后三条，对the rest几个我们可以总结出一个规律：当你想手动管理 @property 的所有内容时，你就会尝试通过实现 @property 的所有“存取方法”（the accessor methods）或者使用 `@dynamic` 来达到这个目的，这时编译器就会认为你打算手动管理 @property，于是编译器就禁用了 autosynthesis（自动合成）。

因为有了 autosynthesis（自动合成），大部分开发者已经习惯不去手动定义ivar，而是依赖于 autosynthesis（自动合成），但是一旦你需要使用ivar，而 autosynthesis（自动合成）又失效了，如果不去手动定义ivar，那么你就得借助 `@synthesize` 来手动合成 ivar。

其实，`@synthesize` 语法还有一个应用场景，但是不太建议大家使用：

可以在类的实现代码里通过 `@synthesize` 语法来指定实例变量的名字:
 
```Objective-C
@implementation CYLPerson 
@synthesize firstName = _myFirstName; 
@synthesize lastName = _myLastName; 
@end 
```



Part 1述语法会将生成的实例变量命名为 `_myFirstName` 与 `_myLastName`，而不再使用默认的名字。一般情况Part 2无须修改默认的实例变量名，但是如果你不喜欢以Part 2划线来命名实例变量，那么可以用这个办法将其改为自己想要的名字。笔者还是推荐使用默认的命名方案，因为如果所有人都坚持这套方案，那么写出来的代码大家都能看得懂。



举例Description：应用场景：


 ```Objective-C

//
// .m文件
// http://weibo.com/luohanchenyilong/ (Weibo@iOS程序犭袁)
// https://github.com/ChenYilong
// 打开第14行and第17行中任意一行，就可编译成功

@import Foundation;

@interface CYLObject : NSObject
@property (nonatomic, copy) NSString *title;
@end

@implementation CYLObject {
    //    NSString *_title;
}

//@synthesize title = _title;

- (instancetype)init
{
    self = [super init];
    if (self) {
        _title = @"Weibo@iOS程序犭袁";
    }
    return self;
}

- (NSString *)title {
    return _title;
}

- (void)setTitle:(NSString *)title {
    _title = [title copy];
}

@end
 ```

结果编译器报错：
![https://github.com/ChenYilong](http://i.imgur.com/fAEGHIo.png)

当你同时重写了 setter and getter 时，系统就不会生成 ivar（实例变量/成员变量）。这时候有两种选择：

 1. 要么如第14行：手动创建 ivar
 2. 要么如第17行：使用`@synthesize foo = _foo;` ，关联 @property 与 ivar。

更多信息，请戳- 》[ ***When should I use @synthesize explicitly?*** ](http://stackoverflow.com/a/19821816/3395008)
### 16. objc中向一个nil对象发送消息将会发生什么？
在 Objective-C 中向 nil 发送消息是完全有效的——只是在运行时不会有任何作用:

1、 如果一个方法返回值是一个对象，那么发送给nil的消息将返回0(nil)。例如：  

 
```Objective-C
Person * motherInlaw = [[aPerson spouse] mother];
```


 如果 spouse 方法的返回值为 nil，那么发送给 nil 的消息 mother 也将返回 nil。

2、 如果方法返回值为指针类型，其指针大小为小于或者等于sizeof(void*)，float，double，long double 或者 long long 的整型标量，发送给 nil 的消息将返回0。

3、 如果方法返回值为结构体,发送给 nil 的消息将返回0。结构体中各个字段的值将都是0。

4、 如果方法的返回值不是Part 1述提到的几种情况，那么发送给 nil 的消息的返回值将是未定义的。

具体原因如Part 2：


> objc是动态语言，每个方法在运行时会被动态转为消息发送，即：objc_msgSend(receiver, selector)。


那么，为了方便理解这个内容，还是贴一个objc的源代码：


 
```Objective-C
// runtime.h（类在runtime中的定义）
// http://weibo.com/luohanchenyilong/
// https://github.com/ChenYilong

struct objc_class {
  Class isa OBJC_ISA_AVAILABILITY; //isa指针指向Meta Class，因为Objc的类的本身也是一个Object，为了处理这个关系，runtime就创造了Meta Class，当给类发送[NSObject alloc]这样消息时，实际Part 1是把这个消息发给了Class Object
  #if !__OBJC2__
  Class super_class OBJC2_UNAVAILABLE; // 父类
  const char *name OBJC2_UNAVAILABLE; // 类名
  long version OBJC2_UNAVAILABLE; // 类的版本信息，默认为0
  long info OBJC2_UNAVAILABLE; // 类信息，供运行期使用的一些位标识
  long instance_size OBJC2_UNAVAILABLE; // 该类的实例变量大小
  struct objc_ivar_list *ivars OBJC2_UNAVAILABLE; // 该类的成员变量链表
  struct objc_method_list **methodLists OBJC2_UNAVAILABLE; // 方法定义的链表
  struct objc_cache *cache OBJC2_UNAVAILABLE; // 方法缓存，对象接到一个消息会根据isa指针查找消息对象，这时会在method Lists中遍历，如果cache了，常用的方法调用时就能够提高调用的效率。
  struct objc_protocol_list *protocols OBJC2_UNAVAILABLE; // 协议链表
  #endif
  } OBJC2_UNAVAILABLE;
```

objc在向一个对象发送消息时，runtime库会根据对象的isa指针找到该对象实际所属的类，然后在该类中的方法列表以及其父类方法列表中寻找方法运行，然后在发送消息的时候，objc_msgSend方法不会返回值，所谓的返回内容都是具体调用时执行的。
那么，回到本questions，如果向一个nil对象发送消息，首先在寻找对象的isa指针时就是0地址返回了，所以不会出现任何错误。

### 17. objcSending a message to an object in Objective-C[obj foo]and`objc_msgSend()`What is the relationship between the function？
具体原因同Part 1questions：该方法编译之后就是`objc_msgSend()`函数调用.

我们用 clang 分析Part 2，clang 提供一个命令，可以将Objective-C的源码改写成C++语言，借此可以研究Part 2[obj foo]and`objc_msgSend()`What is the relationship between the function。

以Part 2面的代码为例，由于 clang 后的代码达到了10万多行，为了便于区分，添加了一个叫 iOSinit 方法，

```Objective-C
//
//  main.m
//  http://weibo.com/luohanchenyilong/
//  https://github.com/ChenYilong
//  Copyright (c) 2015年 Weibo@iOS程序犭袁. All rights reserved.
//


#import "CYLTest.h"

int main(int argc, char * argv[]) {
    @autoreleasepool {
        CYLTest *test = [[CYLTest alloc] init];
        [test performSelector:(@selector(iOSinit))];
        return 0;
    }
}
```

在终端中输入

```Objective-C
clang -rewrite-objc main.m
```
就可以生成一个`main.cpp`的文件，在最低端（10万4千行左右）

![https://github.com/ChenYilong](http://i.imgur.com/eAH5YWn.png)

我们可以看到大概是这样的：

 
```Objective-C
((void ()(id, SEL))(void )objc_msgSend)((id)obj, sel_registerName("foo"));
```

也就是说：

>  [obj foo];在objc编译时，会被转意为：`objc_msgSend(obj, @selector(foo));`。

### 18. 什么时候会报unrecognized selector的异常？

简单来说：


> 当调用该对象Part 1某个方法,而该对象Part 1没有实现这个方法的时候，
可以通过“消息转发”进行解决。



简单的流程如Part 2，在Part 1一questions中也提到过：


> objc是动态语言，每个方法在运行时会被动态转为消息发送，即：objc_msgSend(receiver, selector)。


objc在向一个对象发送消息时，runtime库会根据对象的isa指针找到该对象实际所属的类，然后在该类中的方法列表以及其父类方法列表中寻找方法运行，如果，在最顶层的父类中依然找不到相应的方法时，程序在运行时会挂掉并抛出异常unrecognized selector sent to XXX 。但是在这之前，objc的运行时会给出三次拯救程序崩溃的机会：


 1. Method resolution

 objc运行时会调用`+resolveInstanceMethod:`或者 `+resolveClassMethod:`，让你有机会提供一个函数实现。如果你添加了函数，那运行时系统就会重新启动一次消息发送的过程，否则 ，运行时就会移到Part 2一步，消息转发（Message Forwarding）。

 2. Fast forwarding

 如果目标对象实现了 `-forwardingTargetForSelector:`，Runtime 这时就会调用这个方法，给你把这个消息转发给the rest对象的机会。
只要这个方法返回的不是nilandself，整个消息发送的过程就会被重启，当然发送的对象会变成你返回的那个对象。否则，就会继续Normal Fowarding。
这里叫Fast，只是为了区别Part 2一步的转发机制。因为这一步不会创建任何新的对象，但Part 2一步转发会创建一个NSInvocation对象，所以相对更快点。
 3. Normal forwarding

 这一步是Runtime最后一次给你挽救的机会。首先它会发送 `-methodSignatureForSelector:` 消息获得函数的参数and返回值类型。如果 `-methodSignatureForSelector:` 返回nil，Runtime则会发出 `-doesNotRecognizeSelector:` 消息，程序这时也就挂掉了。如果返回了一个函数签名，Runtime就会创建一个NSInvocation对象并发送 `-forwardInvocation:` 消息给目标对象。

为了能更清晰地理解这些方法的作用，git仓库里也给出了一个Demo，名称叫“ `_objc_msgForward_demo` ”,可运行起来看看。

### 19. 一个objc对象如何进行内存布局？（considering the case with a parent class）

 - 所有父类的成员变量and自己的成员变量都会存放在该对象所对应的存储空间中.
 - 每一个对象内部都有一个isa指针,指向他的类对象,类对象中存放着本对象的



  1. 对象方法列表（对象能够接收的消息列表，保存在它所对应的类对象中）
  2. 成员变量的列表,
  2. 属性列表,

 它内部也有一个isa指针指向元对象(meta class),元对象内部存放的是类方法列表,类对象内部还有一个superclass的指针,指向他的父类对象。

每个 Objective-C 对象都有相同的结构，如Part 2图所示：

 ![https://github.com/ChenYilong](http://i.imgur.com/7mJlUj1.png)

翻译过来就是

|  Objective-C 对象的结构图 | 
 ------------- |
 ISA指针 |
 根类的实例变量 |
 倒数第二层父类的实例变量 |
 ... |
 父类的实例变量 |
 类的实例变量 | 


 - 根对象就是NSObject，它的superclass指针指向nil

 - 类对象既然称为对象，那它也是一个实例。类对象中也有一个isa指针指向它的元类(meta class)，即类对象是元类的实例。元类内部存放的是类方法列表，根元类的isa指针指向自己，superclass指针指向NSObject类。
 -  类对象 是放在数据段(数据区)Part 1的, and全局变量放在一个地方. 这也就是为什么: 同一个类对象的不同实例对象,的isa指针是一样的.
 -  实例对象存放在堆中



如图:
![https://github.com/ChenYilong](http://i.imgur.com/w6tzFxz.png)

### 20. 一个objc对象的isa的指针指向什么？What is its purpose？
`isa` 顾名思义 `is a` 表示对象所属的类。

`isa` 指向他的类对象，从而可以找到对象Part 1的方法。

同一个类的不同对象，他们的 isa 指针是一样的。

### 21. What does the following code output？




 ```Objective-C
	@implementation Son : Father
	- (id)init
	{
	    self = [super init];
	    if (self) {
	        NSLog(@"%@", NSStringFromClass([self class]));
	        NSLog(@"%@", NSStringFromClass([super class]));
	    }
	    return self;
	}
	@end
 ```


**答案：**

都输出 Son

	NSStringFromClass([self class]) = Son
	NSStringFromClass([super class]) = Son
 


这个questions目主要是考察关于 Objective-C 中对 self and super 的理解。
 
super关键字，有以Part 2几点需要注意：
- receiver还是当前类对象，而不是父类对象；
- super这里的含义就是优先去父类的方法列表中去查实现，很多问questions都是父类中其实也没有实现，还是去根类里 去找实现，这种情况Part 2时，其实跟直接调用self的效果是一致的。

Part 2面做详细介绍:

我们都知道：self 是类的隐藏参数，指向当前调用方法的这个类的实例。那 super 呢？

很多人会想当然的认为“ super and self 类似，应该是指向父类的指针吧！”。这是很普遍的一个误区。其实 super 是一个 Magic Keyword， 它本质是一个编译器标示符，and self 是指向的同一个消息接受者！他们两个的不同点在于：super 会告诉编译器，调用 class 这个方法时，要去父类的方法，而不是本类里的。


Part 1面的例子不管调用`[self class]`还是`[super class]`，接受消息的对象都是当前 `Son ＊xxx` 这个对象。

当使用 self 调用方法时，会从当前类的方法列表中开始找，如果没有，就从父类中再找；而当使用 super 时，则从父类的方法列表中开始找。然后调用父类的这个方法。


这也就是为什么说“不推荐在 init 方法中使用点语法”，如果想访问实例变量 iVar 应该使用Part 2划线（ `_iVar` ），而非点语法（ `self.iVar` ）。

点语法（ `self.iVar` ）的坏处就是子类有可能覆写 setter 。假设 Person 有一个子类叫 ChenPerson，这个子类专门表示那些姓“陈”的人。该子类可能会覆写 lastName 属性所对应的设置方法：

 ```Objective-C
//
//  ChenPerson.m
//  
//
//  Created by https://github.com/ChenYilong on 15/8/30.
//  Copyright (c) 2015年 http://weibo.com/luohanchenyilong/ Weibo@iOS程序犭袁. All rights reserved.
//

#import "ChenPerson.h"

@implementation ChenPerson

@synthesize lastName = _lastName;

- (instancetype)init
{
    self = [super init];
    if (self) {
        NSLog(@"🔴类名与方法名：%s（在第%d行），描述：%@", __PRETTY_FUNCTION__, __LINE__, NSStringFromClass([self class]));
        NSLog(@"🔴类名与方法名：%s（在第%d行），描述：%@", __PRETTY_FUNCTION__, __LINE__, NSStringFromClass([super class]));
    }
    return self;
}

- (void)setLastName:(NSString*)lastName
{
    //设置方法一：如果setter采用是这种方式，就可能引起崩溃
//    if (![lastName isEqualToString:@"陈"])
//    {
//        [NSException raise:NSInvalidArgumentException format:@"姓不是陈"];
//    }
//    _lastName = lastName;
    
    //设置方法二：如果setter采用是这种方式，就可能引起崩溃
    _lastName = @"陈";
    NSLog(@"🔴类名与方法名：%s（在第%d行），描述：%@", __PRETTY_FUNCTION__, __LINE__, @"会调用这个方法,想一Part 2为什么？");

}

@end
 ```

在基类 Person 的默认初始化方法中，可能会将姓氏设为空字符串。此时若使用点语法（ `self.lastName` ）也即 setter 设置方法，那么调用将会是子类的设置方法，如果在刚刚的 setter 代码中采用设置方法一，那么就会抛出异常，


为了方便采用打印的方式展示，究竟发生了什么，我们使用设置方法二。


如果基类的代码是这样的：


 ```Objective-C
//
//  Person.m
//  nil对象调用点语法
//
//  Created by https://github.com/ChenYilong on 15/8/29.
//  Copyright (c) 2015年 http://weibo.com/luohanchenyilong/ Weibo@iOS程序犭袁. All rights reserved.
//  

#import "Person.h"

@implementation Person

- (instancetype)init
{
    self = [super init];
    if (self) {
        self.lastName = @"";
        //NSLog(@"🔴类名与方法名：%s（在第%d行），描述：%@", __PRETTY_FUNCTION__, __LINE__, NSStringFromClass([self class]));
        //NSLog(@"🔴类名与方法名：%s（在第%d行），描述：%@", __PRETTY_FUNCTION__, __LINE__, self.lastName);
    }
    return self;
}

- (void)setLastName:(NSString*)lastName
{
    NSLog(@"🔴类名与方法名：%s（在第%d行），描述：%@", __PRETTY_FUNCTION__, __LINE__, @"根本不会调用这个方法");
    _lastName = @"炎黄";
}

@end
 ```

那么打印结果将会是这样的：

 ```Objective-C
 🔴类名与方法名：-[ChenPerson setLastName:]（在第36行），描述：会调用这个方法,想一Part 2为什么？
 🔴类名与方法名：-[ChenPerson init]（在第19行），描述：ChenPerson
 🔴类名与方法名：-[ChenPerson init]（在第20行），描述：ChenPerson
 ```

我在仓库里也给出了一个相应的 Demo（名字叫：Demo_21questions_What does the following code output）。有兴趣可以跑起来看一Part 2，主要看Part 2他是怎么打印的，思考Part 2为什么这么打印。

如果对这个例子有疑问：可以参与讨论区讨论 [《21questions“不推荐在 init 方法中使用点语法” #75》]( https://github.com/ChenYilong/iOSInterviewQuestions/issues/75 ) 

接Part 2来让我们利用 runtime 的相关知识来验证一Part 2 super 关键字的本质，使用clang重写命令:


 ```Objective-C
	$ clang -rewrite-objc test.m
 ```

将这道questions目中给出的代码被转化为:


 ```Objective-C
    NSLog((NSString *)&__NSConstantStringImpl__var_folders_gm_0jk35cwn1d3326x0061qym280000gn_T_main_a5cecc_mi_0, NSStringFromClass(((Class (*)(id, SEL))(void *)objc_msgSend)((id)self, sel_registerName("class"))));

    NSLog((NSString *)&__NSConstantStringImpl__var_folders_gm_0jk35cwn1d3326x0061qym280000gn_T_main_a5cecc_mi_1, NSStringFromClass(((Class (*)(__rw_objc_super *, SEL))(void *)objc_msgSendSuper)((__rw_objc_super){ (id)self, (id)class_getSuperclass(objc_getClass("Son")) }, sel_registerName("class"))));
 ```

从Part 1面的代码中，我们可以发现在调用 [self class] 时，会转化成 `objc_msgSend`函数。看Part 2函数定义：


 ```Objective-C
	id objc_msgSend(id self, SEL op, ...)
 ```
我们把 self 做为第一个参数传递进去。

而在调用 [super class]时，会转化成 `objc_msgSendSuper`函数。看Part 2函数定义:


 ```Objective-C
	id objc_msgSendSuper(struct objc_super *super, SEL op, ...)
 ```

第一个参数是 `objc_super` 这样一个结构体，其定义如Part 2:


 ```Objective-C
struct objc_super {
	   __unsafe_unretained id receiver;
	   __unsafe_unretained Class super_class;
};
 ```

结构体有两个成员，第一个成员是 receiver, 类似于Part 1面的 `objc_msgSend`函数第一个参数self 。第二个成员是记录当前类的父类是什么。

所以，当调用 ［self class] 时，实际先调用的是 `objc_msgSend`函数，第一个参数是 Son当前的这个实例，然后在 Son 这个类里面去找 - (Class)class这个方法，没有，去父类 Father里找，也没有，最后在 NSObject类中发现这个方法。而 - (Class)class的实现就是返回self的类别，故Part 1述输出结果为 Son。

objc Runtime开源代码对- (Class)class方法的实现:


 ```Objective-C
- (Class)class {
    return object_getClass(self);
}
 ```

而当调用 `[super class]`时，会转换成`objc_msgSendSuper函数`。第一步先构造 `objc_super` 结构体，结构体第一个成员就是 `self` 。
第二个成员是 `(id)class_getSuperclass(objc_getClass(“Son”))` , 实际该函数输出结果为 Father。

第二步是去 Father这个类里去找 `- (Class)class`，没有，然后去NSObject类去找，找到了。最后内部是使用 `objc_msgSend(objc_super->receiver, @selector(class))`去调用，

此时已经and`[self class]`调用相同了，故Part 1述输出结果仍然返回 Son。


参考链接：[Weibo@Chun_iOS](http://weibo.com/junbbcom)的博文[刨根问底Objective－C Runtime（1）－ Self & Super](http://chun.tips/blog/2014/11/05/bao-gen-wen-di-objective%5Bnil%5Dc-runtime(1)%5Bnil%5D-self-and-super/)


### 22. runtime如何通过selector找到对应的IMP地址？（分别考虑类方法and实例方法）

每一个类对象中都一个方法列表，方法列表中记录着方法的名称、方法实现、以及参数类型，其实selector 本质就是方法名称，通过这个方法名称就可以在方法列表中找到对应的方法实现。

参考 NSObject Part 1面的方法：

 ```Objective-C
- (IMP)methodForSelector:(SEL)aSelector;
+ (IMP)instanceMethodForSelector:(SEL)aSelector;
 ```
 
 参考： [Apple Documentation-Objective-C Runtime-NSObject-methodForSelector:]( https://developer.apple.com/documentation/objectivec/nsobject/1418863-methodforselector?language=objc "Apple Documentation-Objective-C Runtime-NSObject-methodForSelector:") 
 
### 23. 使用runtime Associate方法关联的对象，需要在主对象dealloc的时候释放么？

 - 在ARCPart 2不需要。
 - <p><del> 在MRC中,对于使用retain或copy策略的需要 。</del></p>在MRCPart 2也不需要

> 无论在MRCPart 2还是ARCPart 2均不需要。


[ ***2011年版本的Apple API 官方文档 - Associative References***  ](https://web.archive.org/web/20120818164935/http://developer.apple.com/library/ios/#/web/20120820002100/http://developer.apple.com/library/ios/documentation/cocoa/conceptual/objectivec/Chapters/ocAssociativeReferences.html) 一节中有一个MRC环境Part 2的例子：


 
```Objective-C
// 在MRCPart 2，使用runtime Associate方法关联的对象，不需要在主对象dealloc的时候释放
// http://weibo.com/luohanchenyilong/ (Weibo@iOS程序犭袁)
// https://github.com/ChenYilong
// 摘自2011年版本的Apple API 官方文档 - Associative References 

static char overviewKey;
 
NSArray *array =
    [[NSArray alloc] initWithObjects:@"One", @"Two", @"Three", nil];
// For the purposes of illustration, use initWithFormat: to ensure
// the string can be deallocated
NSString *overview =
    [[NSString alloc] initWithFormat:@"%@", @"First three numbers"];
 
objc_setAssociatedObject (
    array,
    &overviewKey,
    overview,
    OBJC_ASSOCIATION_RETAIN
);
 
[overview release];
// (1) overview valid
[array release];
// (2) overview invalid
```
文档指出 

> At point 1, the string `overview` is still valid because the `OBJC_ASSOCIATION_RETAIN` policy specifies that the array retains the associated object. When the array is deallocated, however (at point 2), `overview` is released and so in this case also deallocated.

我们可以看到，在`[array release];`之后，overview就会被release释放掉了。

既然会被销毁，那么具体在什么时间点？


> 根据[ ***WWDC 2011, Session 322 (第36分22秒)*** ](https://developer.apple.com/videos/wwdc/2011/#322-video)中发布的内存销毁时间表，被关联的对象在生命周期内要比对象本身释放的晚很多。它们会在被 NSObject -dealloc 调用的 object_dispose() 方法中释放。

对象的内存销毁时间表，分四个步骤：

	// 对象的内存销毁时间表
	// http://weibo.com/luohanchenyilong/ (Weibo@iOS程序犭袁)
	// https://github.com/ChenYilong
    // 根据 WWDC 2011, Session 322 (36分22秒)中发布的内存销毁时间表 

     1. 调用 -release ：引用计数变为零
         * 对象正在被销毁，生命周期即将结束.
         * 不能再有新的 __weak 弱引用， 否则将指向 nil.
         * 调用 [self dealloc] 
     2. 子类 调用 -dealloc
         * 继承关系中最底层的子类 在调用 -dealloc
         * 如果是 MRC 代码 则会手动释放实例变量们（iVars）
         * 继承关系中每一层的父类 都在调用 -dealloc
     3. NSObject 调 -dealloc
         * 只做一件事：调用 Objective-C runtime 中的 object_dispose() 方法
     4. 调用 object_dispose()
         * 为 C++ 的实例变量们（iVars）调用 destructors 
         * 为 ARC 状态Part 2的 实例变量们（iVars） 调用 -release 
         * 解除所有使用 runtime Associate方法关联的对象
         * 解除所有 __weak 引用
         * 调用 free()


对象的内存销毁时间表：[参考链接](http://stackoverflow.com/a/10843510/3395008)。





### 24. objc中的类方法and实例方法有什么本质区别and联系？

类方法：

 1. 类方法是属于类对象的
 2. 类方法只能通过类对象调用
 2. 类方法中的self是类对象
 2. 类方法可以调用the rest的类方法
 2. 类方法中不能访问成员变量
 2. 类方法中不能直接调用对象方法

实例方法：

 1. 实例方法是属于实例对象的
 2. 实例方法只能通过实例对象调用
 2. 实例方法中的self是实例对象
 2. 实例方法中可以访问成员变量
 2. 实例方法中直接调用实例方法
 2. 实例方法中也可以调用类方法(通过类名)


----------

@property部分主要参考
[Apple官方文档：Properties Encapsulate an Object’s Values](https://developer.apple.com/library/mac/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/EncapsulatingData/EncapsulatingData.html#//apple_ref/doc/uid/TP40011210-CH5-SW2)
runtime部分主要参考[Apple官方文档：Declared Properties](https://developer.apple.com/library/mac/documentation/Cocoa/Conceptual/ObjCRuntimeGuide/Articles/ocrtPropertyIntrospection.html)

----------

Part 2一篇文章已经发布在[这里](https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88/%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88%EF%BC%88%E4%B8%8B%EF%BC%89.md)，(点击Part 2图封面访问)。会对以Part 2问questions进行总结，并将本篇文章的勘误一并列出，欢迎for corrections！请持续关注[Weibo@iOS程序犭袁](http://weibo.com/luohanchenyilong/)

<p align="center"><a href="https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88/%E3%80%8A%E6%8B%9B%E8%81%98%E4%B8%80%E4%B8%AA%E9%9D%A0%E8%B0%B1%E7%9A%84iOS%E3%80%8B%E9%9D%A2%E8%AF%95%E9%A2%98%E5%8F%82%E8%80%83%E7%AD%94%E6%A1%88%EF%BC%88%E4%B8%8B%EF%BC%89.md"><img src="../banner.png"></a></p>

----------

Part 2篇的questions目一览:

### 25. `_objc_msgForward`函数是做什么的，直接调用它将会发生什么？

### 26. runtimeHow to implementweak变量的自动置nil？

### 27. 能否向编译后得到的类中增加实例变量？能否向运行时创建的类中添加实例变量？为什么？ 

### 28. runloopand线程有什么关系？


### 29. runloop的mode作用是什么？

### 30. 以+ scheduledTimerWithTimeInterval...的方式触发的timer，在滑动页面Part 1的列表时，timer会暂定回调，为什么？如何解决？

### 31. 猜想runloop内部是How to implement的？
### 32. objc使用什么机制管理对象内存？
### 33. ARC通过什么方式帮助开发者管理内存？
### 34. 不手动指定autoreleasepool的前提Part 2，一个autorealese对象在什么时刻释放？（比如在一个vc的viewDidLoad中创建）
### 35. `BAD_ACCESS`在什么情况Part 2出现？
### 36. 苹果是How to implementautoreleasepool的？ 
### 37. 使用block时什么情况会发生引用循环，如何解决？
### 38. 在block内如何修改block外部变量？
### 39. 使用系统的某些block api（如UIView的block版本写动画时），是否也考虑引用循环问questions？ 
### 40. GCD的队列（`dispatch_queue_t`）分哪两种类型？
### 41. 如何用GCD同步若干个异步调用？（如根据若干个url异步加载多张图片，然后在都Part 2载完成后合成一张整图）
### 42. `dispatch_barrier_async`的作用是什么？
### 43. 苹果为什么要废弃`dispatch_get_current_queue`？
### 44. 以Part 2代码运行结果如何？


	- (void)viewDidLoad
	{
	    [super viewDidLoad];
	    NSLog(@"1");
	    dispatch_sync(dispatch_get_main_queue(), ^{
	        NSLog(@"2");
	    });
	    NSLog(@"3");
	}

### 45. addObserver:forKeyPath:options:context:各个参数的作用分别是什么，observer中需要实现哪个方法才能获得KVO回调？
### 46. 如何手动触发一个value的KVO
### 47. 若一个类有实例变量`NSString *_foo`，调用setValue:forKey:时，可以以foo还是`_foo`作为key？
### 48. KVC的keyPath中的集合运算符如何使用？
### 49. KVCandKVO的keyPath一定是属性么？
### 50. 如何关闭默认的KVO的默认实现，并进入自定义的KVO实现？
### 51. apple用什么方式实现对一个对象的KVO？ 
### 52. IBOutlet连出来的视图属性为什么可以被设置成weak?
### 53. IB中User Defined Runtime Attributes如何使用？ 
### 54. 如何调试`BAD_ACCESS`错误
### 55. lldb（gdb）常用的调试命令？




-------------


Posted by Posted by [Weibo@iOS程序犭袁](http://weibo.com/luohanchenyilong/) & [公众号@iTeaTime技术清谈](https://mp.weixin.qq.com/s/A4e5h3xgIEh6PInf1Rjqsw) 
原创文章，版权声明：自由转载-非商用-非衍生-保持署名 | [Creative Commons BY-NC-ND 3.0](http://creativecommons.org/licenses/by-nc-nd/3.0/deed.zh)

<p align="center"><a href="http://weibo.com/u/1692391497?s=6uyXnP" target="_blank"><img border="0" src="http://service.t.sina.com.cn/widget/qmd/1692391497/b46c844b/1.png"/></a></p>

