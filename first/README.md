思路：
1：每一个星星代表一个实例Round_item
   实例拥有私有属性代表canvas画圆的参数，给每个实例掉一个key值
   arc(x,y,r,startAngle,endAngle,anticlockwise)
   anticlockwise 是否逆时针
2：每一个实例拥有一个canvas的绘制方法
   cadnvas绘制的基本思路
   首先，你需要创建路径起始点。
   然后你使用画图命令去画出路径。
   之后你把路径封闭。
   一旦路径生成，你就能通过描边或填充路径区域来渲染图形
   ctx.beginPath();
   ctx.moveTo(25,25);
   ctx.closePath();
   只有设置shadowColor属性值为不透明,才被绘制

3:申明变量 
  round  星星实体的集合
  initRoundPopulation 星星的个数

4:canvas的宽高用js或者内联css设置

5：先让星星布满画布

6:让星星动起来
  星星实体继承move方法
  调用  requestAnimationFrame  构造 animate()函数
  调用animate也可以用递归，也可以用类似定时的方法
