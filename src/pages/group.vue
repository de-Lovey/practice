<template>
    <div class="bg">
      <Myheader txt="小组" >
        <img src="../assets/images/ic_group_search.png" alt="" slot="left" class="leftImg">
        <img src="../assets/images/ic_create_group_chat_blue.png" alt="" slot="right" class="rightImg">
      </Myheader>
    </div>
</template>

<script>
  import Myheader from "../components/Header"
    export default {
        name: "group",
      components:{
        Myheader
      }
    }
</script>

<style scoped>
    .bg{
        background: #fff;
    }
</style>
