<template>
  <section id="latest-articles">
    <h2>Derniers Articles</h2>
    <div class="articles-grid">

      <ArticleSummary>
        <template #animal-name>L’Axolotl : Le Monstre d'Eau Mexicain</template>
        <template #animal-height>15-30</template>
        <template #animal-weight>60-200</template>
        <template #animal-description>
          Découvrez cet amphibien unique capable de régénérer ses membres.
        </template>
      </ArticleSummary>

      <ArticleSummary>
        <template #animal-name>Le Quokka : L'animal le plus heureux du monde</template>
        <template #animal-height>40-54</template>
        <template #animal-weight>2,5-5</template>
        <template #animal-description>
          Explorez la vie du quokka, célèbre pour son sourire irrésistible.
        </template>
      </ArticleSummary>

      <ArticleSummary>
        <template #animal-name>Le Capybara : Le plus grand rongeur de la planète</template>
        <template #animal-height>100-130</template>
        <template #animal-weight>35-65</template>
        <template #animal-description>
          Plongez dans l'univers du capybara, ce rongeur géant d'Amérique du Sud.
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

section p {
  color: #555;
  line-height: 1.6;
}

.articles-grid {
  display: flex;
  justify-content: space-between;
}
</style>
