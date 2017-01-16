####基本语法
1. 1 Flex布局 弹性布局(Flex Box) Webkit内核的浏览器，必须加上 -webkit前缀,设置为flex布局后，子元素的float,clear,
vertical-align属性将失效。
`.box{display:flex} .box{display:inline-flex}  .box{display:-webkit-flex}`

1. 2 基本概念
    采用flex布局元素，称为flex容器，所有子元素自动成为容器成员，称为flex项目(flex item)
    水平主轴 main axis    垂直交叉  cross axis
1. 3 容器的属性
    flex-direction:row|row-reverse|column|column-reverse   决定项目的排列方向
                   默认值，主轴为水平方向，起点在左|起点在右端|主轴为垂直方向，起点在上沿
    flex-wrap:nowrap|wrap|wrap-reverse    项目一条轴线排不下，如何换行       
               默认值，不换行|换行，第一行在上方|换行，第一行在下方
    flex-flow:  flex-direction和flex-wrap的简写，默认值 row wrap
     
    **justify-cotent** flex-start|flex-end|center|space-between|space-around 定义了项目在主轴上的对齐方式
                           默认值，左对齐|右对齐|居中|两端对齐，项目之间的间隔相等||每个项目两侧的间隔相等，所以项目之间
                           的间隔比项目与边框的间隔大一倍。
     
    **align-items** flex-start|flex-end|center|baseline|stretch  
                         交叉轴起点对齐|交叉轴终点对齐|交叉轴中点对齐|项目的第一行文字的基线对齐|默认值，如果项目未设置
                         高度或者设为auto，将占满整个容器的高度
    align-content:flex-start|flex-end|center|space-between|space-around|stretch     定义了多根轴线的对齐方式，如果项目只
                        有一根轴线，该属性不起作用。
                        
1. 4 项目的属性
     order 定义项目的排列顺序，数值越小，排列越靠前，默认值0
     flex-grow定义项目的放大比例，默认值为0，即如果存在剩余空间，也不放大
     flex-shrink定义项目的所辖比例，默认值1，即如果空间不足，项目将缩小，属性值为0，空间不足，不缩小
     flex-basis 项目占据的主轴空间（width height） 默认值auto，项目本来大小
     flex：flex-grow,flex-shrink,flex-basis的简写，默认值为 0 1 auto
            auto (1 1 auto) none( 0 0 auto)
     align-self  允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性