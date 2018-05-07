* 将html文件和css样式组合到一起的方法有三种
  * 内联样式 <p style="color:red">
  * style标签，
  * 外部样式表

* 选择器
* 类选择器 .apple 
* id选择器 #apple
* combinator
  * div>p  
    * 选择div的子元素p 
    （注意子元素和后代元素的区别)
  * div + p 
    * 选中div后面紧挨着的兄弟元素p
  * div ~ p 
    * 选中div后面所有的兄弟元素p
* 属性选择器 css selector
  * \[attr="foo"]{} 属性值为foo
  * \[attr^="foo"]{} 属性值开头为foo
  * \[attr$="foo"]{} 属性值结尾为foo 
  * \[attr\*="foo"]{} 属性值中出现foo
  * \[attr]{} 属性存在
  * \[attr~="foo"]{} 有一个属性值为foo
  * \[attr\|="foo"]{}
     属性值为foo或者属性值以foo-开头

* 伪类选择器 
  * 结构伪类
    * first-child
    * nth-child(),括号中可以出现表达式
    * first-type
    * nth-of-type
  * 动态伪类
    * hypertext伪类lv
    * 用户行为伪类 fha
  * UI state 伪类(用于那些能跟用户交互的元素如表单)
    * enable;disabled;checked;default;valid;required;optional等
    * 其实:focus可以被当作一个UI-state 伪类
  * :target
    * 当网址后面有#id时候，这个id元素就是对应target
  * :lang
    * especially for language specifity
  * :not
    * :not(),括号中只能填入一个选择器，不能填多个选择器的组合，例如 p a不行，但是p可以,pseudo-element也不能包在括号中

* 伪元素选择器 pseudo-element
  * 只能出现在选择器的末尾，只能应用到块级元素
  * ::first-letter,选择第一个字母，如果它的前面或后面有其他符号，则也会被选中
  * ::first-line
  * ::before,::after, 例如h2::before{content: "]]";color:silver;},在一个元素前面或者后面插入一些内容，同时设置这些内容的样式
 

* 选择器的优先级
  比较方法
  1. sorting by weight and origin
  2. sorting by specificity(0,0,0,0)
  3. sorting by order
  
  * 优先级的定义，四个数，四位的无穷进制数
  * (0,4,6,15)
  * id选择器，第二位加1
  * 类、伪类、属性选择器，第三位加1
  * 标签选择器，第四位加1
  * 通配符(\*)的优先级为(0,0,0,0)
  * 继承的优先级最低，比(0,0,0,0)都低
  * 内联样式/行内样式，第一位为1，<h1 style="color:red">
  * !important 例如h1{color:red !important ;}单独拿出来对比，有important的选择器>没有important的

* value and unit 值与单位
  * value
    * normal keywords
      例如{text-decoration:underline;}
    * global keywords
      * inherit
      * innitial
      * unset
    * strings
      开始和结束的quote要对应
    * urls
      * absolute
      * relative 相对当前页面所在文件
    * images
      * url of an image
      * image-set a set of images
    


  * 百分比一般是用在长度(相对于父级元素的长度)
  * px 
  * ppi 例如96ppi，意思是96pixels per inch
  * em 相对值，相对于当前元素font-size的大小
  * rem root element's em,相对于html元素的字号
  * vw viewport width视口宽度的%1
  * calc() 括号里面运算符的左右两边必须加空格
  * 角度
    * degree 角度,45deg
    * radian 弧度，2rad
    * turn 1turn=360deg
  * 时间
    * s  ms









