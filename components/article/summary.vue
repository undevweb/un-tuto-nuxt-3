<template>
  <div class="article">
    <h3><slot name="animal-name" /></h3>
    <p class="animal-infos">Taille : <slot name="animal-height" /> cm, Poids : <slot name="animal-weight" /> kg</p>
    <p><slot name="animal-description" /></p>
  </div>
</template>
<style scoped lang="css">
.article {
  width: 30%;
  padding: 15px;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

.article h3 {
  margin-top: 10px;
}

.animal-infos{
  background: #f4f4f4;
  border-radius: 15px;
  border: 1px solid #555555;
  padding: 4px;
  text-align: center;
  font-size: 9pt;
}
</style>
<script setup lang="ts">
</script>
