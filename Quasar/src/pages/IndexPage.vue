<template>
  <q-page class="flex flex-center">
    <div class="q-ma-sm">
      <q-card class="my-card q-mb-sm text-grey-1" v-for="data in data" :key="data.id">
        <q-card-section>
          <div class="text-h6">{{ data.title }}</div>
          <div class="text-subtitle2">{{ data.subtitle }}</div>
        </q-card-section>
        <q-card-section> {{ data.id }} {{ data.name }} </q-card-section>
      </q-card>
    </div>
  </q-page>
</template>

<script setup>
defineProps({
  message: String,
});

const data = [
  {
    id: 1,
    title: "Title",
    subtitle: "Subtitle",
    name:
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi sed, laboriosam voluptatum enim voluptatibus distinctio tempore odit, corporis provident, eum necessitatibus repudiandae repellat beatae incidunt aut ipsa perferendis. Aliquid, officia. ",
  },
  {
    id: 2,
    title: "Title",
    subtitle: "Subtitle",
    name:
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi sed, laboriosam voluptatum enim voluptatibus distinctio tempore odit, corporis provident, eum necessitatibus repudiandae repellat beatae incidunt aut ipsa perferendis. Aliquid, officia.",
  },
  {
    id: 3,
    title: "Title",
    subtitle: "Subtitle",
    name:
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi sed, laboriosam voluptatum enim voluptatibus distinctio tempore odit, corporis provident, eum necessitatibus repudiandae repellat beatae incidunt aut ipsa perferendis. Aliquid, officia.",
  },
  {
    id: 3,
    title: "Title",
    subtitle: "Subtitle",
    name:
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi sed, laboriosam voluptatum enim voluptatibus distinctio tempore odit, corporis provident, eum necessitatibus repudiandae repellat beatae incidunt aut ipsa perferendis. Aliquid, officia.",
  },
];
</script>

<style scoped>
.my-card {
  background-color: blueviolet;
}
</style>
