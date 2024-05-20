<template lang="">
  <!-- <p>{{ $route.params.id }}</p> -->
  <div>
    <h4>상세페이지</h4>
    <h5>{{ blogData[$route.params.id].title }}</h5>
    <p>{{ blogData[$route.params.id].content }}</p>
    <router-view></router-view>
  </div>
</template>
<script>
export default {
  name: "Detail-a",
  props: {
    blogData: Array,
  },
};
</script>
<style lang=""></style>
