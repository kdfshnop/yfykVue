<template>
  <div class="xf-poster">

    <!--楼盘画报-->
    <div class="wk-panel building-poster" v-for="(item , index) in getInfoData.posterData" :key="item.id">
      <div class="poster-info" >
        <p class="title">{{item.title}}</p>
        <p class="time">{{item.publishTimeStr}}</p>
        <div class="poster-pic"><img :src="item.fileKey" :alt="item.fileName"></div>
        <p class="poster-content">{{item.content}}</p>
      </div>
    </div>

  </div>
</template>

<script>
  import data from '../../../mock/xf/posters';

  export default {
    name: "xfPoster",
    data() {
      return {
        getInfoData:{
          posterData: data.data,
        }
      }
    },
    methods:{

    }
  }
</script>
<style lang="less">
  @import "../../../src/less/xf/poster.less" ;
</style>
