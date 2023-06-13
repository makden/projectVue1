<template>
  <div id="myForm">
    <div>{{ titleForm }}</div>
    <form action="" @submit.prevent>
      <label for="user">Имя: </label>
      <input v-model="user" type="text" id="user" /><br />
      <label for="email">E-mail: </label>
      <input v-model="email" type="text" id="email" /><br /><br />
      <input type="submit" value="Подписаться" />
    </form>
  </div>
</template>

<script>
export default {
  //name: 'HelloWorlds',
  props: {
    titleForm: String,
    user: String,
  },
  data() {
    return {
      user: '1',
      email: '2',
    };
  },
  methods: {
    submit(e) {
      this.user = e.target.value;
    },
  },
};
</script>

<style scoped>
label {
  width: 100px;
  display: inline-block;
  text-align: right;
  padding-right: 5px;
}

#myForm {
  margin: 20px auto;
  width: max-content;
  padding: 10px;
  border: solid 1px #aaa;
}

#myForm > div {
  text-align: center;
  margin-bottom: 10px;
}
</style>
