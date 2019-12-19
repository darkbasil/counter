<template>
    <div class='num-getter'>
        <label>{{ number }}</label>
    </div>
</template>

<script>
  import { EventBus } from './EventBus'
  export default {
    name: 'NumGetter',
    data: function () {
      return {
        number: 0
      }
    },
    created() {
      EventBus.$on('change', (num) => {
        this.number = num
      })
    }
  }
</script>

<style scoped>
    .num-getter {
        border: 1px solid black;
        padding: 10px;
        width: 300px;
        margin-top: 10px;
    }
</style>
