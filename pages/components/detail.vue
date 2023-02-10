<template>
  <div class="box">
        <div class="max-w-6xl mx-auto mt-6 sm:px-6 lg:px-8">
          <!-- 标题 -->
          <h1 class="artical-title">{{upinfo.articleTitle}}</h1>
           <!-- 作者信息 -->    
          <el-row>
            <!-- up主头像 -->
              <div class="grid-content bg-purple-dark">
              <div class="demo-basic--circle">
                <div class="block"><el-avatar :size="50" :src="upinfo.circleUrl">
                  </el-avatar></div>
              </div>
            </div>
            <!-- up主相关信息 -->
              <div class="grid-content bg-purple-dark">
              <div class="author-info-name">
                <span>{{upinfo.upName}}</span>
                <span title="创作等级"><img :src="upinfo.level" alt=""></span>
              </div>
              <div class="date-info">
                <span title="更新时间">{{upinfo.upDate}}</span>
                <span>.&nbsp;&nbsp;阅读 {{upinfo.readed}}</span>
              </div>
  
            </div>
          </el-row> 
          <!-- 文章详情 -->
          <!-- 前言 -->
          <div>
            <img :src="preface.prefaceImg" alt=""  style="width:100%;overflow: hidden;">
            <p>{{preface.text1}}</p>
            <blockquote>{{preface.text2}}</blockquote>
            <a href="#">{{preface.text3}}</a>
          </div>
          <!-- 标题循环 -->
          <div class="detail">
            <div :key="yiji.name" v-for="yiji in title">
                <h1>{{ yiji.yijititle }}</h1>
                <div :key="erji.name" v-for="erji in yiji.erjititles">
                    <h2>{{erji.erjititle1}}</h2>
                    <div :key="sanji.name" v-for="sanji in erji.sanjititles">
                        <h3>{{sanji.sanjititle1}}</h3>
                        <p>{{sanji.text1}}</p>
                        <p>{{sanji.text2}}</p>
                        <p>{{sanji.text3}}</p>
                        <p>{{sanji.text4}}</p>
                        <img :src="sanji.img1" alt="" style="width:100%;overflow: hidden;">

                        <h3>{{sanji.sanjititle2}}</h3>
                        <p>{{sanji.text5}}</p>
                        <p>{{sanji.text6}}</p>

                        <h3>{{sanji.sanjititle3}}</h3>
                        <p>{{sanji.text7}}</p>

                        <h3>{{sanji.sanjititle4}}</h3>
                        <p>{{sanji.text8}}</p>

                        <h3>{{sanji.sanjititle5}}</h3>
                        <p>{{sanji.text9}}</p>
                        <img :src="sanji.img2" alt="" style="width:100%;overflow: hidden;">
                        <ul :key="item" v-for="item in sanji.cheque">
                          <li>{{item}}</li>
                        </ul>
                        <p>{{sanji.text11}}</p>

                        <h3>{{sanji.sanjititle6}}</h3>
                        <p>{{sanji.text12}}</p>
                        <p>{{sanji.text13}}</p>
                        <p>{{sanji.text14}}</p>

                        <h3>{{sanji.sanjititle7}}</h3>
                        <p>{{sanji.text15}}</p>

                        <h3>{{sanji.sanjititle8}}</h3>
                        <p>{{sanji.text16}}</p>

                    </div>    

                    <h2>{{erji.erjititle2 }}</h2>
                    <div :key="erjititle2s.name"   v-for="erjititle2s in erji.erjititle2s">
                        <blockquote>{{erjititle2s.text1}}</blockquote>
                        <p>{{erjititle2s.text2}}</p>
                        <blockquote>{{erjititle2s.text3}}</blockquote>
                        <p>{{erjititle2s.text4}}</p>
                        <p>{{erjititle2s.text5}}</p>
                        <p>{{erjititle2s.text6}}</p>
                        <blockquote>{{erjititle2s.text7}}</blockquote>
                        <p>{{erjititle2s.text8}}</p>
                        <p>{{erjititle2s.text9}}</p>
                        <p>{{erjititle2s.text10}}</p>
                        <blockquote>{{erjititle2s.text11}}</blockquote>
                        <p>{{erjititle2s.text12}}</p>
                        <p>{{erjititle2s.text13}}</p>
                        <p>{{erjititle2s.text14}}</p>
                        <p>{{erjititle2s.text15}}</p>
                    </div>
                    <h2>{{erji.erjititle3}}</h2>
                    <div :key="erjititle3s.name"   v-for="erjititle3s in erji.erjititle3s">
                      <blockquote>{{erjititle3s.text1}}</blockquote>
                      <p>{{erjititle3s.text2}}</p>
                      <ol>
                        <li>{{erjititle3s.erjititle3slist[0]}}</li>
                        <li>{{erjititle3s.erjititle3slist[1]}}</li>
                        <li>{{erjititle3s.erjititle3slist[2]}}</li>
                        <li>{{erjititle3s.erjititle3slist[3]}}</li>
                        <li>{{erjititle3s.erjititle3slist[4]}}</li>
                        <li>{{erjititle3s.erjititle3slist[5]}}</li>
                        <li>{{erjititle3s.erjititle3slist[6]}}</li>
                      </ol>
                      <p>{{erjititle3s.text3}}</p>
                    </div>
                </div>
                
            </div>
