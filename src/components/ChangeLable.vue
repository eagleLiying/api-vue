<template>
  <div>
    <div v-if="loginType === 'username'">
      <label>Username</label>
      <input v-model="username" placeholder="Enter your username">
      <p>Username is: {{ username }}</p>
    </div>
    <div v-else>
      <label>Email</label>
      <input v-model="email" placeholder="Enter your email address">
      <p>Email is: {{ email }}</p>
    </div>
    <button @click="change">change</button>
    <button @click="submit">submit</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data: function() {
    return {
      loginType: "username",
      username: '',
      email: '',
    };
  },
  methods: {
      change: function() {
          if(this.loginType === 'username') {
              this.loginType = 'email'
          }else {
              this.loginType = 'username'
          }
      },
      submit: function() {
          alert(this.email);
      }
  }
};
</script>