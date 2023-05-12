<template>
  <div class="fishBone">
    <div class="fish_ul">
      <div class="fish_li" v-for="(item,index) in fish_month">{{ item.name }}</div>
    </div>
  </div>
</template>
<script>
export default {
  data(){
    return{
      fish_month:[{name:"1月"},{name:"2月"},{name:"3月"},{name:"4月"},{name:"5月"},{name:"6月"},{name:"7月"},{name:"8月"},{name:"9月"},{name:"10月"},{name:"11月"},{name:"12月"}]
    }
  }
}
</script>
<style  scoped>
.fishBone{}
.fish_ul{
  display: flex;
}
.fish_li{
  width: 120px;
  height: 40px;
}
</style>
