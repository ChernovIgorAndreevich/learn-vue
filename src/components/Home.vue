<template>
  <div class="container">
    <div class="container-item">
      <div v-bind:class="{'form-error': $v.login.$invalid}">
        Login: <input v-model="login">
      </div>
      <div>
        Password: <input v-model="password">
      </div>
    <button v-bind:disabled="$v.login.$invalid"
      @click="onSubmit">Submit</button>
    </div>
  </div>
</template>

<script>
import { required, numeric } from 'vuelidate/lib/validators'
export default {
  name: 'HelloWorld',
  data () {
    return {
      login: '',
      password: ''
    }
  },
  methods: {
    onSubmit (event) {
      console.log(123, this.login, this.password)
    }
  },
  validations () {
    return {
      login: {
        required,
        numeric
      }
    }
  }
}
</script>

<style scoped lang="scss">
.form-error {
    color: red;
  }
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    .container-item {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      input {
        margin: 10px;
      }
    }
  }
</style>
