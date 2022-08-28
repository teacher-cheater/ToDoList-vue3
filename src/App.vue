<template>
  <div class="container _active">
    <div class="header">
      <h1 class="header__title">To do list</h1>
      <button
          class="header__add-task"
          @click="showDialog"
      >
        <span class="header__icon"></span>
      </button>
    </div>
    <div class="search">
      <div class="search__content">
        <img src="./icons/search.svg" alt="search">
        <input class="search__text" type="text" placeholder="Поиск Имени, статуса или даты"/>
      </div>
      <p class="search__sort">Сортировать по: <span>date</span></p>
    </div>
    <div class="text">
      <p class="subtext">Описание</p>
      <div class="sort">
        <p class="subtext-status">Статус</p>
        <p class="subtext-date">Дата</p>
      </div>
      </div>
    <div class="tasks">
      <div class="task" v-for="task in tasks">
        <div class="content" >
          <input type="checkbox" name="checkbox" id="checkbox">
          <p class="problem">{{ task.title }}</p>
        </div>
        <div class="block-status">
          <p class="status">{{task.body}}</p>
          <p class="date">{{ date }}</p>
        </div>
      </div>
    </div>
<!--    <add-tasks-window v-for="task in tasks" :task="task">-->

<!--    </add-tasks-window>-->
    <add-tasks-window v-model:show="dialogVisible" >
    <div class="create add-tasks-window " v-if:show="false" >
      <div  class="create__block">
        <div class="create__content">
          <h3 class="create__title">Создать новую задачу</h3>
          <button

              @click="closeModalWindow"
              class="create__close"
          >
            <span class="create__close-icon"></span>
          </button>
        </div>
        <form
            class="create__items"
            @submit.prevent
        >
          <p class="create__text">Описание</p>
          <input
              type="text"
              class="create__task"
              v-bind:value="title"
              @input="inputTitle"
          />
          <button
              class="create__btn"
              @click="addTask"
          >
            Создать
          </button>
        </form>
      </div>
    </div>
    </add-tasks-window>
  </div>

</template>

<script>
// import AddTasksWindow from "@/components/UI/AddTasksWindow";
export default {
  // components: {AddTasksWindow},
  data(){
    return{
      tasks:[
        {id:1, title: 'My first task', body: 'Выполнено', date: '27.08.2022'}
      ],
      title: '',
      body: '',
      date: '',
      dialogVisible: false,
    }
  },
  methods:{
    addTask(){
      const newTask = {
        id: Date.now(),
        title: this.title,
        body: this.status,
        date: this.date
      }
      this.tasks.push(newTask);
      this.title = '';
      this.body = 'working';
      this.date = String(new Date()
          .getDate()).padStart(2, '0') + '.' + String(new Date()
          .getMonth() + 1).padStart(2, '0') + '.' + new Date().getFullYear();
    },
    inputTitle(event){
      this.title = event.target.value;
    },
    closeModalWindow(){
      this.$emit('update:show', false)
      this.dialogVisible = false;
    },
    showDialog(){
      this.dialogVisible = true;
    },
    name: 'add-tasks-window',
      show: {
        type: Boolean,
        default: false,
      },

    // hideDialog(){
    //   this.$emit('update:show', false)
  }
    // taskCreateOnWindow(){
    //   showModal: false;
    // }

}
</script>

