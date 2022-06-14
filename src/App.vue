<template>
  <div>{{ greet }} {{ name }} Welcome to {{ Channel }} </div>
  <div v-text="Channel"></div>
  <div v-html="bold"></div>
  <div v-html="hack"></div>
  <div v-bind:id="headingId">heading demo for id (do inspect bro)</div>
  <button v-bind:disabled="isDisabled">hii</button>
  <h2 class="underline"> Underline</h2>
  <h2 v-bind:class="status">status</h2>
  <h2 v-bind:class="isPromoed && 'promoted'">Promoted business</h2>
  <h2 v-bind:class="isSoldout ? 'sold-out' : 'new' ">is soldout</h2>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      greet: "Hello",
      name: "Joyin mahmmad",
      Channel: "Codevoluiton",
      bold: "<b>Text Bold</b>",
      hack: `<a href="#" onclick="alert('You Have Been Hacked')">Cick to Hack</a>`,
      headingId: 'heading',
      isDisabled: false,
      status: 'danger',
      isPromoed: true,
      isSoldout: false, 
    };
  },

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.underline {
  text-decoration: underline;
}
.promoted{
  font-style:italic;
}
.new{
  color: green;
}
.sold-out{
  color: red;
}
</style>
