<template>
    <div>
      <Radio txt="广播">
        <img src="../assets/images/ic_status_search_user.png" alt="" slot="left" class="leftImg">
        <img src="../assets/images/ic_create_group_chat_blue.png" alt="" slot="right" class="rightImg">
      </Radio>
    </div>
</template>

<script>
  import Radio from "../components/Header"
    export default {
        name: "radio",
      components:{
          Radio
      }
    }
</script>

<style scoped>

</style>
