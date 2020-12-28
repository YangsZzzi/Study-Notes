## 1. 安装

在 IDEA的 setting 的 Plugins 的 Marketplace 中搜索 leetcode，找到该插件，安装完成之后重启即可。

![img](https://img-blog.csdnimg.cn/20200308102947255.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTAxODA4MTU=,size_16,color_FFFFFF,t_70)

## 2. 参数配置

2.1 第一次使用前，需要进行一些基本的配置。在Setting的Tools中可以找到安装好的leetode plugin：

- URL选项：可以选择是国内还是国外的语言。
- LoginName：注册的用户名
- Password：密码
- TemFilePath：项目存放的路径，可以自己设定。
- CodeFileName：代码文件名字，正常是让你显示每个题目的英文名字。所以我的配置是：

```java
$!velocityTool.camelCaseName(${question.titleSlug})
```

- CodeTemplate：每个题目Code初始化模板。

```java
${question.content}
package com.cute.leetcode.editor.cn;
public class $!velocityTool.camelCaseName(${question.titleSlug}) {
    public static void main(String[] args) {
        Solution solution = new $!velocityTool.camelCaseName(${question.titleSlug})().new Solution();
    }
    ${question.code}
}
```

PS：在 CustomConfig则是代码模版说明。

![img](https://img-blog.csdnimg.cn/20200514092909606.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTAxODA4MTU=,size_16,color_FFFFFF,t_70)

## 3.开启刷题之路

配置完成之后，在IEDA的右下角有一个Leetcode的菜单，打开会显示同步你网站上的刷题菜单。

- 在上方会有很多按钮，包括刷新题目、配置等。
- 第一个 Problems 为所有的题目，题目标题按难易程度分别用不同的颜色进行标识，绿色表示容易，黄色表示中等，红色表示困难。
- 双击题目会将题目按先前配置的信息加载到本地路径中，并生成相应的模板。
- 做完题目之后，也可以直接提交，并有反馈结果。

![img](https://img-blog.csdnimg.cn/20200308105453205.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTAxODA4MTU=,size_16,color_FFFFFF,t_70)

![img](https://img-blog.csdnimg.cn/20200308105233933.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTAxODA4MTU=,size_16,color_FFFFFF,t_70)