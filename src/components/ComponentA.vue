<template>
  <countdown :time="myTime" :interval="myInterval">
    <template slot-scope="props">倒计时：{{ props.days }} 天, {{ props.hours }} 时, {{ props.minutes }} 分, {{ props.seconds }} 秒.</template>
  </countdown>
</template>

<script>
import Vue from 'vue';
import VueCountdown from '@chenfengyuan/vue-countdown';
 
Vue.component(VueCountdown.name, VueCountdown);

export default {
  name: 'ComponentA',
  computed: {
    myTime: function(){
      return 2 * 24 * 60 * 60 * 1000;  //倒计时2天，此时间可以进页面的时候从后台拉取剩余的时间
    },
    myInterval: function(){
      return 1000;   //倒计时间隔1s
    }
  }
}
</script>

<style scoped>
</style>