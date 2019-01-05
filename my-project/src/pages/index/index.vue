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
    
  </div>
</template>

<script>
  import Search from '@C/search'
  export default {
    components:{
      Search
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
        }]
      }
    },
    mounted(){

    }
  }
</script>
<style lang="scss">
  @import "@S/style.scss";
  .index{
    .search{
      margin-top:20rpx;
      margin:0 auto;//水平
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
  }
</style>