<style scoped>
  .container{
    max-width: 1330px;
    padding: 0 15px;
    margin: 0 auto;
    color: #16191D;
  }
  *{
    margin: 0;
    padding: 0;
    border: 0;
    box-sizing: border-box;
  }
  ._active{
    /*background: rgba(255, 255, 255, 0.01);*/
    /*backdrop-filter: blur(4px);*/
  }
  ._close-window{
    /*display: none;*/
  }
  ._open-window{
    display: block;
  }
  .header{
    display: flex;
    justify-content: space-between;
    padding: 10px 40px;
  }
  .header__title{
    font-weight: 700;
    font-size: 24px;
    line-height: 132%;
    color: #16191D;
  }
  .header__add-task{
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background: #D6DBEB;
    position: relative;
    cursor: pointer;
  }
  .header__icon{
    background: #314B99;
    width: 20px;
    height: 2px;
    position: absolute;
    top: 18px;
    left: 10px;
  }
  .header__icon::before{
    content: '';
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    width: 20px;
    height: 2px;
    background: #314B99;
    transform: rotate(90deg);
  }
  .search{
    padding: 10px 40px;
    display: flex;
    justify-content: space-between;
  }
  .search__content{
    display: flex;
    gap: 16px;
  }
  input:active, :hover, :focus {
       outline: 0;
       outline-offset: 0;
  }
  .search__text{
    width: 100%;
    max-width: 300px;
    font-weight: 400;
    font-size: 14px;
    line-height: 132%;
    color: #C4C4C4;
  }

  .text{
    display: flex;
    justify-content: space-between;
    padding: 10px 40px 10px 50px;
  }
  .subtext-status,
  .subtext-date,
  .subtext{
    font-weight: 400;
    font-size: 14px;
    line-height: 132%;
    color: #16191D;
    border-left: 1px solid #C4C4C4;
    padding: 0 0 0 20px;
    width: 150px;
  }

  .sort{
    display: flex;
  }
  #checkbox{
    width: 20px;
    height: 20px;
    border: 1px solid #16191D;
  }

  .task{
    display: flex;
    justify-content: space-between;
    padding: 20px 40px;
    border-bottom: 1px solid #C4C4C4;
    border-top: 1px solid #C4C4C4;
  }

  .block-status{
    display: flex;
  }
  .content{
    display: flex;
    justify-content: space-between;
  }
  .problem{
    font-weight: 400;
    font-size: 14px;
    line-height: 132%;
    color: #16191D;
    padding: 0 20px;
  }
  .status{
    font-weight: 400;
    font-size: 14px;
    line-height: 132%;
    padding: 0 0 0 20px;
    width: 150px;
    color: #134EC1;
  }
  .date{
    font-weight: 400;
    font-size: 14px;
    line-height: 132%;
    color: #16191D;
    padding: 0 0 0 20px;
    width: 150px;
  }
  .tasks-window{
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(255, 255, 255, 0.01);
    backdrop-filter: blur(4px);
    position: fixed;
    display: flex;
  }
  .tasks-window__content{
    margin: auto;
    padding: 40px 40px 50px 40px;
    background: #FFFFFF;
    border: 1px solid #DDE2E4;
    box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
    border-radius: 6px;
    min-width: 400px;
  }
  .create{
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(255, 255, 255, 0.01);
    backdrop-filter: blur(4px);
    position: fixed;
    display: flex;

    /*   _close-window" v-if="showModal" @close="showModal = true*/
    /*  document.querySelector('.registration__back').addEventListener('click', () => document.querySelector('.registration').classList.toggle('reg-on-off'))*/
  }
  .create__block{
    margin: auto;
    padding: 40px 40px 50px 40px;
    background: #FFFFFF;
    border: 1px solid #DDE2E4;
    box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
    border-radius: 6px;
    min-width: 400px;
  }
  .create__content{
    display: flex;
    justify-content: space-between;
    margin-bottom: 30px;
    width: 400px;
  }
  .create__title{
    font-weight: 700;
    font-size: 18px;
    line-height: 132%;
    color: #16191D;
  }
  .create__close{
    background: #314B99;
    border-radius: 5px;
    width: 30px;
    height: 30px;
    position: relative;
    cursor: pointer;
  }
  .create__close-icon{
    background: #FFFFFF;
    width: 18px;
    height: 2px;
    position: absolute;
    top: 14px;
    left: 6px;
    transform: rotate(45deg);
  }
  .create__close-icon::before{
    content: '';
    transform: rotate(90deg);
    background: #FFFFFF;
    width: 18px;
    height: 2px;
    position: absolute;
    top: 0;
    left: 0;
  }

  .create__text{
    font-weight: 400;
    font-size: 14px;
    line-height: 14px;
    color: #16191D;
    margin-bottom: 5px;
  }
  .create__task{
    background: #FFFFFF;
    border: 1px solid #DDE2E4;
    border-radius: 8px;
    width: 100%;
    padding: 16px 11px;
    color: #000000;
    opacity: 0.5;
    margin-bottom: 30px;
  }
  .create__btn{
    display: flex;
    background: #F0F5FF;
    border-radius: 8px;
    padding: 12px 40px;
    font-weight: 400;
    font-size: 18px;
    line-height: 132%;
    color: #314B99;
    margin: 0 auto;
    cursor: pointer;
  }

</style>
