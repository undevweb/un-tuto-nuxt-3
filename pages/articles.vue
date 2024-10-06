<template>
  <div id="articles">
    <h1>Articles (Total : {{ articles.length }} )</h1>

    <div class="articles-grid">
      <ArticleSummary v-for="animal of articles" :key="`animal-${animal.name}`">
        <template #animal-name>{{ animal.name }} ({{ animal.name.length }} lettres) <span v-if="isTall" class="badge">Grand</span></template>
        <template #animal-height>{{ animal.height }}</template>
        <template #animal-weight>{{ animal.weight }}</template>
        <template #animal-description>{{ animal.description }}</template>
      </ArticleSummary>
    </div>

    <h1>Ajouter un article</h1>

    <ArticleSummary v-if="animal.name">
      <template #animal-name>{{ animal.name }} ({{ animal.name.length }} lettres) <span v-if="isTall" class="badge">Grand</span></template>
      <template #animal-height>{{ animal.height }}</template>
      <template #animal-weight>{{ animal.weight }}</template>
      <template #animal-description>{{ animal.description }}</template>
    </ArticleSummary>

    <form id="form-article-update">
      <p>
        <label for="name">Nom : </label>
        <input id="name" v-model="animal.name" width="400">
      </p>
      <p>
        <label for="height">Hauteur : </label>
        <input type="number" id="height" v-model="animal.height" min="0"></input>
      </p>
      <p>
        <label for="weight">Poids : </label>
        <input type="number" id="weight" v-model="animal.weight" min="0"></input>
      </p>
      <p>
        <label for="description">Description : </label>
        <textarea id="description" v-model="animal.description" cols="100" rows="5"></textarea>
      </p>
    </form>

    <a href="/">Revenir à l'accueil</a>
  </div>
</template>
<script setup lang="ts">
import type {AnimalInterface} from '~/utils/interfaces/animal.interface';

const nbArticles = ref(1);
const animal = ref<AnimalInterface>({
  name: "",
  description: ""
});
const isTall = computed(() => animal.value.height && animal.value.height > 200);
const articles = ref<AnimalInterface[]>([
  {
    name: "Le Fennec : Renard du Désert",
    height: 35,
    weight : 1,
    description: "Le fennec est un petit renard vivant dans les déserts d'Afrique du Nord. Il est facilement identifiable grâce à ses grandes oreilles, qui lui permettent de réguler la température de son corps et d’entendre les proies se déplacer sous le sable. Ce nocturne est parfaitement adapté à son environnement aride : il peut survivre de longues périodes sans boire d’eau, car il obtient toute l’humidité nécessaire de la nourriture qu'il consomme, comme des insectes, des rongeurs et des plantes."
  },
  {
    name: "Le Panda Roux : Une Espèce en Danger",
    height: 60,
    weight : 4.5,
    description: "Le panda roux est un petit mammifère vivant dans les forêts montagneuses de l'Himalaya et du sud-ouest de la Chine. Bien qu’il partage une partie de son nom avec le panda géant, ces deux espèces ne sont pas étroitement liées. Le panda roux est un grimpeur agile et passe une grande partie de son temps dans les arbres, où il mange principalement des bambous, mais aussi des fruits, des insectes et des œufs. Avec son pelage roux et sa queue touffue, il est extrêmement mignon, mais aussi menacé par la déforestation."
  },
  {
    name: "L’Axolotl : Le petit monstre tout mignon d'Eau Mexicain",
    height: 17.5,
    weight : 0.130,
    description: "L'axolotl est un amphibien originaire des lacs du Mexique, principalement le lac Xochimilco. Ce petit animal est fascinant pour sa capacité à régénérer ses membres, ses organes et même des parties de son cerveau. Contrairement à la plupart des amphibiens, l'axolotl reste à l’état larvaire toute sa vie, conservant ses branchies externes et vivant exclusivement sous l'eau. Il se nourrit de petits poissons, de vers et d'insectes aquatiques. Cependant, à cause de la pollution et de la destruction de son habitat, il est aujourd'hui gravement menacé."
  }
]);
</script>
<style scoped lang="css">
.badge{
  background: #4CAF50;
  font-weight: bold;
  border-radius: 15px;
  border: 1px solid #555555;
  padding: 4px;
  text-align: center;
  font-size: 9pt;
}

.articles-grid {
  display: flex;
  justify-content: space-between;
}
</style>
