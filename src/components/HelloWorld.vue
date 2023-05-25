<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <li>
      <a href="https://github.com/wzhazha" target="_blank">不知名菜鸟</a>
    </li>
    <p>
      点击这里进行
      <router-link to="/login">登录</router-link>
    </p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: '谁能教教我下一步怎么写'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
a {
  font-size: 16px;
}

a[target=_blank] {
  font-size: 20px;
}
</style>
