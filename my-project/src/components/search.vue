<template>
  <div class="search flex-col-center">
    <div class="search-div flex-col-center">
      <i class="icon-search search-icon mgl-30"></i>
    </div>
    <input type="text" :disabled="disabled" placeholder="搜索">
  </div>
</template>
<script>
  export default {
    props:{
      disabled:{
        type:Boolean,
        default:false,
      },
    },
  }
</script>
<style lang="scss">
  @import '@S/color.scss';
  @import '@S/iconfont.scss';
  @import "@S/style.scss";
  .search{
    width:600rpx;
    height: 57rpx;
    background-color: $bg-light-grey;
    border-radius:27rpx;
    line-height: 51rpx;
    position: relative;
    &-div{
      position: absolute;
    }
    input{
      padding-left:72rpx; 
      width:100%;
      font-size: 24rpx;
    }
  }
</style>


