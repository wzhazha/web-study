<template>
  <div>
    <h1>登录页面</h1>
    <form @submit.prevent="login">
      <div>
        <label>用户名</label>
        <input type="text" v-model="username" />
      </div>
      <div>
        <label>密码</label>
        <input type="password" v-model="password" />
      </div>
      <button type="submit">登录</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    login() {
      fetch('http://localhost:8081/copy/mall/admin/login', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
        },
        body: JSON.stringify({
          username: this.username,
          password: this.password,
        })
      })
        .then(response => {
          if (response.ok) {
            alert("登录成功！");
            // 登录成功跳转页面
            this.$router.push("/");
          } else {
            alert("用户名或密码错误！");
          }
        })
        .catch(error => {
          console.log(error);
        });
    },
  },
};
</script>

<style scoped>

</style>
