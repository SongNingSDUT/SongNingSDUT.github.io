---
presentation:
  enableSpeakerNotes: true
  fragments: true
  mouseWheel: true
  transition: 'default' # none/fade/slide/convex/concave/zoom
  # === 可选的主题 ===
  # "beige.css"
  # "black.css"
  # "blood.css"
  # "league.css"
  # "moon.css"
  # "night.css"
  # "serif.css"
  # "simple.css"
  # "sky.css"
  # "solarized.css"
  # "white.css"
  # "none.css"  
  theme: beige.css
---

<!-- slide -->

---
## 第一讲 绪论
---
<br>
<small>宋宁·山东理工大学·数学系 </small>

<!-- slide vertical=true data-notes="各位未来的数学老师们，各位即将战斗在数学教育第一线的战友们，大家上午好！ 从今以后，在我这个课上，我对你们的称呼就不是“小张同学”、“小王同学”、“小李同学”……而是“小张老师”、“小王老师”、“小李老师”．我希望你们以一个未来数学教师的立场来上我这个课，同时以一个未来数学老师的责任感和使命感来要求自己．尤其是我们同学当中的师范生们，你们将来大部分会成为数学老师．其实我也是师范生出身，我是山东师范大学数学与应用数学专业2004级的本科师范生．在收到录取通知书以后，我当时一直有一个疑问：" -->
 
究竟什么叫==师范==呢？ 

<!-- slide vertical=true data-notes="我的疑问后来在入学的当天得到了解答．当时我们大一新生在山东师大的北校区，在济南水屯村附近．当时那里比较荒凉，所以我在公交车上很远就看到北校区的大楼上有八个大字" -->

> “学高为师，身正为范”

<!-- slide vertical=true data-notes="据说这是陶行知的话，从此以后，“师范”的这个解释牢牢地刻在了我的心中．首先说后面四个字，浓缩一下，这里说的是“师德”．这些年来，我们从各种媒体见到了太多的有违教师职业道德的事情，其中有大学老师、中学老师、甚至小学老师，尤其近些年还出现幼儿园老师的问题．我觉得我们作为老师应该多一份使命感和责任感，应该对得起人家恭恭敬敬地叫你的一声“老师”．当然，这并不是我们这个课程所需要讨论的内容．我们还是重点来看一下前面这四个字．这四个字向我们提出了一个深刻的问题：" -->

### <p align="left"> 思考</p>

  + 一个合格的数学教师应该具备什么样的知识结构？
  + 哈哈哈

<!-- slide vertical=true data-notes="过去我们说，要给学生一滴水，你需要一桶水；在现在这个知识爆炸的时代，也许一桶水还不够，可能你需要一个水库．比如，山东省很多地方招聘高中数学老师，必须要有硕士学位．甚至在北京上海等地广泛出现一个现象：大量名校的硕士博士竞聘高中数学教师的职位．" -->

> 这是唯学历论吗？

<!-- slide vertical=true data-notes="请大家来看一下，这是2019年上半年教师资格考试（高中数学）中的科目三《数学学科知识与教学能力》的试卷真题：" -->

sssss

$$
\frac{4}{3}x^2=hhhh
$$



<!-- slide vertical=true data-notes="请大家来看一下，这是2019年上半年教师资格考试（高中数学）中的科目三《数学学科知识与教学能力》的试卷真题：" -->

+ 从这份试卷中我们可以看出：
  + 第2、3、4、5、6、10、11、14题都是大学数学专业课的内容．
  + 你们念大一的时候，我就教过你们．当时就有同学说：

<!-- slide vertical=true -->

> “我只是想毕业当个中学数学老师，中学数学用不着数学分析、高等代数这些东西”

<!-- slide vertical=true -->

ssss

<!-- slide vertical=true -->

ssss

ssss

<!-- slide -->

@import "4.6-1.gif"

<!-- slide -->

> <a href="https://songningsdut.github.io/html/lecture/mathTeacher/gaozhong/2019-1-e.html">2019年（上）教师资格考试（高中）《数学学科知识与教学能力》</a>

<!-- slide -->

Multiple Presentation themes are supported, you can change it easily from the extension settings.  

