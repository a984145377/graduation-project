<template>
  <div class="message-operation pdl-20">
    <div class="message-operation-share">
      <i class="icon-share"></i>分享
    </div>
    <div class="message-operation-comment">
      <i class="icon-comment"></i>评论
    </div>
    <div class="message-operation-dianzan ">
      <i class="icon-dianzan"></i>1
    </div>
  </div>
</template>
<script>
  export default {
    
  }
</script>
<style lang="scss">
  .message-operation{
    display: flex;
    height: 65rpx;
    div{
      flex:1;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 26rpx;
    }
    &-share{
      i{
        margin-right: 7rpx;
      }
    }
    &-comment{
      i{
        margin-right:10rpx;
      }
    }
    &-dianzan{
      i{
        margin-right: 7rpx;
      }
    }
  }
</style>


