# java-4
Java第四次实验
#### 一、实验目的
##### 掌握Java中抽象类和抽象方法的定义； 
##### 掌握Java中接口的定义，熟练掌握接口的定义形式以及接口的实现方法
##### 了解异常的使用方法，并在程序中根据输入情况做异常处理
#### 二、实验内容
##### 某学校为了给学生提供勤工俭学机会，也减轻授课教师的部分压力，准许博士研究生参与课程的助教工作。此时，该博士研究生有双重身份：学生和助教教师。
##### 设计两个管理接口：学生管理接口和教师管理接口。学生接口必须包括缴纳学费、查学费的方法；教师接口包括发放薪水和查询薪水的方法。
##### 设计博士研究生类，实现上述的两个接口，该博士研究生应具有姓名、性别、年龄、每学期学费、每月薪水等属性。
##### 编写测试类，并实例化至少两名博士研究生，统计他们的年收入和学费。根据两者之差，算出每名博士研究生的年应纳税金额。
#### 三、实验要求
##### 在博士研究生类中实现各个接口定义的抽象方法;
##### 对年学费和年收入进行统计，用收入减去学费，求得纳税额；
##### 国家最新纳税标准（系数），属于某一时期的特定固定值，与实例化对象没有关系，考虑如何用static  final修饰定义。
##### 实例化研究生类时，可采用运行时通过main方法的参数args一次性赋值，也可采用Scanner类实现运行时交互式输入。
##### 根据输入情况，要在程序中做异常处理。
#### 五、实验步骤
##### 1.先用interface来定义student和teacher这两个接口接口
##### 2.然后在Graduate里面用implements来实现这两个接口
##### 3.在Graduate里面把学费，收入，纳税的算法写出来
##### 4.用输出函数把姓名，性别，年龄，月收入，学费写出来
##### 5.用for循环来把这些变量循环，一直到有两个研究生后退出程序
##### 6.加入try-catch函数做异常处理，不能输入与收入无关的东西
#### 六、核心代码
```
public class Test {
    public static void main(String[] args) {
        Graduate graduate = new Graduate();
        graduate.setName("CRZ");//设置姓名
        graduate.setmoney(6000, 1500);//设置每学期的费用,月工资
        System.out.println("CRZ学费为："+graduate.getxuefei());
        System.out.println("CRZ年收入为："+graduate.getsalary()); 
        System.out.println("CRZ纳税额："+((graduate.getsalary()*0.25)-1005));
        graduate.setmoney(5000, 2000);//设置每学期的费用,月工资
        System.out.println("SYW学费为："+graduate.getxuefei());
        System.out.println("SYW年收入为："+graduate.getsalary()); 
        System.out.println("SYW纳税额："+((graduate.getsalary()*0.25)-1005));	
        }
 }
 ```
#### 七、实验结果
![实验截图](https://github.com/penny0203/java-4/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202020-11-08%20232850.png)
#### 八、实验感想
##### 对于这次实验我对try-catch异常处理有了初步了解
##### 知道了interface定义接口，implement实现接口
