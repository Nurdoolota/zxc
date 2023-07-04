<template>
  <div>
    <input v-model="nameInput" placeholder="Название компонента" />
    <input v-model="descriptionInput" placeholder="Описание компонента" />
    <button @click="addComponent">Добавить компонент</button>

    <div v-for="(component, index) in components" :key="index">
      <h2>{{ component.name }}</h2>
      <p>{{ component.description }}</p>
    </div>
    <form-button
      class="courses__button"
      @click="$router.push({ name: 'courses' })"
      label="Мои курсы"
    />
  </div>
</template>

<script>
export default {
  // import FormButton from "@/components/FormButton.vue";

  // import CourseElement from "@/components/CourseElement.vue";
  methods: {
    addComponent() {
      const name = this.nameInput;
      const description = this.descriptionInput;

      this.components.push({ name, description });
    },
  },
};
</script>
