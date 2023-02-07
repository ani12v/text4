<template>
  <div class="box">
    <!-- <el-container> -->
      <!-- <el-main> -->
        <div class="max-w-6xl mx-auto mt-6 sm:px-6 lg:px-8">
          <!-- 标题 -->
          <h1 class="artical-title">{{upinfo.articleTitle}}</h1>
           <!-- 作者信息 -->    
          <el-row>
            <!-- up主头像 -->
            <!-- <el-col :span="2"> -->
              <div class="grid-content bg-purple-dark">
              <div class="demo-basic--circle">
                <div class="block"><el-avatar :size="50" :src="upinfo.circleUrl">
                  </el-avatar></div>
              </div>
            </div>
          <!-- </el-col> -->
            <!-- up主相关信息 -->
            <!-- <el-col :span="20"> -->
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
          <!-- </el-col> -->
          </el-row> 
          <!-- 文章详情 -->

          <div>
            <div :key="yiji.name" v-for="yiji in title">
                <h1>{{ yiji.yijititle }}</h1>
                <div :key="erji.name" v-for="erji in yiji.erjititles">
                    <h2>{{erji.erjititle}}</h2>
                    <div :key="sanji.name" v-for="sanji in erji.sanjititles">
                        <h3>{{sanji.sanjititle}}</h3>
                        <div :key="siji.name" v-for="siji in sanji.sijititles">
                            <h4>{{siji.sijititle}}</h4>
                            <div :key="wuji.name" v-for="wuji in siji.wujititles">
                                <h5>{{wuji.wujititle}}</h5>
                                <div :key="liuji.name" v-for="liuji in wuji.liujititles">
                                    <h6>{{liuji.liujititle}}</h6>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

        <div class="h1">
          <!-- 一级标题 -->
            <div v-for="h1 in upinfo.detail.h1"
               :key="h1">
              <h1>
                {{h1}}                 
              </h1>
              <!-- 二级标题 -->
              <div class="h2">
                <div v-for="h2 in upinfo.detail.h2"
                  :key="h2">
                  <h2>{{h2}}</h2>
                </div>
                <!-- 三级标题 -->
                <div class="h3">
                  <div v-for="h3 in upinfo.detail.h3"
                    :key="h3">
                    <h3>{{h3}}</h3>
                  </div>
                  <!-- 四级标题 -->
                  <div class="h4">
                    <div v-for="h4 in upinfo.detail.h4"
                      :key="h4">
                      <h4>{{h4}}</h4>
                    </div>
                    <!-- 五级标题 -->
                    <div class="h5">
                      <div v-for="h5 in upinfo.detail.h5"
                        :key="h5">
                        <h5>{{h5}}</h5>
                      </div>
                      <!-- 六级标题 -->
                      <div class="h6">
                        <div v-for="h6 in upinfo.detail.h6"
                          :key="h6">
                          <h6>{{h6}}</h6>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              
              </div>
            </div>

        </div>
       </div>
    <!-- </el-container> -->
  </div>
</div>
  </template>
  <style>
  .box{
    width: 94%;
    padding: 0 3%;
    /* display: flex;
    justify-content: center;
    overflow: hidden; */
  }
    
    /* body{background-color: #eceff4;} */

    /* .bg-purple-light {
      background: #e5e9f2;
    } */
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
  li{
    list-style: none;
  }
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
            detail:{
              h1:["2022是本命年，对我来说今年勉强可以算得上是一切顺利吧",
            ],
              h2:["2022是本命年，对我来说今年勉强可以算得上是一切顺利吧",
            
            ],h3:["2022是本命年，对我来说今年勉强可以算得上是一切顺利吧",
            ],
            h4:["2022是本命年，对我来说今年勉强可以算得上是一切顺利吧",
            ],
            h5:["2022是本命年，对我来说今年勉强可以算得上是一切顺利吧",
            ],
            h6:["2022是本命年，对我来说今年勉强可以算得上是一切顺利吧",
             
            ],
            
            },          
          },
          title:[{
            yijititle:'这是h1标题',erjititles:[{
              erjititle:'这是h2标题',sanjititles:[{
                sanjititle:'这是h3标题',sijititles:[{
                  sijititle:'这是h4标题',wujititles:[{
                    wujititle:'这是h5标题',liujititles:[{
                      liujititle:'这是h6标题'
                    }]
                  }]
                }]
              }]
            }]
          },
          {
            yijititle:'这是h1标题',erjititles:[{
              erjititle:'这是h2标题',sanjititles:[{
                sanjititle:'这是h3标题',sijititles:[{
                  sijititle:'这是h4标题',wujititles:[{
                    wujititle:'这是h5标题',liujititles:[{
                      liujititle:'这是h6标题'
                    }]
                  }]
                }]
              }]
            }]
          },]
          

  
        }
      }
  }
  </script>
  