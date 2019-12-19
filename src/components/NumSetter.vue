<template>
  <div class='num-setter'>
    <label class='item'>{{ number }}</label>
    <input type='button' value='+' @click='add'/>
    <input type='button' value='-' @click='sub'/>
  </div>
</template>

<script>
  import { EventBus } from './EventBus'

  export default {
    name: 'NumSetter',
    data: function () {
      return {
          number: 0
      }
    },
    methods: {
      add: function () {
          EventBus.$emit('change', ++this.number)
      },
      sub: function () {
          EventBus.$emit('change', --this.number)
      }
    }
  }
</script>

<style scoped>
    .num-setter {
        border: 1px solid black;
        padding: 10px;
        width: 300px;
    }

    .item {
        margin: 0px 10px 0px 10px;
    }

    input[type='button'] {
        margin-right: 5px;
    }
</style>
