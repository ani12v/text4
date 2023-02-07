<template>

  <!-- 整个页面 -->
  <div>

    <!-- 顶部导航栏 -->
    <div class="header">
      顶部导航栏
    </div>

    <div>
      <!-- 主页导航栏 -->
      <div class="homeheader">
        主页导航栏
      </div>
    </div>

    <!-- 正文 -->
    <div  class="main">

      <!-- 正文内容 -->
      <div class="maintext">
        <detail/>
      </div>

      <!-- 侧边栏 -->
      <div class="aside">
      </div>
    </div>
  </div>
</template>

<script>
import detail from "~/pages/components/detail";
export default {
  components:{
    detail
  },
}
</script>
<style>
html,body,div{
    margin: 0;
    padding: 0;
  }
.header{
  width: 100%;
  height: 3rem;
  background: red;
}
.homeheader{
  width: 100%;
  height: 2rem;
  background: rgb(211, 224, 172);
}
.main{
  width: 100%;
  /* height: 51vw; */
  background: #eceff4;
  display: flex;
  justify-content: center;
  overflow: hidden;
}
.maintext{
  width: 64%;
  height: 100%;
  background-color: white;
}
.aside{
  width: 20%;
  /* height: 100%; */
  height: 51vw;
  margin-left: 20px;
  background-color: burlywood;
}
@media (max-width:960px){
  .main{
    width: 100%;
    height: auto;
    background: black;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
  .maintext{
    width: 100%;
    height: 100%;
    background-color: white;
  }
  .aside{
    width: 0px;
    height: 0px;
 }
 .gist1{
    font-weight: 700;
    font-size: 5vw;
    line-height: 10vw;
    color: #1d2129;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
  }
.gist2{
    line-height:7vw;
    font-size: 2vw;
    color: #999;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
  }
}
</style>
