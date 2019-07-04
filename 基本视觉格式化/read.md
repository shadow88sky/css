# 基本视觉格式化

## 水平属性
* margin-left  
* border-left  
* padding-left  
* width  
* padding-right  
* border-right  
* margin-right

## 垂直属性
* margin-top
* border-top
* padding-top
* height
* padding-bottom
* border-bottom
* margin-bottom

## 规则
* 正常流中的块级元素框的水平部分总和就等于父元素的width
* 正常流中的块级元素框的垂直部分总和就等于父元素的height
* 水平七属性中，只有margin-left,width,margin-right才能设置width为auto

## 匿名文本  
  匿名文本（anonymous text）是指所有未包含在行内元素中的字符串。因此，在标记`<p> I'm <em>so</em> happy!</p>`中，序列“I'm”和 “happy!”都是匿名文本。注意，空格也是匿名文本的一部分，因为空格与其他字符一样都是正常的字符。 
  
## em框  
  em框在字体中定义，也称为字符框（character box）。实际的字形可能比其em框更高或更矮，见第5章的讨论。在CSS中，font-size的值确定了各个em框的高度。 
  
## 内容区  
  在非替换元素中，内容区可能有两种，CSS2.1规范允许用户代理选择其中任意一种。内容区可以是元素中各字符的em框串在一起构成的框，也可以是由元素中字符字形描述的框。本书中，为简单起见采用了前一种定义，即em框定义。在替换元素中，内容区就是元素的固有高度再加上可能有的外边距。边框或内边距。

## 行间距  
  行间距（leading）是font-size值和line-height值之差。这个差实际上要分为两半，分别应用到内容区的顶部和底部。毫不奇怪，为内容区增加的这两部分分别称为半间距（half-leading）。行间距只应用于非替换元素。 
  
## 行内框  
  这个框通过向内容区增加行间距来描述。对于非替换元素，元素行内框的高度刚好等于line-height的值。对于替换元素，元素行内框的高度则恰好等于内容区的高度，因为行间距不应用到替换元素。

## 行框  
  这是包含该行中出现的行内框的最高点和最低点的最小框。换句话说，行框的上边界要位于最高行内框的上边界，而行框的底边要放在最低行内框的下边界。