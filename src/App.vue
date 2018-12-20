<!-- Basic App Component -->
<!-- Provides a basic nav bar and renders the router view -->
<!-- Also defines global styles -->

<template>
  <div id="app">
    <!-- 
    <div id="nav">
      <router-link to="/">Home</router-link> |
    </div>
    -->
    <router-view/>
  </div>
</template>


<style lang="sass">

@import url('https://fonts.googleapis.com/css?family=Raleway:300,400')

*
  margin: 0
  padding: 0

html, body
  width: 100%
  height: 100%

body
  font-family: 'Raleway', sans-serif
  font-weight: 300


#app
  display: flex
  flex-flow: column nowrap
  height: 100%

</style>
