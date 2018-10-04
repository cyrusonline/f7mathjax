<template>
  <f7-page>
    <f7-navbar sliding title="Home"></f7-navbar>
    <f7-block-title>{{ title }}</f7-block-title>
    <f7-block inner>
      <p>
  When \(a \ne 0\), there are two solutions to \(ax^2 + bx + c = 0\) and they are
  $$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$
</p>
     <textarea v-model="formula" cols="30" rows="10"></textarea>
  <vue-mathjax :formula="formula"></vue-mathjax>
  
   Lorem ipsum dolor sit amet, consectetur adipisicing elit.
      Distinctio est aliquam officiis quaerat placeat, cum explicabo magni
      soluta totam maxime autem minima accusamus eos suscipit dignissimos
      corporis modi voluptatum fugiat!
    </f7-block>
  </f7-page>
</template>
<script>
import { VueMathjax } from 'vue-mathjax'
import mathjax from 'mathjax';
export default {
  name: 'Home',
  components: {
    'vue-mathjax': VueMathjax
  },
  data() {
    return {
      title: 'Hello World',
      formula: '$$x = {-b \\pm \\sqrt{b^2-4ac} \\over 2a}.$$',
      msg: 'Welcome to Your Vue.js App'
    };
  }
};
</script>
