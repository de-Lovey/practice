<template>
    <div>
     <Header bol="true" class="head">
         <img src="../assets/images/ic_chat_white.png" alt="" slot="right" class="rightImg">
         <input type="text" slot="search" class="searchs">
     </Header>
      <Banner>
        <div slot="slid" class="swiper-slide">
          <img src="../assets/images/banner/01.jpg" alt="">
        </div>
        <div slot="slid" class="swiper-slide">
          <img src="../assets/images/banner/02.jpg" alt="">
        </div>
        <div slot="slid" class="swiper-slide">
          <img src="../assets/images/banner/03.jpg" alt="" class="imgNews">
        </div>
      </Banner>
      <Modular class="hot">
          <div class="orangeHot"></div>
          <p slot="modleft">热点</p>
      </Modular>
      <div>
           <ul>
             <li v-for="item in arr">
              <router-link :to="{name:'xiangqing',params:{id:item.id}}">
                <News :title="item.title"
                      :des="item.des"
                      :author="item.author">
                  <img :src="item.src" alt="" slot="Img">
                </News>
              </router-link>
             </li>
           </ul>
         </div>
    </div>
</template>

<script>
  import Header from "../components/Header"
  import Banner from "../components/banner"
  import  Modular from "../components/Modular"
  import News from "../components/News"
  import axios from "axios"
    export default {
        name: "home",
      components:{
        Header,Banner,Modular,News
      },
      data:function(){
          return {
            arr:[]
          }
      },
      created:function () {
        var that=this;
        axios.get('../../static/newslist.json').then(function (res) {
          //res是json文件 res.data是json里的数据
          // console.log(res.data);
           that.arr=res.data;
           console.log(that.arr);
        })
      }
    }
</script>

<style scoped>
.head .searchs{
  width: 90%;
}

  /*新闻*/
  ul li{
    list-style-type: none;
  }
</style>
