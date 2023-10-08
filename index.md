---
layout: default
---

this is a new project about human-blance. （基于多模态信号的人体平衡能力的评估（展示方案初版））（图片插入已解决）（注意符号统一，排版问题）（测试action错误问题。已解决，问题初步估计是script/validate-html中的results.errors.each { |err| puts err }err后的.to_s字符串转换冗余，不确定err是否关联其他方法，但应该不影响，暂留存测试）
[Link to another page](./another-page.html).

There should be whitespace between paragraphs.
（项目展示排版：摘要；引言；综述（具体方案）；->数据集；实验；结论与展望；参考文献）
There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# 摘要（这部分从关键词给出来的扩写润色一下就行）（注意，使用#及其不同数量可以控制字体大小）
失衡跌倒造成的伤害是导致老年人致残或死亡的主要原因之一。本项目利用多模态信号采集技术和机器学习算法，研究人体平衡能力的评估方法，
为日常健康管理和老年人康复提供科学依据。首先，采集包括声音、图像、加速度等多模态信号。
其次，融合现有人体平衡能力评估方法，构建并优化评估模型，实现对人体平衡能力的准确评估。最后，探索不同人群中平衡能力的差异，为健康管理和康复提供有针对性的方案。

## 引言（从背景写到意义）
全球人口预期寿命的增加与生育率的下降导致全球面临人口老龄化的危机，联合国出版的《2020年世界人口老龄化-老年人的生活安排》中预估2050年的老年人口将达到15亿以上，而根据WHO报道全世界每年估计有64.6万人因跌倒没有得到及时救治而死亡，60岁以上老年人死亡率最高，所占比例最大。跌倒会造成一些致命伤害，比如脑部出血等，及时发现人的跌倒状态并及时报警至关重要。因此，老人的跌倒检测是社会医疗监护的重要组成部分。在我国，跌倒是65岁以上老年人伤害死亡的首位原因，平均每10人就有3~4人发生过跌倒。其会引发髋关节、脊椎骨、手腕部等部位骨折。其中髋关节骨折最为严重，老年人的这个部位一旦骨折，一年后的生存率只有50%左右。且跌倒后引发的多种并发症也是更是导致老年人死亡的主要威胁。经相关机构预测到2022年左右，中国超过65岁的人口将占总人口的14%；并且到2030年，中国将会进入老年人口占比25.26%的深度老龄化社会。在这快速老龄化的社会，老年人的健康问题日益凸显，失能、半失能老人数量急剧增加，因跌倒产生的各种健康医疗问题将会愈发显著。因此，当今社会对人体平衡能力进行全面评估是十分必要的，并应提供科学有效的筛查方法和手段，以帮助医疗机构早期发现和诊断与平衡障碍有关的疾病，从而加强疾病预防能力，提高治疗效果和预后，并减轻病人的社会和经济负担。
随着时代进步，人们也不断开发新的技术来更有效的实现有关人体体态等信息的分析，手势识别、步态识别、动作分析、情感识别等众多行为分析技术已逐步应用到日常生活中，随之需要的各种传感器更是不断迭代升级，现如今已经能够通过多种技术来采集人体体态信息并加以分析。目前主要应用的技术主要以下几种：

（1） 计算机视觉：通过摄像头采集人体行为动作图像序列, 利用计算机视觉计算方法, 提取和识别人体动作序列, 如手势、步态等.该方法识别准确, 是目前使用最为广泛的一种方法.但是该方法计算量巨大, 容易受到光照条件以及障碍物的影响.同时摄像头存在监测死角, 只能实现视距下特定范围内的感知。

（2） 可佩戴设备：通过将专用传感器, 如加速度计等安装到人体上, 采集相关的动作信息, 从而实现人体行为感知.例如, 加速度计被安装在人体身上来实现摔倒检测;声学传感器被用来区分吃饭和咳嗽等行为;智能传感器被用来监测驾驶行为.专用传感器可以实现细粒度的行为感知, 但是造价昂贵, 安装和携带不便, 难以广泛应用。
由此可见各种技术目前对于相关信息的采集已经较为成熟，而随着传感器技术、智能系统和信息技术的不断发展，可穿戴设备具备了小型化、高灵敏度和低成本等特征，并广泛地应用于人们的日常生活中，尤其是老年人的日常监护场景中。可穿戴传感器设备能够实时地检测老年的活动状态，并在老人出现跌倒等意外情况时发出报警信息。因此，利用可穿戴传感器设备对老年人进行日常监护，并通过上述技术收集人体平衡状态信息进行综合分析提前预警的一整套流程正是当今社会所需的一种医疗预防预警方案。
因此，综合当今社会老龄化逐渐严重的发展趋势和随之而来的有关老人平衡能力降低导致的各种意外与疾病问题日益突出，设计一套通过从多方面收集人体信息进而筛查人体平衡能力的方法与标准，对于提前排除隐患，帮助医疗机构早期发现和诊断与平衡障碍有关的疾病，加强疾病预防能力，提高治疗效果和预后，减轻病人的社会和经济负担，有非常重大的意义。
> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.（这句可以写作文）

## 综述（使用方法，技术）

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```
关于代码部分，如果需要参照上例或下例：
```js
    cout<<“Hello World!”<<endl;
    return 0；
```

注意：（“```js” ,“```”） 是代码块展示格式，web不会展示出来

```
文本块展示：使用一组```来展示文本内容，注意```的位置来确定文本框的起始位置（上述代码块在第一个```后加上高级语言代码，比如js，且保证```为单独一行后来表示文本块为代码块标注形式）

此外，一些合适的排版可能会让模板自动识别为文本，如果想直接展示可以适当调整文本。
```

#### 部分1

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

#### 部分2

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

#### 部分3（表格这部分说一下，html应该大家都不是很熟练，所以直接使用markdown语法来“画”一个表格出来，如下：（注意，md的表格写法只有这一种展示形式，这意味着如果想要自定义需要使用html修改css文件，之后解决）
| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

例：
| 8 | 1 | 6 |
|:--|:--|:--|
| 3 | 5 | 7 |
| 4 | 9 | 2 |

### There's a horizontal rule below this.

* * *

### 数据集:（把老师说的那几个数据集先整理一下编辑到页面上吧）

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### 实验:（这部分先不编辑）

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### 结论与展望:（项目预期成果与发展前景）

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image（这个是链接，打开是github网站中git创建分支的介绍界面，不用管它只是个演示）

![Branching](https://guides.github.com/activities/hello-world/branching.png)

```
图片插入演示：
              （1.上传图片到assets库里（assets/css/，应该是这个文件夹）（找add file按键，之后会建立一个文件夹的）

                2.在index.md或者html里（我没找到html版的，这个应该没有），输入如上引用：![图片描述](/assets/css/xxx.jpg(或者png，看具体后缀)
              
                 3.保存改动，等待github自动更新网页）
               
               （或者：使用一个URL来引用非本地图片，实例如上：![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)）```

```
本地实例如下：

![blue archive](/assets/css/icon.png)



### 参考文献：（数据集+实验+方法）

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
