<template>
<div id="dog">
<button @click="img()"> choose a dog</button>
</div>
</template>


<script>

import {onMounted, onUnmounted, onUpdated } from "vue";

export default {
    
  setup() {
    onMounted(() => console.log("Mount: ✅ Game Component"));
    onUnmounted(() => console.log("unMount: 👋🏻 Game Component "));
    onUpdated(() => console.log("Updated: 🔥 Game Component"));

let imgEl = document.createElement("img");
function img() {
  imgEl.innerHTML = "";
    fetch("https://dog.ceo/api/breeds/image/random")
     .then(res =>  res.json())
      .then(img => img.message)
      .then((src) => {
       imgEl.src = src
       document.body.append(imgEl)
  })
}
let button = document.querySelector("button")
button.addEventListener("click", img);

    //     ref(()=>{
    //         img()
    //     })
    //   onMounted(()=>{
    //       img();
    //   })
    //    onUnmounted(()=>{
    //       img();
    //   })
    //   onUpdated(()=>{
    //   img();})
    return {img};
      },
};
</script>
<style>
.img{
    size: 400px;
    display:flex;
    flex-direction: column;
}
</style>