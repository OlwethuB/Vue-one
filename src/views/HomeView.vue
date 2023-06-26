<template>
  <p>
    <span :title="message"> Hover and see the dynamic title</span>
  </p>
  <p :class="{ red: isRed }" @click="toggleRed">
    This should be red... but click me to toggle
  </p>
  <p :style="{ color }" @click="toggleColor">
    This will change colour when clicking
  </p>
</template>

<style>
  .red {
    color: red
  }
</style>
<script>



export default{
  data(){
    return{
      message:"Ayyyyeeee !",
      isRed: true,
      color: 'green'
    }
  },
  methods: {
    toggleRed(){
      this.isRed=!this.isRed
    },
    toggleColor(){
      this.color= this.color=== 'green'? 'blue':'green'
    }
  },


}


</script>
