<template>
    <div>
        <div class="header">
            <v-header></v-header>
        </div>
        <div class="tab">
            <div class="tab-item"><router-link :to="{ name: 'goods'}">商品</router-link></div>
            <div class="tab-item"><router-link :to="{ name: 'ratings'}">评论</router-link></div>
            <div class="tab-item"><router-link :to="{ name: 'seller'}">商家</router-link></div>
        </div>
        <router-view>

        </router-view>
    </div>
</template>

<script>
  import header from './components/header/header.vue';

  export default{
    components: {
      'v-header': header
    }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus">
    .tab
        display: flex
        width: 100%
        height: 40px
        line-height: 40px
        .tab-item
            flex: 1
            text-align: center
</style>
