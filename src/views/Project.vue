<template>
  <div id="container"> 
        <img src="../assets/INTMarkus.jpg"/>
        <img src="../assets/potsandplants.jpg"/>
        <img src="../assets/doubleexp.png"/>
    </div>
</template>

<script>
export default {
  data: () => ({})
};
</script>

<style>

#container {
  display: flex;
  justify-content: center;
  width: 100%;
  flex-flow: row wrap;
}

img {
  height: 300px;
  margin: 30px;
}


</style>

