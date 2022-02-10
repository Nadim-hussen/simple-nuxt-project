<template>
    <div class="card" style="width: 18rem;">

  <div class="card-body">
    <h5 class="card-title">{{singleData.title}}</h5>
    <p class="card-text">
      {{singleData.body}}
    </p>
    <div class="center-btn">
    <NuxtLink to="/" class="btn">Go Back</NuxtLink>
    </div>
  </div>
</div>
</template>
<script>
export default {
  props: ["singleData"],
}
</script>
<style scoped>
.card{
  background-color: #a2a2a2;
  padding: 5px 8px;
  margin: 10px auto;
}
.card-title{
  font-size: 18px;
  text-align: center;
  text-transform: capitalize;

}
.card-text{
  font-size: 15px;
  text-align: justify;
  text-transform: capitalize;
}
.btn{
  text-decoration: none;
  text-transform: capitalize;
  background-color: #00584e;
  color: #fff;
  padding: 4px;
  margin: 0 auto;
}
.center-btn{
  display: flex;
  justify-content: center;
}
.card-body{
  padding: 5px;
}
</style>