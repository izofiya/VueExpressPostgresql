<template>
  <div>
    <h1>Register</h1>
    <input type="email" name="email" placeholder="email" v-model="email"/>
    <br>
    <input type="password" name="password" placeholder="password" v-model="password"/>
    <br>
    <button @click="register">Register</button>
  </div>
</template>

<script>
/* eslint-disable */
import AuthenticationService from "@/services/AuthenticationService"

export default {
  data () {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    async register() {
      await AuthenticationService.register({
        email: this.email,
        password: this.password
      })
    }
  }
}
</script>

<style>
</style>

