1. 手势对html端的支持，在pc端，手势所返回的事件属性跟手机端（至少android端）不一致，android端，ontouchmove,onpammove均具有文档上说的changedTouches属性，而在pc端，没有该属性（虽然有别的属性可以等价计算，但是这样就不能三端同步了）。为了调用手势检测滑动位置和距离，需要给pc端和android端写两套代码。
2. debug的热加载不能自动加载子组件的修改，只能加载顶层组件的修改，如果子组件和父组件同时发生更改，不会报错，但是子组件就消失了。
3. 文件的命名不能包含关键字，比如：list.we,cell.we等
4. 网页版的weexplayground不能滑动
