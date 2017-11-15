# 移动端高清方案干货

 1  cssreset作用
      <script src="build/flexible_css.debug.js"></script>
 
 2  核心方法
      <script src="build/flexible.debug.js"></script>
 
 3  改变字体大小的js
      <script src="js/jquery-3.2.1.min.js"></script>
      <script src="js/dprchangefont.js"></script>
 
 4  我使用使用stylus编译并且压缩为相应的css文件
      stylus --compress css/
 
 5  假设设计稿是 750
 
 6  用stylus  将px转换为rem
      px2rem(px)
        return unit(px / 75, 'rem')
      调用  @import '/px2rem.styl'
        width  px2rem(200)  注意这个200是设计稿的原始值
 
 7  字体大小设置
      字体统一用px单位
      有字体大小的元素统一加相应的class（dprchangefont）方便js处理
      初始字号写 data-drp = 1时候的大小 (安卓机)
        设计稿字体是24px  那就写12px
      当data-drp != 1时候 (苹果机)
        交给相应的dprchangefont.js处理

        