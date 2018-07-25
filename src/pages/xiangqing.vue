<template>
    <div class="product">
      <!--{{$route.params.id}}-->
      <p>id：{{product.id}}</p>
      <p>作者：{{product.author}}</p>
      <img :src="product.src" alt="">
    </div>
</template>

<script>
  import  axios from 'axios'
    export default {
        name: "xiangqing",
      data:function () {
        return{
          product:[]
        }
      },
      created:function () {
        var newId=this.$route.params.id;
        console.log(newId);
        var that=this;
        axios.get("../../static/newslist.json").then(function (res) {
          // console.log(res.data);
          for (var i=0;i<res.data.length;i++){
              var items=res.data[i];
              console.log("items:"+items.author);
              if(newId==items.id){
                  that.product=items;
              }

          }
        })
      }

    }
</script>

<style scoped>

</style>
