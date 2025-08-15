<template>
  <div>
    <header-one></header-one>
    <section-one></section-one>
  </div>
</template>

<script>
import header from './components/header.vue'
import section from './components/section.vue'

export default{
  data(){
    return{
    }
  },
  components:{
    "header-one":header,
    "section-one":section
  }
}
</script>
