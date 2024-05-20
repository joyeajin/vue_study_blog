<template>
  <div v-for="(data, i) in blogData" :key="i">
    <h5 @click="$router.push(`/detail/${data.number}`)">
      {{ data.title }}
    </h5>
    <p>{{ data.date }}</p>
  </div>
</template>
<script>
export default {
  name: "List-a",
  props: {
    blogData: Array,
  },
};
</script>
<style lang=""></style>
