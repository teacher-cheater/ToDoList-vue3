
<!--<template>-->
<!--  <form-->
<!--      class="create__items"-->
<!--      @submit.prevent-->
<!--  >-->
<!--    <p  class="create__text">Описание</p>-->
<!--    <input-->
<!--        type="text"-->
<!--        class="create__task"-->
<!--        v-bind:value="title"-->
<!--        @input="inputTitle"-->
<!--    />-->
<!--    <button-->
<!--        class="create__btn"-->
<!--        @click="addTask"-->
<!--    >-->
<!--      Создать-->
<!--    </button>-->
<!--  </form>-->
<!--</template>-->

<!--<script>-->
<!--export default {-->
<!--  // name: 'create-form-window',-->
<!--methods:{-->
<!--  addTask(){-->
<!--    const newTask = {-->
<!--      id: Date.now(),-->
<!--      title: this.title,-->
<!--      body: this.status,-->
<!--      date: this.date-->
<!--    }-->
<!--    this.tasks.push(newTask);-->
<!--    this.title = '';-->
<!--    this.body = 'working';-->
<!--    this.date = String(new Date()-->
<!--        .getDate()).padStart(2, '0') + '.' + String(new Date()-->
<!--        .getMonth() + 1).padStart(2, '0') + '.' + new Date().getFullYear();-->
<!--  },-->
<!--  inputTitle(event){-->
<!--    this.title = event.target.value;-->
<!--  },-->
<!--}-->
<!--}-->
<!--</script>-->

<!--<style scoped>-->

<!--</style>-->