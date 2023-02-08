<template>
  <button 
    :type="type" 
    class="p-2 rounded-lg text-white hover:bg-blue-600 transition-all ease-linear duration-200 font-bold"
    :class="{ 'bg-blue-500': !isSubmitting, 'bg-gray-500': isSubmitting }"
  >
    <!-- show current value of isSubmitting -->
    {{ isSubmitting ? 'Loading...' : value }}
  </button>
</template> 

<script>
  export default {
    props: {
      type: {
        type: String,
        default: 'button'
      },
      isSubmitting: {
        type: Boolean,
        default: false
      },
      value: {
        type: String,
        default: ''
      }
    }
  }
</script>