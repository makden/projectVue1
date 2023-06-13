<template>
  <div id="app">
    <myForm titleForm="Подписка на спам!" />
  </div>
</template>

<script>
import myForm from './components/myForm.vue';

export default {
  name: 'App', // В данном случаи роль не играет
  components: {
    myForm,
  },
};
</script>
