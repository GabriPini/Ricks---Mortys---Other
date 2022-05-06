<template>
 <div class="col-3">
  <img :src="character.image" alt="" />
  <h2>{{ character.name }}</h2>
  <div>{{ character.origin }}</div>
  <div>{{ character.species }}</div>
  <div v-if="character.status == 'unknown'" class="text-warning">{{ character.status }}</div>
  <div v-else-if="character.status == 'Alive'" class="text-success">{{ character.status }}</div>
  <div v-else-if="character.status == 'Dead'" class="text-danger">{{ character.status }}</div>
 </div>
</template>

<script>
export default {
 name: "CharacterComponent",
 props: {
  character: Object,
 },
};
</script>

<style>
</style>