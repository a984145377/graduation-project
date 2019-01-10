<template>
  <div class="message">
    <cut-off-line></cut-off-line>
    <div class="message-top pdt-26 pdl-20">
      <img :src="item.imgSrc" alt="" class="message-top-avatar">
      <div class="message-top-info pdl-20">
        <span class="fs-26">{{item.name}}</span>
        <span class="fs-22">{{item.time}}</span>
      </div>
    </div>
    <div class="message-text mgt-20 pdr-20 pdl-20">
      <p class="ellipse-6 fs-26">{{item.text}}</p>
    </div>
    <div class="message-imgs pdl-20">
      <img :src="imgItem" alt="" v-for="(imgItem,index) of item.imgs" :key="index" class="message-imgs-img">
    </div>
    <div class="message-fenli mgl-20">
      <div class="">

      </div>
    </div>
    <MessageOperation></MessageOperation>
  </div>
</template>
<script>
  import MessageOperation from "./messageOperation.vue"
  import CutOffLine from './cutOffLine'
  export default {
    components:{
      MessageOperation,
      CutOffLine,
    },
    props:{
      item:{},
    },
    mounted(){
    }
  }
</script>
<style lang="scss">
  .message{
    &-top{
      display: flex;
      &-avatar{
        width:78rpx;
        height: 78rpx;
      }
      &-info{
        display: flex;
        flex-direction: column;
        justify-content: center;
      }
    }
    &-text{

    }
    &-imgs{
      margin-top:10rpx;
      &-img{
        width:219rpx;
        height: 219rpx;
        padding-right:20rpx;
      }
    }
    &-fenli{
      div{
        width: 100%;
        height: 1rpx;
        background-color: #eeeeee;
      }    
    }
  }
</style>
