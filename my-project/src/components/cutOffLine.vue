<template>
  <div class="cut-off-line" :style="{width:width,height:height,backgroundColor:backgroundColor}">
    
  </div>
</template>
<script>
  export default {
    props:[
      {
        width:{
          type:String,
          default:'100%'
        },
        height:{
          type:String,
          default:'17rpx'
        },
        backgroundColor:{
          type:String,
          default:'$bg-height-light-grey'
        },
      }
    ],
  }
</script>
<style lang="scss">
  @import '@S/color.scss';
  .cut-off-line{
    height: 17rpx;
    width: 100%;
    background-color: $bg-height-light-grey;
  }
</style>


