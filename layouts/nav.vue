<template>
  <div class="nav-wrapper">
    <nav class="nav">
      <ul>
        <li v-for="(item,index) in navList">
          <nuxt-link :to="item.path">{{item.name}}</nuxt-link>
        </li>
      </ul>
    </nav>
    <nuxt/>
  </div>
</template>
<script>
  export default{
    name: '',
    data() {
      return {
        navList: [
          { name: '首页', path: '/' },
          { name: '商品管理', path: '/commodity' },
          { name: '订单管理', path: '/order' },
          { name: '用户管理', path: '/user' }
        ]
      }
    },
    computed: {},
    methods: {}

  }
</script>
<style type="text/css">
  .nav-wrapper{
    display: flex;
  }
  nav{
    background: pink;
    color: #fff;
  }
  html {
    font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
                 Roboto, 'Helvetica Neue', Arial, sans-serif;
    font-size: 16px;
    word-spacing: 1px;
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%;
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    box-sizing: border-box;
  }

  *,
  *:before,
  *:after {
    box-sizing: border-box;
    margin: 0;
  }

  .button--green {
    display: inline-block;
    border-radius: 4px;
    border: 1px solid #3b8070;
    color: #3b8070;
    text-decoration: none;
    padding: 10px 30px;
  }

  .button--green:hover {
    color: #fff;
    background-color: #3b8070;
  }

  .button--grey {
    display: inline-block;
    border-radius: 4px;
    border: 1px solid #35495e;
    color: #35495e;
    text-decoration: none;
    padding: 10px 30px;
    margin-left: 15px;
  }

  .button--grey:hover {
    color: #fff;
    background-color: #35495e;
  }
</style>
