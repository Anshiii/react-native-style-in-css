# ReactNativeStyleInCss

由于 react-native 的部分样式如 Padding，Border，Margin 在定义时较为繁琐，且不支持 CSS 中的简式声明(如 padding: 12px 8px ;)，为了延续 CSS 写法的一些优点，故产生了本方法。

## 优势

使用 react-native 定义的形式声明样式。

``` javascript
let styleNative = {
  marginTop: 10,
  marginRight: 18,
  marginBottom: 12,
  marginLeft: 10,

  borderBottomColor: 'red',
  borderBottomWidth: 1,
  borderStyle: 'solid',

  paddingVertical: 12,
  paddingHorizontal: 22
};
```

使用 ReactNativeStyleInCss 声明样式。

``` javascript
let style = reactNativeStyleInCss({
  margin: [10, 18, 12, 10], //以 css 上右下左 的声明顺序
  border: [1, 'solid', 'red'], //以 css 的声明顺序
  padding: [12, 22]
});
```

## 安装

``` javascript
npm install react-native-style-in-css
```

## 使用

``` javascript
import reactNativeStyleInCss from 'react-native-style-in-css'

let styles = reactNativeStyleInCss({
  margin: [10, 18, 12, 10],
  fontSize: 12,
});
```