<template>
  <div class="big-button d-flex justify-content-center" v-bind:style="{ width: btnWidth }">
    <p class="text-link">
      <span class="fa" v-bind:class="faName"></span>
      {{text}}
    </p>
  </div>
</template>

<script>
export default {
  props: [
    'faName',
    'text',
    'btnWidth'
  ]
}
</script>

<style scoped>
.big-button {
  padding: 10px 20px 0px;
  background-color: #2f56af;
  border: 1px solid #204599;
  font-size: 21px;
  color: white;
  width: 200px;
  box-sizing: border-box;
}
.text-link:link, .text-link:visited {
  text-decoration: none;
}
.text-link:hover {
  text-decoration: none;
}
</style>
