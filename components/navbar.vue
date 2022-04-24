<template>
  <div>
      <div class="head">
          <div class="logo">
              DadJokes
          </div>
          <div class="menu">
              <nuxt-link class="item" to="/">home</nuxt-link>
              <nuxt-link class="item" to="/joke">joke</nuxt-link>
              <nuxt-link class="item" to="/about">about</nuxt-link>
          </div>

      </div>
      <hr>
  </div>
</template>

<script>
export default {
 name : "NavBar"
}
</script>

<style>
.head{
    display: flex;
    justify-content: space-between;
    padding-right: 5%;
    padding-left: 5%;
}
.logo{
    color: #526488;
    font-size: 25px;
}
.menu{
    display: flex;
    align-content: space-between;
}
.item {
    display: inline-block;
    padding: 0.3rem 1rem;
    margin-right: 0.5rem;
    background: black;
    color: white;
    text-decoration: none;
}
</style>