<template>
  <section id="featured-articles">
    <h2>Articles en vedette</h2>
    <div class="articles-grid">

      <ArticleSummary>
        <template #animal-name>Le Narval : La Licorne des Mers</template>
        <template #animal-height>400-500</template>
        <template #animal-weight>800-1 600</template>
        <template #animal-description>
          Découvrez le narval, cet étonnant cétacé vivant dans les eaux glacées de l'Arctique.
        </template>
      </ArticleSummary>

      <ArticleSummary>
        <template #animal-name>Le Fennec : Renard du Désert</template>
        <template #animal-height>35-40</template>
        <template #animal-weight>1-1,5</template>
        <template #animal-description>
          Explorez la vie fascinante du fennec, un animal parfaitement adapté aux conditions désertiques.
        </template>
      </ArticleSummary>

      <ArticleSummary>
        <template #animal-name>Le Panda Roux : Une Espèce en Danger</template>
        <template #animal-height>50-65</template>
        <template #animal-weight>3-6</template>
        <template #animal-description>
          Apprenez-en plus sur ce charmant mammifère vivant dans les montagnes asiatiques.
        </template>
      </ArticleSummary>

    </div>
  </section>
</template>
<script setup lang="ts">
</script>
<style scoped lang="css">
section {
  margin: 20px 0;
  padding: 20px;
  background-color: white;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

section h2 {
  color: #333;
  margin-bottom: 10px;
}

.articles-grid {
  display: flex;
  justify-content: space-between;
}
</style>

