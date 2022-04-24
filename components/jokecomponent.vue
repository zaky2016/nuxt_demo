<template>
  <div class="joke">
      <p :id=id> {{joke}}</p>
      <hr>
  </div>
</template>

<script>
export default {
name : 'jokecomponent',
props: ['joke', 'id']
}
</script>

<style>

</style>