* vscode  
@import "https://i.loli.net/2017/07/12/5965b5c7783fb.png" {width: 60%}
* atom  
@import "http://i.imgur.com/lwaogVZ.png" {width: 60%}

check [Reveal.js Speaker Notes](https://github.com/hakimel/reveal.js#speaker-notes) section for more information.


<!-- slide -->
By default, all slides are aligned horizontally, but you can also create vertical slides by adding `vertical=true`.
For example:
```html
<!-- slide vertical=true -->
```

<!-- slide  vertical=true -->
You just discovered a vertical slide!

<!-- slide data-transition="zoom"  -->
You can set `id` and `class` for your slide like this:
```html
<!-- slide id="my-id" class="my-class1 my-class2" -->
```

<!-- slide -->
You can set slide background very easily.
For example:
```html
<!-- slide data-background-color="#ff0000" -->
```

<!-- slide data-background-color="#ffebcf"-->
Of course you can do more about slide **background**.
* `data-background-image`
URL of the image to show. GIFs restart when the slide opens.
* `data-background-size`
See [background-size](https://developer.mozilla.org/docs/Web/CSS/background-size) on MDN.
* `data-background-position`
See [background-position](https://developer.mozilla.org/docs/Web/CSS/background-position) on MDN.
* `data-background-repeat`
See [background-repeat](https://developer.mozilla.org/docs/Web/CSS/background-repeat) on MDN.

<!-- slide -->
You can also set **video background** and **iframe background**.
* `data-background-video`
A single video source, or a comma separated list of video sources.
* `data-background-video-loop`
Flags if the video should play repeatedly.
* `data-background-video-muted`
Flags if the audio should be muted.
* `data-background-iframe`
Embeds a web page as a background.

<!-- slide -->  
Fragment is supported.  
```
- Item 1 <!-- .element: class="fragment" data-fragment-index="2" -->
- Item 2 <!-- .element: class="fragment" data-fragment-index="1" -->
```

- See [this doc](https://github.com/hakimel/reveal.js#fragments) for different fragment animations <!-- .element: class="fragment" -->
- Item 1 <!-- .element: class="fragment" data-fragment-index="2" -->
- Item 2 <!-- .element: class="fragment" data-fragment-index="1" -->

<!-- slide -->
For example, the markdown snippet below will generate slide like...
```html
<!-- slide data-background-image="https://i.loli.net/2017/07/12/5965b7edd3a2a.jpeg" data-transition="zoom" -->
<p style="color: #fff;">国漫大法好！</p>
<p style="color: #fff;">国漫大法好！</p>
<p style="color: #fff;">国漫大法好！</p>
```

<!-- slide data-background-image="https://i.loli.net/2017/07/12/5965b7edd3a2a.jpeg"
data-transition="zoom"
-->
<p style="color: #fff;">国漫大法好！</p>
<p style="color: #fff;">国漫大法好！</p>
<p style="color: #fff;">国漫大法好！</p>

<!-- slide -->
It is also very easy to customize presentation css.
Run command:
`Markdown Preview Enhanced: Customize Css`
then edit:
```less
.markdown-preview.markdown-preview {
  .slides {
    // This will modify all slides.
  }
  .slides > section:nth-child(1) {
    // This will modify `the first slide`.
    background-color: blue;
  }
}
```

<!-- slide -->
You can check your presentation in browser by
right clicking at the preview, then choose

`Open in Browser`

<!-- slide -->
**Markdown Preview Enhanced** can also generate beautiful **HTML** or **PDF** files for your presentation.

<!-- slide -->
#### Star this project if you like it ;)
* Github Repository can be found [here](https://github.com/shd101wyy/markdown-preview-enhanced)
* Feel free to post issues and request new features [here](https://github.com/shd101wyy/markdown-preview-enhanced/issues)
* Source code of this presentation can be found [here](https://github.com/shd101wyy/markdown-preview-enhanced/blob/master/docs/presentation-intro.md), [raw](https://raw.githubusercontent.com/shd101wyy/markdown-preview-enhanced/master/docs/presentation-intro.md)


<!-- slide data-background-image="http://ooo.0o0.ooo/2016/07/18/578c66da6a5a3.jpg" -->

