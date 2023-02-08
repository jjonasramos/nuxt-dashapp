<template>
  <form ref="loginForm" class="flex flex-col gap-2 w-full" @submit.prevent="submit">
    <input 
      name="email"
      :value="email"
      type="email" 
      class="border border-gray-300 p-2 mb-2 rounded-lg focus:outline-none" 
      placeholder="E-mail" 
    />
    <input 
      type="password" 
      name="password"
      required
      :value="password"
      class="border border-gray-300 p-2 mb-2 rounded-lg focus:outline-none" 
      placeholder="Password" 
    />
    <Button type="submit" sx="bg-red-500" :is-submiting="isSubmitting" value="Sign In"></Button>
  </form>
</template>

<script>
  export default {
    el: 'LoginForm',
    data() {
      return {
        values: {
          email: {
            type: String,
            default: ''
          },
          password: {
            type: String,
            default: ''
          }
        },
        isSubmitting: false
      }
    },
    methods: {
      submit() {
        this.isSubmitting = true
        setTimeout(() => {
          this.isSubmitting = false
        }, 3000);
      }
    }
  }
</script>