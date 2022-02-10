<template>
  <div class="data">
    <div v-if="data">
      <h2 class="title">
        {{ data.title }}&nbsp; &nbsp;
        <nuxt-link class="a" :to="`article/${data.id}`"
          ><span class="bold"> More details</span>
        </nuxt-link>
      </h2>
    </div>
  </div>
</template>
<script>
export default {
  props: ["data"],
  data(){
      return{

      }
  },
    methods: {

    }


};
</script>
<style scoped>
h2 {
  font-size: 16px;
}
.data {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.title {
  color: #0f403f;
  font-size: 17px;
  text-transform: capitalize;
  background-color: #78d1cf;
  padding: 5px;
}
.a{
  text-decoration: none;
}
.a:hover{
  text-decoration: underline;
}
.bold{
  font-weight: bold;
}
</style>