</div>
  </div>
</div>
  </template>
  <style>
  p {
    display: block;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
}

  .box{
    width: 94%;
    padding: 0 3%;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
    float: left;
    margin-right: 10px;
  }
  /* .touxiang{
    width: 3.333rem;
    height: 3.333rem;
  } */
  .author-info-name:nth-child(1){
    display: inline-block;
    vertical-align: top;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    font-size: 1rem;
    font-weight: 500;
    color: #515767;
    padding: 0;
    margin: 0;
  }
  .author-info-name img{
    width: 35px;
    height: 16px;
  }
  
  .date-info{
    font-size: 0.9rem;
    color: #8a919f;
    position: absolute;
    bottom: 0;
    line-height: 22px;
  }
  ul li{
    list-style: none;
  }
  ol{
    padding-left: 28px;
    padding-right: 10px;
  }

  blockquote{color:#666;padding:15px 23px;margin:22px 0;border-left:4px solid #cbcbcb;background-color:#f8f8f8;}
  </style>

  <script>
  export default {
    name: 'IndexPage',
    data () {
        return {
          upinfo:{
            articleTitle:"2022年终总结——工作第五年",
            circleUrl: "https://p3-passport.byteimg.com/img/user-avatar/cf7ce21f16971d0f950a1048a2e99a69~100x100.awebp",
            upName:"阿彪最稳健了",
            upDate:"2023年01月11日 15:45",
            readed:"4978",
            level:"//lf3-cdn-tos.bytescm.com/obj/static/xitu_juejin_web/img/lv-2.99ba5b2.png",         
          },
          preface:{
            prefaceImg:"https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/2cd16299a58744e88ea6e738fc1bf9af~tplv-k3u1fbpfcp-zoom-crop-mark:3024:3024:3024:1702.awebp",
            text1:"「回顾2022，展望2023，我正在参与2022年终总结征文大赛活动」",
            text2:"2022是本命年，对我来说今年勉强可以算得上是一切顺利吧。",
            text3:"前几年的年终总结"
          },

          title:[{
            yijititle:'',erjititles:[{
              erjititle1:'先验收下去年的期望吧',erjititle2:"总结下2022年期望的完成情况",erjititle3:"对2023年的期望",
              sanjititles:[
                {
                  sanjititle1:"1、关于订婚和云南一周游 ✅",
                  text1:`今年大概2月底开始上海疫情开始变得很严重，然后就是漫长的三个月封控，原计划4月份订婚加云南一周游的计划也推迟了，好在儿童节那天终于解封了，买了个金镯子，给了6.6个w，然后6月6号订婚，计划2023年底领证，从大二开始谈恋爱到工作快五年了，即将修成正果。`,
                  text2:`云南的旅行真的期待太久了，最终选择趁着中秋节凑假期出行，避开国庆节。事实证明我的决定真特喵的机智😑！由于是旅游淡季，而且受疫情影响，不管是吃住都特别便宜。`,
                  text3:`第一站丽江挑到一家很赞的民宿，100多住到差不多35平米的房间，而且超级干净，连住3晚还附送接机服务，因为媳妇儿核酸结果出的太晚，导致我俩没法坐同一班飞机，我先到了之后在机场等她到12点多，然后凌晨1点才到住的地方，听说我们没吃饭老板还拿了白天做的大闸蟹、鲜花饼和咸鸭蛋给我们。后面去玉龙雪山、泸沽湖、包括去大理都可以从老板那边拼车，他们当地商家都有很多群一条龙服务，因为是淡季，价格我觉得还可以，不是很坑。`,
                  text3:`后面就是按媳妇儿做的攻略开始逛丽江古城，蓝月谷，玉龙雪山，泸沽湖、丽江古城、环大理洱海。`,
                  text4:`民宿门口的小池塘`,
                  img1:"https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/055aea953bf54a4aac921dc4ad2a67b2~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp",
                
                  sanjititle2:"2、关于看书 ❌",
                  text5:"今年太堕落了，去年买的两本书全都没看，小部分原因是今年大部分时间都是在家办公的状态，特别年初封控的三个月我一个人在家，媳妇儿封在公司里，每天没人说话，很郁闷，除了code，其他时间基本是在看电影、追剧打永劫无间，压根没看书。后半年到了新公司由于要熟悉新环境，熟悉项目，重新把angular捡起来，学习Three.js，学英语。好吧其实今年就是堕落了，下班就是在打游戏，基本想要看书的时候，脑子里就是下次一定。",
                  text6:"不过今年看了ThreeJs开发指南，已经看了百分之90，而且做了笔记，后面会拆分成文章发出来。",
                
                  sanjititle3:"3、关于学位考和学位证 ❌",
                  text7:"由于疫情考试一直被取消，到后面我都麻木了，然后年底的时候通知安排线上考试，我还以为学校也麻了，准备放水让我们都过了算了，就简单的复习了下，结果失算了，考试前一周的的时候上线看了下具体的考试要求，才发现是双机位考试，前面一个摄像头对着脸，后面也要求一个摄像头全程对着桌面和电脑屏幕，而且必须开麦，房间里不允许有其他人，根本没有机会抄，然后考前一周疯狂复习，结果考试当天老师也不讲武德，题目全是变体，然后就两门全挂，只能23年补考了！",
                
                  sanjititle4:"4、关于房产证 ❌",
                  text8:"契税要交快两万，没钱，没办，就是这样子。",
                
                  sanjititle5:"5、年底根据实际情况，提车 ✅",
                  text9:"12月初提车了，不过是问界M5四驱至臻版（我不是华为粉，买这个车纯看个人需求和性价比）。必须要吐槽外环高速真的堵成狗了，我早上要开一个小时20分钟才能到公司！",
                  img2:"https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/9600802812024e0fa2227f686d604a5e~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp",
                  text10:"为啥不是去年考虑的汉2代或小鹏p7或ct5或宝马x1顶配呢，",
                  cheque:[
                    "今年没出汉2代。",
                    "小鹏P7今年没改款而且感觉小鹏快G了。",
                    "ct5去四儿子店里看了，后排真的是网上说的那样狗都不坐。",
                    "宝马x1没去看。",
                    "另外今年考虑了c260L，媳妇儿看了内饰很心动，毕竟付首付她也出钱了，我就去问了4s店销售，报价33.5落地可谈，然后保险就要1.2w，预算超了4w，考虑到后面保养加油等花费，犹豫半天没去试驾。",
                    "极氪001很心动，不过到了年底了卖的又火，权益退坡太快了觉得不划算。",
                    "哪吒s增程大版店里没有试驾车，而且交付遥遥无期。",
                    "当时特斯拉Model Y 四驱长续航超预算了，这两天的消息特斯拉打骨折，降到29万多了，我心好痛，没有再等等！",
                  ],
                  text11:"大概心理历程就是这样，最终在上海试驾了问界M5四驱至臻，武汉提车。当时活动优惠8k，送了个watch3手表跟便宜的贴膜。到现在为止开了半个月，觉得整体还不错。就是余大嘴说的双层隔音玻璃，图书馆级别的静谧性我实在没体验到，差评。这点哪里来的遥遥领先？ 还有就是刚提车就出险了，在特么商城地下停车场出去的时候擦墙了，定完损去用户中心换了个前脸的壳子，真的啥比，停车场出口是S弯，而且窄的要死，墙上全都是车剐蹭的印子，也不知道重新修一下。",

                  sanjititle6:"6、提升自己的收入❌",
                  text12:"今年虽然跳槽涨了波工资，但还是很缺钱，买车首付还借了几个w，除了房贷又加了车贷，我真的头太铁了。",
                  text13:"提升收入这部分，真不知道除了code去哪里赚钱，感觉自己做了几年码农之后，思想已经出现固化了。今年想开发个宠物店的进销存系统卖给宠物店用的，卖猫那家老板娘本来答应我可以试用了，后来我带着设计去细谈的时候，老板分析了一波，我醒了，而且感觉很羞愧，自己有时还是天真了。国内大部分城市宠物店都是夫妻店，可能电脑都用不利索，进销存系统他们根本都不会用，而且也不会花钱去买的，自己本来赚的都是辛苦钱。稍微大一点的宠物连锁店，像他们自己家这种有个两三家分店的，老板自己会用excel搞一个表格就够用了，更大的连锁宠物店老板说她也没见过。",
                  text14:"另外今年年初封控没去当卖菜群的团长，年末没屯药卖，赚不来这种快钱。",
                
                  sanjititle7:"7、减肥 ✅",
                  text15:"勉强算是有效果吧，虽然跟去年比没有变化，但是今年11月的时候称了下已经159了，我直接裂开，然后坚持吃轻食，然后晚上有空了去跑步，现在降到151的样子。不过刚刚杨康，不敢跑步了，后面恢复了还得继续努力，目标是140。",
                
                  sanjititle8:"8、关于健康这部分 ❌",
                  text16:"身上的硬结偶尔还能发现，本来打算22年去做个全身体检的，结果一拖再拖，23年一定要做个全身体检。还有就是感觉IT行业每天上时间坐在位置上，颈椎病已经很常见了，刚毕业呆的那家公司同事，之前跟我说他颈椎病最严重的时候压迫神经，甚至发生过早上出门直接晕倒的情况。 快年底的时候身边有个朋友肾炎加重，出现了尿血的情况，好像继续加重会变成肾衰竭，他说就是一直要吃药控制指标。按他说的，他肾炎可能是作息不规律、不运动、加上久坐憋尿等等导致的。一定一定要爱惜自己的身体。",
                },

              //   {sanjititle:'这是h3标题0000',sijititles:[{sijititle:'这是h4标题',wujititles:[{
              //       wujititle:'这是h5标题',liujititles:[{
              //         liujititle:'这是h6标题'
              //       }]
              //     }]
              //   }]
              // }
            ],
            erjititle2s:[
              {
                text1:"3/8，一半都没达到！",
                text2:"大概盘了下，我特喵的整年基本都在打游戏，永劫无间都干到几百级了，段位上到蚀月，直接导致用来学习提升的时间被压缩了很多， 博客更新频率急速下降，而且能明显感觉到自己相较于去年提升不多，虽然也有些其他客观原因吧。",
                text3:"工作上今年下半年跳槽到一家500强外企，由小团队的前端扛把子变成大团队的前端螺丝钉。",
                text4:"其实从心里没想着跳槽，之前公司又稳定，通勤又近，同事又好，又是前端扛把子，自己感兴趣的技术都可以尝试去用，而且leader很乐意帮我逐步转型到产品经理，但是受限于收入（受疫情影响涨薪很少），受限于上升空间（受疫情影响公司对原来团队的定位更保守了），其实主要是太缺钱了，房贷要还，而且马上要订婚结婚，还要买车，彩礼等等等，唉😪",
                text5:"在现在的部门有时候会觉得挺难受的，都快不自信了。定位是Senior Engineer，前端现在四个人，一个Leader Engineer，其他两个也都是Senior，然后现有的产品都是Leader 他们之前做的，听他们讲历经了8年+的迭代，除了专职前端外还有全栈的同事参与开发，而且他们在ng1的时候就开始用了，很多东西都是自己琢磨的，可以说是非常经典的屎山项目了，没有Component Doc，组件怎么用完全一抹黑，甚至没有Api Doc，全靠口口相传，还有很多过度封装的地方，一言难尽，本地Start一个项目，要3-5分钟，Hot Update 1-2分钟，开发体验极差，我曾经尝试去优化构建，看到2000行的angular.json文件后我放弃了。",
                text6:"关于重构，跟老员工沟通了一下结合自己日常体验，结论就是大老板那里要提高部门竞争力，跟国外团队抢预算抢项目，对于代码优化或者重构也确实没法给到时间。另外在这边想推动一些变化是比较无力的，入职不久我提出过出一份api doc，我的直属老板拉了一个会议，最终是决定用swagger出一个api文档，但是至今我没见那个swagger地址有更新过。当然这也跟我后面没有持续跟进有关吧。至于组件文档，按会议上其中一个后端老员工的原话来讲就是",
                text7:"你要是觉得不方便你就自己写一份，大家都欢迎，你让别人写，别人很忙啊，手上一堆事要处理，哪里有时间去写这个呢！",
                text8:"其实想想也没毛病，大家都很忙啊！现在结果都已经这样了，还能怎么办呢😫",
                text9:"不过让我也没法写，屎山要挖这么深，怎么挖，我刚来不久，多少个基础组件，多少个业务组件我都不晓得，然后就不了了之了。",
                text10:"日常开发是这边是分了敏捷team，部分业务team和一个架构team（里面全是leader engineer），我理所应当的就归属于业务仔了，技术评审轮不到业务team来做，也就是说我回归了搬砖仔的岗位，加上自己英语不好，有些需要跟国外团队合作开发的项目也暂时无法加入，总的来说就是心里落差很大，不甘心却又不知道如何破局，只能想办法先把英语搞定。",
                text11:"生活上今年好像没什么变化。年初封城在家办公三个月，年底解封阳了又在家办公接近一个月，今年像是丢了四个月的时间。",
                text12:"今年年初搬了新家，住上了一室一厅一厨一卫，皮蛋现在14斤了是个大肥猫，皮小花也10斤了，现在小花变成了挨揍的那个，被皮蛋揍得上蹿下跳。然后年底的时候买猫的那家宠物店因为疫情倒闭了。",
                text13:"新公司通勤单程1h20min，买车之后走外环高速早高峰还是1h20min，晚上倒是快了，40-50min就到家，不过公司停车费600一个月我好特么心疼啊！为了补上停车费，我现在开始带饭了，晚上炒一个菜，第二天可以带两顿，还避免了外卖高油高盐，省钱又健康，好耶😋！",
                text14:"还有就是身边朋友一个个都要成家了，一个关系好的高中同学年前结婚，一个大学室友过年的时候也要结婚了。还有疫情三年，三观被一直被刷新，对越南现状表示无奈，屠龙者后代终成了恶龙。",
                text15:"如果说有什么是我现在非常后悔的事，那就是20年傻了吧唧的去买了房！狗都不买！ 如果可以补充，可以酸一把的话，那就是我曾经的创业思路，被别人做起来了，现在已经接近20人团队，看他朋友圈，每年单研发费用支出就得200w了😣，这还是在郑州这种二线城市，而我还是个码仔。 不过即使我当时真的辞职去做，刚毕业不久没有资金支持，没有几个靠谱合伙人说不定我早就天台见了。",
              },
            ],
            erjititle3s:[{
              text1:"无法全力倚父，那就全力以赴。",
              text2:"2023年对自己来讲绝对是关键的一年",
              erjititle3slist:[
                "拿下三门学位考。",
                "看书，看更多的书，不限于技术类。保底也要看完重构改善既有代码的设计和大话设计模式。",
                "搞定英语读写和基本无障碍口语交流，保底看两本以上英文书，并且敢于开口用英语交流。",
                "扩充知识面，卷一点源码学习思路，输出10篇以上的技术文章，尝试做个VR/AR相关的Demo玩一玩，尝试入门Web3。",
                "把结婚证领了，然后去一趟西藏。",
                "减到140，平时注意锻炼身体，做一个全身体检, 参加一个羽毛球俱乐部，多打打羽毛球。",
                "尝试破局，不再局限于程序员和打工仔的身份去看待事情。"
              ],
              text3:"今年一定要克服自己自制力差的问题，把目标做拆分，然后每个月复盘一次，既然自制力差，不持久，那就提高打鸡血的频率，我特喵要直接化身鸡血战士！",
            }]
            }]
          },
          ]

          // title:[{
          //   yijititle:'这是h1标题',erjititles:[{
          //     erjititle:'这是h2标题',sanjititles:[{
          //       sanjititle:'这是h3标题',sijititles:[{
          //         sijititle:'这是h4标题',wujititles:[{
          //           wujititle:'这是h5标题',liujititles:[{
          //             liujititle:'这是h6标题'
          //           }]
          //         }]
          //       }]
          //     }]
          //   }]
          // },
          // {
          //   yijititle:'这是h1标题',erjititles:[{
          //     erjititle:'这是h2标题',sanjititles:[{
          //       sanjititle:'这是h3标题',sijititles:[{
          //         sijititle:'这是h4标题',wujititles:[{
          //           wujititle:'这是h5标题',liujititles:[{
          //             liujititle:'这是h6标题'
          //           }]
          //         }]
          //       }]
          //     }]
          //   }]
          // },]
          

  
        }
      }
  }
  </script>
  