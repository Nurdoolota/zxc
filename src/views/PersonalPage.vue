<template>
  <div class="courses">
    <form-button class="courses__button" @click="logOut" label="Выход" />
    <form-button
      class="courses__button"
      @click="$router.push({ name: 'courses' })"
      label="Мои курсы"
    />
    <form-button
      class="courses__button"
      @click="$router.push({ name: 'createcourse' })"
      label="Создать курс"
    />
  </div>
</template>

<script>
import FormButton from "@/components/FormButton.vue";

export default {
  components: {
    FormButton,
  },
};
</script>
