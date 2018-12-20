<template>
  <div class="home">
    <div class="header">
      <p>Soart</p>
    </div>
    <ElementArray></ElementArray>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import ElementArray from '@/components/ElementArray.vue';

@Component({
  components: {
    ElementArray,
  },
})
export default class Home extends Vue {}
</script>

<style scoped lang="sass">

.home
  display: flex
  flex-flow: column nowrap
  justify-content: space-between
  height: 100%

  .header
    width: 100%
    text-align: center

    p
      font-size: 5em

</style>
