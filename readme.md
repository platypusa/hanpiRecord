# 踩坑记录

1. 问题：vue 中输入框防抖，methods 中在函数内加入 debounce 防抖失效：
   onInput() {
   debounce(fn)
   }
   解决：在函数体内使用防抖，vue 在每次调用时会初始化函数导致防抖失效，应该给方法赋值防抖函数
   onInput: debounce(fn)
