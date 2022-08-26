<template>
  <div class="container">
    <div class="header">
      <h1 class="header__title">To do list</h1>
      <div class="header__add-task"><span class="header__icon"></span></div>
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
      <div class="task">
        <div class="content">
          <input type="checkbox" name="checkbox" id="checkbox">
          <p class="problem">TASK 01</p>
        </div>
        <div class="block-status">
          <p class="status">Выполнено</p>
          <p class="date">26.08.2022</p>
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
    color: #16191D;
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
    /*background: white;*/
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
  .subtext{
    /*padding: 0 0 0 20px;*/
  }
  .subtext-status{
    /*margin-right: 30px;*/
  }
  .sort{
    display: flex;
  }
  #checkbox{
    width: 20px;
    height: 20px;
    border: 1px solid #16191D;
  }
  .tasks{

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
</style>
