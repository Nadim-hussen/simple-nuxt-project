<template>
    <SingleDataCard :singleData="singleValue" />
    <!-- <div>
        <h1>hello {{$route.params.id}}</h1>
    </div> -->
</template>
<script>
export default {

     data() {
    return {
      singleValue: '',
    };
  },
    async fetch() {
    this.singleValue = await fetch(
      `https://jsonplaceholder.typicode.com/posts/${this.$route.params.id}`
    ).then((res) => res.json());
  },

}
</script>