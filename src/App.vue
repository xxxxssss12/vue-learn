<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
    </div>
    <router-view/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <span v-once>这个将不会改变: {{ message12 }}</span>
    <div v-html="message1" v-once></div>

    <input type="text" v-model="message1"/>
    <div id="components-demo">
      <!--<base-model-test v-model="lovingVue"></base-model-test>-->
      <ButtonCounter count="0"></ButtonCounter>
      <ButtonCounter count="0"></ButtonCounter>
      <ButtonCounter count="0"></ButtonCounter>
      <ButtonCounter count="0"></ButtonCounter>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ButtonCounter from "./components/ButtonCounter";

export default {
  name: 'app',
  data: function() {
    return { visible: false,
      message12:"test message",
      message1:"<h1 style='color: red'>test message</h1>",
      lovingVue:true
    }
  },
  components: {
      ButtonCounter,
      HelloWorld
  }
}

// Vue.component('base-model-test', {
//     model: {
//         prop: 'checked',
//         event: 'change'
//     },
//     props: {
//         checked: Boolean
//     },
//     template: `
//       <input
//         type="checkbox"
//         v-bind:checked="checked"
//         v-on:change="$emit('change', $event.target.checked)"
//       >
//     `
// })
// 定义一个名为 button-counter 的新组件
// Vue.component('button-counter', {
//     data: function () {
//         return {
//             count: 0
//         }
//     },
//     template: '<button v-on:click="count++">You clicked me {{ count }} times.</button>'
// })

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
