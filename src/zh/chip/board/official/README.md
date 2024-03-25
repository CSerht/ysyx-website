---
title: "官方板卡"
---

## 板卡简介
本页面为星空单板计算机的 **开发文档** 首页。星空(StarrySky)系列 [单板计算机(Single Board Computer, SBC)](https://en.wikipedia.org/wiki/Single-board_computer) 是2023年3月份 [一生一芯项目组](https://ysyx.oscc.cc/) 在吸收前期多款测试板卡的设计经验后，专门规划设计的一款基于 **一生一芯流片SoC** 的官方板卡，用于评估和展示一生一芯SoC的丰富外设应用。项目组独立完成了星空系列单板计算机的硬件设计，生产管理，教程编写和包装视觉设计。短期目标希望能够依托每年2~3次一生一芯SoC的流片持续打磨星空系列板卡的软硬件系统，为开源社区提供一款稳定，易于开发的软件测试平台，长期目标是希望围绕星空系列化板卡构建轻量化的软硬件生态系统，并探索其在科研流片领域的丰富应用场景。

<!-- 一张图片，可以是规划图 -->

## 视觉概念
### 板卡设计
为了保证星空系列开发板整体视觉上的一致性，项目组规范板卡设计上统一使用**黑色阻焊油墨+白色字符丝印+沉金焊盘**的工艺。并约束板卡机械尺寸为**110X84mm**。考虑到功能性和冗余度，星空系列开发板会**一直搭载FPGA核心板(SoM)**，一方面是为了通过ChipLink接口扩展外设功能，为SoC板卡提供最基本的访存能力，同时为下一代一生一芯SoC的FPGA原型验证提供支持。

### 板卡名字
为了满足本系列开发板的对外宣传需要，项目组精心选择了本系列板卡的正式名字。为了能够更有效率地筛选出符合条件的名字，项目组从下面几个方面对板卡的正式名字进行选择：
- 名字需要遵循国家法律和道德的约束。
- 名字不会造成歧义，并且不会联想到特定个人或群体。
- 符合板卡的自身定位和特征，并且不与市场上现有公开售卖的板卡名字重复。
- 中英文名字能相互对应，简短，并且易懂，易于传播，方便对外宣传。
- 名字需要具有一定的故事性和可形象化性。

项目组依照上述要求对板卡名字进行了多次头脑风暴，得到的符合条件的候选板卡名字列表：

<style>
.name_table_center
{
  width: auto;
  display: table;
  margin-left: auto;
  margin-right: auto;
}
</style>

<div class="name_table_center">

| 中文 | 英文 | 寓意 |
| :-: | :-: | :- |
| 流星/彗星/天穹/星辰/星宿/星河/星云/星空 | FlashStar/Galaxy/Nebula/StarrySky | 流星的寓意代表着命运的转变。流星的出现往往伴随着大气层内的摩擦和摩擦产生的电离效应，所以人们常常将流星看做是一种崭新的开始。对于那些遭受挫折、陷入低谷的人来说，流星意味着一种新的机会，一个全新的开始，带来新的生命、新的希望和机遇。因此，流星被视为一个令人激动的象征，为许多追求成功的人打开了新的大门。其次，流星的寓意也带有一定的警示。因为流星在短暂燃烧的过程中释放出的能量非常强大，类似于一场短暂的爆炸，这也说明了人在自己人生的某个时间点上，可能会经历重重困难和不幸的打击。因此，流星的象征意义也提醒着我们，一定要珍惜眼前的一切，以积极的心态来面对环境的变化和一些突发的难题。尤其是在事业上，要将此种能量转换为自己前进的动力，提高自己的竞争力和抵御力 |
| 算器/珠算 | Abacus | 算盘大不盈尺却凝结着中华先人高超的数学智慧，是我国古代商业活动中最重要的计算工具，它制作简单、操作方便，可以解决各种复杂的运算，甚至可以开多平方。国内外都有类似的工具 |
| 仙人掌 | Cactus | 相信在很多人心中，仙人掌象征的是坚强。在荒无人烟中的沙漠随处可见，是沙漠中难得一见的绿色。它像我们展现了生命的顽强，不仅可以生长在沙漠中，开出来的花朵还能在风吹日晒中绽放，所以，仙人掌代表了坚强的涵义 |
| 向日葵 | SunFlower/Helianthus | 向日葵的花序总是随着太阳转动，一生向着光明生长，给人一种十分励志的感觉，可以象征着信念、光辉、高傲、沉默的爱等含义 |
| 矩阵 | Matrix | Matrix是一套复杂的模拟系统程序，它是由具有人工智能的机器建立的，模拟了人类以前的世界，用以控制人类。在Matrix中出现的人物，可以看作是具有人类意识特征的程序 |
| 奇异果 | Kivi Pi | 猕猴桃简介因猕猴喜食，故名猕猴桃，也有说法是因为果皮覆毛，貌似猕猴而得名，是一种品质鲜嫩，营养丰富，风味鲜美的水果。类似树莓派的那种命名 |

</div>

经过多轮讨论，并分别从命名含义、功效性、情感性等多个方面进行筛选，项目组最终确定选用 **星空** 作为板卡的正式名字。选用 **星空** 不仅仅是因为其很好地符合上面提出的所有要求，更是因为 **星空** 向我们展示了一个广阔，深邃而神秘的未知空间，并忠实地映射着宇宙间生命的涌动，生根，发芽，开花，结果的全过程。隐喻着科学探索的神秘和无穷尽，需要我们一点一点地发现它的美。另外星空还是灵动和恬静两种意象的辩证统一，在星空中点缀的些许繁星，如同镶嵌在星月中的颗颗钻石，在黯淡中散发着微光，展示出一幅 **“星月满空琼草青”** 的画卷，这是静的一面；而划过天际的流星，宛如一条条轻盈的丝带，纤纤起舞着，钻进无人的夜空，这是动的一面。在星空下，人们可以肆意畅想未来，可以尽情释放内心的压抑。星空完美展示了科幻和浪漫感，给人带来了希望。

### 包装设计

在设计包装整体视觉效果时，项目组充分考虑到了功能性和美术性。首先确定设计风格是现代简约geek风，使用白色打底以清晰展示底部众多支持单位的logo，正面设计有主标题+副标题，图案和众多支持单位的logo，为主功能面。底面则为板卡的DXF线稿图，在设计过程中参考了苹果和大疆白底色产品包装的风格：

![星空开发板盒型刀版设计](/res//images/board/package/package-intro.png)

包装正面上使用 **星空+分割线+StarrySky+阿拉伯数字** 来展示主标题，使用 **“搭载学生自制CPU的RV64单板计算机”** 作为副标题。包装正面左上角为一生一芯项目的logo和标语，右上角为一生一芯项目官网地址二维码。底部水平放置所有支持单位的logo。包装主标题右侧设计有以星空背景为主体的几何图案，几何图案选取星空中常见天文现象作为设计元素：
- 星宿
- 卫星
- 星轨和流星雨

由以上设计元素组成的几何图案的含义如下：
- 使用点表征过孔(狭义)和星星(广义)，使用线类比芯片和PCB中的过孔(狭义)和行星轨迹(广义)，展示一种“点->线”的连接(动静变化)。
- 图案中设计有北斗七星(星宿，群体，静态)和恒星+卫星双星系统(卫星，群体，静态)。并通过线联系在一起，宛若流星(个体，动态)。而众多流星汇聚一起构成流星雨(群体，动态)，而流星雨恰好是夜晚星空中最浪漫而美丽的景象。

![星空开发板盒型3D渲染](/res//images/board/package/package-3d.png)

另外在包装设计上还解决了印刷过程中的丢色，模糊等问题，并确定了制造工艺，其具体制造参数如下：
- 盒型：后开带锁扣扣底
- 内尺寸：135X37X105 mm
- 外尺寸：136X38X107 mm
- 制造尺寸：135.6X37.6X106.1 mm
- 材质：350g白卡纸，厚度0.5mm，亚膜工艺
- 印刷：数码喷墨打印

## 版本约定
目前星空开发板的硬件版本命名方式采用：**星空+V主版本号.副版本号** 这种格式。其中**主版本号**的变更表示所搭载的一生一芯SoC存在**代次间**的变化，比如SoC架构的演进或者是制程工艺的提升等。而**副版本号**的变更则表示板卡硬件外设的修改。
<!-- 开发进度图 -->

## 板卡型号
下面展示了所有板卡的 **开发文档** 页面，可以点击下面卡片中的 ***详细信息*** 跳转到特定板卡的页面。
<TheBoards />

## 用户许可
本文档用户许可在撰写时参考了互联网上众多内容文档的许可条款， **希望能够在保证文档内容版权完整的前提下，为用户提供尽可能开放的阅读和引用体验**。请用户仔细阅读并透彻理解本声明，一旦用户在阅读和其他平台以任何形式发布本文档内容时，均视为已经阅读**以下全部条款**并确认全部无条件接受。

### 公开展示
本页面的所有文档内容都是公开，可以被免费阅览的，因此没有选项支持让特定人无法看到文档中的任何一个页面。另外本文档支持被搜寻引擎收录，因此有些用户贡献的内容可能会出现在一些检索结果中。

### 内容修改
**一生一芯项目组拥有对文档内容的维护权**，用于对文档进行合并、关闭和修改，而不需要就文档内容的改变单独通知所有用户。用户可能需要自行维护引用内容改变所造成的相应传播媒介内容的修改。

### 内容授权
所有文档**原创内容**采用**受限制的自由内容版权发布**，这表示它的内容可以被任何人在本网站或外部引用、复制、加工和传播，但是本文档原创内容**不能未经过版权许可就直接应用到商业领域**，并且用户需要声明**一生一芯项目组拥有对文档原创内容的所有权和引用出处**，包括但不限于文字，图片，视频，代码等多种形式。虽然本站点也会有一些可以合理使用的公开新闻资讯，但是本文档主要放置受限制自由版权的内容，并以传播知识内容为主，因此不希望个人和组织在未声明所有权和出处的情况下使用本文档内容。本文档在引用有些外来的资源时会依照附加的、不同于本页所描述的授权方式**进行显示版权声明**。使用内容的用户有义务了解并遵守本文档和本文档可能引用的外部资源的授权方式。当使用以Creative Commons Attribution-Share Alike License（创作共用-姓名标示-相同方式分享）来引用本文档内容时，你必须以前面 ***标注来源*** 段落中的介绍的方式之一来标注来源。需要注意的是版权法所保护的只是一种想法的创造性表达方式（creative expression of ideas），而不是想法或信息本身。因此，阅读一条百科全书的条目或其他著作后使用自己的语言表达出来，然后再提交给本文档的过程是完全合法的。请注意，将本文档的内容转载至其他网站时，本文档不保证该网站合理使用的资源（文字，图片，视频，代码等）合乎当地法律。

对于文档站以外的内容（如Email，兴趣小组，论坛等）如果未有明确说明，**不能假设也以这样的授权方式发布**。



### 免责说明
- 用户需要承诺秉着合法、合理的原则使用本文档内容，不利用本文档进行任何违法、侵害他人合法利益等恶意的行为，亦不将本文档引用于任何违反我国法律法规的网站平台。
- 任何单位或个人因下载使用本文档而产生的任何意外、疏忽、合约毁坏、诽谤、版权或知识产权侵犯及其造成的损失 (包括但不限于直接、间接、附带或衍生的损失等)，本团队不承担任何法律责任。
- 用户明确并同意本声明条款列举的全部内容，对使用本文档可能存在的风险和相关后果将完全由用户自行承担，本团队不承担任何法律责任。
- 任何单位或个人在阅读本免责声明后，应在 [内容授权](#内容授权) 所允许的范围内进行合法的发布、传播和使用本文档等行为，若违反本免责声明条款或违反法律法规所造成的法律责任(包括但不限于民事赔偿和刑事责任），由违约者自行承担。
- 任何单位或个人不得在未经本团队书面授权的情况下对本文档本身申请相关的知识产权。
- 如果本声明的任何部分被认为无效或不可执行，则该部分将被解释为反映本团队的初衷，其余部分仍具有完全效力。不可执行的部分声明，并不构成我们放弃执行该声明的权利。
- 本团队有权随时对本声明条款及附件内容进行单方面的变更，并以消息推送、网页公告等方式予以公布，公布后立即自动生效，无需另行单独通知；若您在本声明内容公告变更后继续使用的，表示您已充分阅读、理解并接受修改后的声明内容。

#### **一生一芯项目组对以上所有条款拥有最终解释权**