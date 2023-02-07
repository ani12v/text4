<template>
 <div>
    <el-tabs v-model="activeName" @tab-click="handleClick" style="margin-left: 10px;margin-right: 10px;">
        <el-tab-pane  :key="category.name"
                      v-for="category in categorys"
                      :label="category.label"
                      :name="category.name"
                      >
          <!-- 本标签下文章内容 -->
          <el-row class="cardmain">
          <el-col class="card" :span="8" :key="card.name" v-for="card in category.cards">
            <el-card style="margin: 0;padding: 0;">
              <div class="cardheader">
                <span>{{card.username}}</span>
                <el-divider direction="vertical"></el-divider>
                <span>{{card.date}}</span>
                <el-divider direction="vertical"></el-divider>
                <span>{{card.tag}}</span>
              </div>
              <div style="display: flex; justify-content: center;">
                <div class="article">
                  <div class="gist1">{{card.title}}</div>
                  <div class="gist2">{{card.gist}}</div>
                </div>
                <img src="https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/3cb06981fc8a4f3fa66b314b5b77faa6~tplv-k3u1fbpfcp-no-mark:240:240:240:160.awebp?" class="img">
              </div>
            </el-card>
          </el-col>
        </el-row>
        </el-tab-pane>
      </el-tabs>
 </div>
</template>
<script>
 export default {
  name:'Main',
   data () {
     return {
      activeName: '1',
      categorys:[
        {label:'推荐',name:'1',cards:[
                              {username:"青训营官方账号",
                              date:"4月前",
                              tag:"青训营",
                              title:"叮咚！青训营-快乐出发Flag打卡活动来啦",
                              gist:"的数量开服就亏了多少解放路水电费水电费塞德里克封建时代双方都没法看了时代峰峻",
                              },
                              {username:"测试1",
                              date:"1.29",
                              tag:"马一珂",
                              title:"这是进行for循环嵌套测试",
                              gist:"这是第一页推荐",
                              }
                            ],
        },
      {label:'最新',name:'2',cards:[
                              {username:"青训营官方账号",
                              date:"4月前",
                              tag:"青训营",
                              title:"叮咚！青训营-快乐出发",
                              gist:"的数量开服就亏了多少解放路水电费水电费塞德里克封建时代双方都没法看了时代峰峻",
                              },
                              {username:"测试2",
                              date:"1.29",
                              tag:"马一珂",
                              title:"这是进行for循环嵌套测试",
                              gist:"这是第二页最新",
                              }
                            ],
    },
      {label:'热榜',name:'3',cards:[
                              {username:"青训营官方账号",
                              date:"4月前",
                              tag:"青训营",
                              title:"叮咚！青训营-快乐出发Flag打卡活动来啦",
                              gist:"的数量开服就亏了多少解放路水电费水电费塞德里克封建时代双方都没法看了时代峰峻",
                              },
                              {username:"测试3",
                              date:"1.29",
                              tag:"马一珂",
                              title:"这是进行for循环嵌套测试",
                              gist:"这是第三页热榜",
                              }
                            ],},
      {label:'aaa',name:'4',cards:[
                              {username:"青训营官方账号",
                              date:"4月前",
                              tag:"青训营",
                              title:"叮咚！青训营-快乐出发Flag打卡活动来啦",
                              gist:"的数量开服就亏了多少解放路水电费水电费塞德里克封建时代双方都没法看了时代峰峻",
                              },
                              {username:"测试4",
                              date:"1.29",
                              tag:"马一珂",
                              title:"这是进行for循环嵌套测试",
                              gist:"这是第四页aaa",
                              }
                            ],},
      {label:'bbb',name:'5',cards:[
                              {username:"青训营官方账号",
                              date:"4月前",
                              tag:"青训营",
                              title:"叮咚！青训营-快乐出发Flag打卡活动来啦",
                              gist:"的数量开服就亏了多少解放路水电费水电费塞德里克封建时代双方都没法看了时代峰峻",
                              },
                              {username:"测试5",
                              date:"1.29",
                              tag:"马一珂",
                              title:"这是进行for循环嵌套测试",
                              gist:"这是第五页bbb",
                              }
                            ],},
      {label:'ccc',name:'6',cards:[
                              {username:"青训营官方账号",
                              date:"4月前",
                              tag:"青训营",
                              title:"叮咚！青训营-快乐出发Flag打卡活动来啦",
                              gist:"的数量开服就亏了多少解放路水电费水电费塞德里克封建时代双方都没法看了时代峰峻",
                              },
                              {username:"测试6",
                              date:"1.30",
                              tag:"马一珂",
                              title:"这是进行for循环嵌套测试",
                              gist:"这是第六页ccc",
                              }
                            ],},
      {label:'ddd',name:'7',cards:[
                              {username:"青训营官方账号",
                              date:"4月前",
                              tag:"青训营",
                              title:"叮咚！青训营-快乐出发Flag打卡活动来啦",
                              gist:"的数量开服就亏了多少解放路水电费水电费塞德里克封建时代双方都没法看了时代峰峻",
                              },
                              {username:"测试7",
                              date:"1.30",
                              tag:"马一珂",
                              title:"这是进行for循环嵌套测试",
                              gist:"这是第七页ddd",
                              }
                            ],},
      {label:'eee',name:'8'},
      {label:'fff',name:'9'},
      {label:'ggg',name:'10'},
      {label:'hhh',name:'11'},
      {label:'iii',name:'12'},
      {label:'jjj',name:'13'},
      {label:'kkk',name:'14'},
      {label:'lll',name:'15'},
      {label:'mmm',name:'16'},
    ]
     }
   },
   methods: {
    handleClick(tab, event) {
        console.log(tab, event);
    }
  }
 }
</script>
<style>
.cardmain{
  width: 100%;
  height: 100%;
}
.card{
  width: 100%;
  height: auto;
  padding-bottom: 1vw;
}
.cardheader{
  margin-left: 1vw;
  align-items: center;
  font-size: 13px;
  line-height: 22px;
  color: #4e5969;
}
.article{
   width: 80%;
   margin-left: 1vw;
   /* 超出的文本隐藏 */
  overflow:hidden;
  /* 溢出用省略号显示 */
  text-overflow:ellipsis;
  /* 溢出不换行  */
  white-space:nowrap;
}
.gist1{
  font-weight: 700;
  font-size: 2vw;
  line-height: 3vw;
  color: #1d2129;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  }
.gist2{
  line-height: 3vw;
  font-size: 1vw;
  color: #999;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  }
.img{
  width: 120px;
  height: 80px;
  margin-left: 1vw;
}

</style>
