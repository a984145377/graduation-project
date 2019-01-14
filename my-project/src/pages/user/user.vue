<template>
  <div class="user" :style="{height:height}">
    <div class="user-info flex-center">
      <i class="icon-setting"></i>
      <img src="../../images/test-avatar.png" alt="" class="user-info-avatar">
      <p class="user-info-name fs-28 mgt-10">站着说好不腰疼</p>
      <p class="user-info-brief fs-30 mgt-10">简介:哈哈哈哈哈哈哈哈哈哈哈哈</p>
    </div>
    <div class="user-cell" v-for="(item,index) of cellList" :key="index">
      <div class="user-cell-left">
        <i :class="[item.leftIcon]"></i>{{item.leftText}}
      </div>
      <div class="user-cell-right">
        <i class="icon-xiala rotate"></i>
      </div>
    </div>
    
  </div>
</template>
<script>
  import Common from "@C/common.vue"
  export default {
    components:{
      Common,
    },
    data(){
      return{
        cellList:[{
          leftText:'我的创作',leftIcon:'icon-user-compile'
        },{
          leftText:'我的浏览',leftIcon:'icon-user-liulan'
        },{
          leftText:'我的点赞',leftIcon:'icon-user-dianzan'
        },{
          leftText:'我的收获',leftIcon:'icon-user-compile'
        },{
          leftText:'帮助与反馈',leftIcon:'icon-user-bangzhi'
        }],
        height:'auto'
      }
    },
    mounted(){
      var self = this
      wx.getSystemInfo({
        success(res){
          self.height = res.windowHeight+'px';
        }
      })
    }
  }
</script>
<style lang="scss">
  @import "@S/style.scss";
  @import "@S/color.scss";
  .user{
    background-color: $bg-f5-grey;
    height: 100%;
    &-info{
      height: 320rpx;
      width:100%;
      flex-direction: column;
      position: relative;
      background-color: $bg-white;
      i{
        position: absolute;
        right: 20rpx;
        top:20rpx;
      }
      &-avatar{
        height: 130rpx;
        width:130rpx;
        border-radius: 50%;      
      }
      &-name{
        
      }
      &-brief{
        color: $text-light-grey;
      }
    }
    &-cell{
      margin-top:20rpx;
      height: 100rpx;
      display: flex;
      align-items: center;
      justify-content: space-between;
      background-color:$bg-white;
      &-left{
        padding-left:24rpx;
        display: flex;  
        font-size: 30rpx;  
        >i{
          margin-right: 24rpx;
        }    
      }
      &-right{
        padding-right:24rpx;
      }
    }
  }
</style>


