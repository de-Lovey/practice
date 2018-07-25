<template>
    <div>
      <Mine txt="我的">
        <img src="../assets/images/ic_settings.png" alt="" slot="right" class="rightImg">
      </Mine>
        <Modular text="提醒">
          <img src="../assets/images/ic_settings.png" alt="" slot="modleft" class="modImg">
          <p slot="modcontent">提醒</p>
          <img src="../assets/images//ic_arrow_gray_small.png" alt="" slot="modright" class="modImg">
        </Modular>
    </div>
</template>

<script>
  import Mine from "../components/Header"
  import Modular from "../components/Modular"
    export default {
        name: "mine",
      components:{
          Mine,Modular
      }
    }
</script>

<style scoped>

</style>
