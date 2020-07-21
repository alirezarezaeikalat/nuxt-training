<template>
  <div class="container">
    <h1>this is the single user page {{$route.params.id}}</h1>

  </div>
</template>

<script>
export default {
  validate(data) {
    console.log(data)
    return /^\d+$/.test(data.params.id);
  }
}
</script>