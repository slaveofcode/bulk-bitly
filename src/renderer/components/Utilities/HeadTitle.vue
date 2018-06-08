<template>
  <div>
    <p class="col-title">
      <span class="fa" v-bind:class="faName"></span>
      {{title}}
    </p>
  </div>
</template>

<script>
export default {
  props: [
    'faName',
    'title'
  ]
}
</script>

<style>
.col-title {
  font-size: 18px;
  color: #2f56af;
}
.fa {
  margin-right: 5px;
  font-size: 17px;
}
</style>
