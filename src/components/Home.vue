<template>
  <div class="conteiner">
    <div class="conteiner-item">
      Login<input v-model="login">
      password<input v-model="password" type="password">
      <button v-on:click="onSubmit">кнопкааааааа</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      login: '',
      password: ''
    }
  },
  methods: {
    onSubmit () {
    }
  }
}

</script>
