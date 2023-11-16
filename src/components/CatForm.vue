<template>
  <form @submit.prevent="createCat">
    <input type="text">
    <button type="submit">Submit</button>
  </form>
</template>


<script>
import { logger } from '../utils/Logger.js';

export default {
  setup() {
    return {
      createCat() {
        logger.log('CREATING CAT')
      }
    }
  }
}
</script>


<style lang="scss" scoped></style>