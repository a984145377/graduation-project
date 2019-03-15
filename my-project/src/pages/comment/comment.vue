<template>
  <div class="comment">
    <div class="comment-title">
      <span class="fs-30 comment-title-cancel">取消</span>
      <div class="comment-title-name">
        <p class="send-title fs-32">发说说</p>
        <p class="comment-title-name-user fs-28">哈哈哈啊</p>
      </div>
      <button class="comment-title-send fs-30">
        发送
      </button>
    </div>
    <div class="comment-text">

    </div>
    <div class="comment-function">

    </div>
  </div>
</template>
<script>
  import Common from "@C/common.vue"
  export default {
    
  }
</script>
<style lang="scss">
  @import '@S/color.scss';

  .comment{
    &-title{
      display: flex;
      align-items: center;
      border-bottom:1px solid $bg-f5-grey;
      position: relative;
      &-cancel{
        position: absolute;
        left:20rpx;
      }
      &-name{
        margin:0 auto;
        margin-bottom:10rpx;
        text-align: center;
        &-user{
          color:$text-grey;
        }
      }
      &-send{
        margin-left:0;
        line-height: 2.1;
        position: absolute;
        right: 20rpx;
      }
    }
    
  }
</style>


