<template>
  <div class="container">
    <div class="header">
      <h1 class="header__title">To do list</h1>
      <div class="header__add-task">+</div>
    </div>
    <div class="search">
      <input class="search__text" type="text" placeholder="Поиск Имени, статуса или даты"/>
      <p class="search__sort">Сортировать по:</p>
    </div>
    <div class="text">
      <p class="subtext">Описание</p>
      <div class="sort">
        <p class="subtext">Статус</p>
        <p class="subtext">Дата</p>
      </div>
      </div>
    <div class="tasks">
      <div class="task">
        <input type="checkbox" name="checkbox" id="checkbox">
        <p class="problem">TASK 01</p>
        <div class="block-status">
          <p class="status">Выполнено</p>
          <p class="date">Дата</p>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
export default {

}
</script>

<style scoped>
  .container{
    max-width: 1330px;
    padding: 0 15px;
    margin: 0 auto;
  }
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
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
    background-color: dimgray;
  }
  .search{
    padding: 10px 40px;
    display: flex;
    justify-content: space-between;
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
    /*background: white;*/
  }

  .text{
    display: flex;
    justify-content: space-between;
    padding: 10px 40px;

  }
  .subtext{
    font-weight: 400;
    font-size: 14px;
    line-height: 132%;
    color: #16191D;
    border-left: 1px solid #C4C4C4;
    padding: 0 20px;
  }
  .sort{
    display: flex;
  }
  #checkbox{

  }
  .tasks{
    /*display: flex;*/
  }
  .task{
    display: flex;
    padding: 20px 40px;
    gap: 20px;
    border-bottom: 1px solid #C4C4C4;
    border-top: 1px solid #C4C4C4;
  }
  .problem{

  }

</style>
