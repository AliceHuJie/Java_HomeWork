# 1. Why should you have minimum scope for variables?

通过变量作用域最小化，尽可能的将变量引用点集中在一起，从而能够对变量施加控制。将局部变量的作用域最小化，可以增强代码的可读性和可维护性，并降低出错的可能性。

# 2. Why should you understand performance of String Concatenation?
字符串拼接（“+”，concat,StringBuilder,StringBuffer）实际都是生成了新的String对象；  
在大量字符串拼接时，效率按快慢排序是：  
StringBulider > StringBuffer > String.concat > “+” 。

# 4. When is it recommended to prefer Unchecked Exceptions?
继承自RuntimeException的类或者error的子类，为unchecked exceptions。  
其他都属于checkedException。  

适合的使用场景：  
受检异常：期望调用者从异常中恢复，catch中处理异常或将它传播出去；  
非受检异常：不可恢复的情景。


# 5. When do you use a Marker Interface?
不包含任何方法的接口为标记接口，例如Serializable。其作用是给接口的实现类贴上一个标签 ，然后我们可以根据这个实现类是否持有这个标签来对实现类进行一些相关操作。  

因此当需要标记哪些实现类可以执行某操作时，可以让其去实现一个标记接口。


# 6. Why are ENUMS important for Readable Code?
枚举类型使代码更具可读性,理解清晰,可以检查 非法数值，同时易于维护。
# 7. Why should you minimize mutability?
可变性最小化可以尽可能的让自己管理自己，提高模块独立性，尽可能减少代码耦合导致的扩展、测试、修改、优化的困难。
不可变类比可变类更加易于设计,实现和使用,不容易出错,且线程安全。 
# 8. What is functional programming?
函数式编程是指可以将函数作为一个参数传递给指定方法。
# 9. Why should you prefer Builder Pattern to build complex objects?
建造者模式可以将部件和其组装过程分开，一步一步创建一个复杂的对象。
# 10. Why should you avoid floats for Calculations?
浮点运算会丢失精度，计算不准确，解决方法是使用BigDecimal类。
# 11. Why should you build the riskiest high priority features first?