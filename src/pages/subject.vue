<template>
    <div>
      <Subject txt="书影音">
        <img src="../assets/images/ic_group_search.png" alt="" slot="left" class="leftImg">
        <img src="../assets/images/ic_create_group_chat_blue.png" alt="" slot="right" class="rightImg">
      </Subject>
      <div>
         <div class="twoLevelRouting">
           <span><router-link to="/subject/file">电影</router-link></span>
           <span><router-link to="/subject/read">读书</router-link></span>
           <span><router-link to="/subject/tv">电视</router-link></span>
           <span><router-link to="/subject/city">同城</router-link></span>
           <span><router-link to="/subject/music">音乐</router-link></span>
         </div>
         <div>
           <router-view></router-view>
         </div>
      </div>
      <Modular>
        <p slot="modleft">电影院热映</p>
        <p slot="modright">更多</p>
      </Modular>
    </div>
</template>

<script>
  import Subject from "../components/Header"
  import Modular from "../components/Modular"
    export default {
        name: "subject",
      components:{
          Subject,Modular
      }
    }
</script>

<style scoped>

.twoLevelRouting span{
  display: inline-block;
  width: 15%;
  text-align: center;
}
.twoLevelRouting a{
 text-decoration:none;
}
</style>
