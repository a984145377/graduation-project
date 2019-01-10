<template>
  <div class="index">
    <!-- 搜索框 -->
    <search disabled=true ></search>
    <!-- 功能列表 -->
    <div class="index-nav flex-ver-center">
      <ul class="index-nav-ul">
        <li v-for="(item,index) in navList" :key="index" :class="['index-nav-ul-li','mgb-35',item.isMarginLeft?'mgl-35':'',item.isMarginRight?'mgr-35':'']">
          <i :class="[item.icon,'mar-ver-center']"></i>
          <span class="fs-24">{{item.name}}</span>
        </li>
      </ul>
    </div>
    <!-- 树洞说说 -->
    <p class="pdl-20 index-title">树洞说说</p>
    <!-- 最新、最热 -->
    <div class="index-bar mgt-20">
      <div class="index-bar-hot">
        <span class="fs-32">最热</span>
        <div class="index-bar-single">
          <i class="icon-noColor-single-top"></i>
          <i class="icon-noColor-single-bottom"></i>
        </div>
      </div>
      <div class="index-bar-new">
        <span class="fs-32">最新</span>
        <div class="index-bar-single">
          <i class="icon-noColor-single-top"></i>          
          <i class="icon-noColor-single-bottom"></i>
        </div>
      </div>     
    </div>
    <!-- 分割线 -->
    <messages v-for="(item,index) of messageList" :key="index" :item="item"></messages>
    <messages v-for="(item,index) of messageList" :key="index" :item="item"></messages>
    <!-- <messages :item="messageList"></messages> -->
  </div>
</template>

<script>
  import Search from '@C/search'
  import CutOffLine from '@C/cutOffLine'
  import Messages from '@C/message'
  export default {
    components:{
      Search,
      CutOffLine,
      Messages
    },
    data(){
      return{
        navList:[{
          id:1,name:'校园活动',icon:'icon-school-activity',isMarginRight:true,isMarginLeft:false,
        },{
          id:2,name:'二手市场',icon:'icon-flea-market',isMarginRight:true,isMarginLeft:true,
        },{
          id:3,name:'失物招领',icon:'icon-thing-get',isMarginRight:true,isMarginLeft:true,
        },{
          id:4,name:'资源共享',icon:'icon-resource-share',isMarginRight:false,isMarginLeft:true,
        },{
          id:4,name:'资源共享',icon:'icon-resource-share',isMarginRight:true,isMarginLeft:false,
        }],
        messageList:[
          {imgSrc:require('../../images/test-avatar.png'),name:"哈哈哈哈",time:"2018-10-10 14:30:20",text:'哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈',imgs:[require('../../images/test-imgs.png'),require('../../images/test-imgs.png'),require('../../images/test-imgs.png')]},
        ]
      }
    },
    mounted(){

    },
  }
</script>
<style lang="scss">
  @import "@S/style.scss";
  .index{
    position: relative;
    height: 100%;
    .search{
      margin:0 auto;//水平
      margin-top:30rpx;
    }
    &-nav{
      width:100%;
      height: 280rpx;
      margin-top:40rpx;
      &-ul{
        width: 620rpx;
        height: 100%;
        display: flex;
        flex-wrap: wrap;
        padding-left:30rpx;
        &-li{
          height: 100rpx;
          width:98rpx;
        }
      }
    }
    &-title{
      font-size:40rpx;
    }
    &-bar{
      height: 70rpx;
      width:100%;
      display: flex;
      >div{
        flex: 1;
        display: flex;
        align-items: center;
        justify-content: center; 
        >span{
          margin-right: 11rpx;
        }
      }
      &-hot{

      }
      &-new{

      }
    }
    .footer{
      position: absolute;
      bottom: 0;
    }
  }
</style>

