---
category: Components
type: Data Display
chinese: 走马灯
english: Carousel
---


一组轮播的区域。

### 规则
- 所展示信息属于同一个层级；同时，鼓励用户进行内容的浏览和探索。
- 一般情况下，只进行横向滚动。
- 默认自动轮播，当用户轻触时该区域时停止；允许用户向前、向后滚动 Carousel。


## API ( 适用平台：WEB、React-Native )

| 参数             | 说明                                         | 类型     | 默认值                          |
|------------------|----------------------------------------------|----------|---------------------------------|
| selectedIndex |  手动设置当前显示的索引  |  number  |  0  |
| dots | 是否显示面板指示点 | Boolean   | true |
| vertical | 垂直显示(web 为内容，rn 为 pagination) | Boolean   | false |
| autoplay | 是否自动切换 | Boolean   | false |
| infinite | 是否循环播放 | Boolean   | false |
| afterChange      | 切换面板的回调                              | function(current)  | 无
| easing (`web only`) | 动画效果 | String   | linear |
| beforeChange  (`web only`)     | 切换面板的回调                              | function(from, to) | 无
| onScrollBeginDrag (`rn only`) | 见 react-native scrollView onScrollBeginDrag | function | 无 |
| bounces (`rn only`) | 见 react-native scrollView bounces       |   Boolean              | true |

更多参数可参考：https://github.com/FormidableLabs/nuka-carousel
