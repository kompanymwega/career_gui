<template>
  <b-row class="justify-content-md-center">
    <b-col cols="6">
      <b-form>
          <b-form-group id="fieldsetHorizontal"
                  horizontal
                  :label-cols="4"
                  breakpoint="md"
                  description="Email that you use.."
                  label="Enter your email"
                  label-for="inputHorizontal">
            <b-form-input id="inputHorizontal" v-model="user.email"></b-form-input>
          </b-form-group>
        <b-form-group id="fieldsetHorizontal"
                  horizontal
                  :label-cols="4"
                  breakpoint="md"
                  description="Input a strong password"
                  label="Enter your password"
                  label-for="inputHorizontal">
                  
          <b-form-input type="password" id="inputHorizontal" v-model="user.password"></b-form-input>
        </b-form-group>
        <button class="btn btn-primary" type="submit" @click="Login()">Login</button>
        <b-button type="button" variant="success" @click="$router.go(-1)">Cancel</b-button>
      </b-form>
    </b-col>
  </b-row>
</template>

<script>

import axios from 'axios'

export default {
  name: 'Login',
  data () {
    return {
      errors: [],
      user:{
        email:'',
        password:''
      }
    }
  },
  methods: {
    Login(){
      console.log("Congrats, "+this.user.email+" you're Logged in as a user.")
    }
  }
}
</script>