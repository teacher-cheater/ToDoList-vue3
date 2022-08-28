<!--<template>-->
<!--  <div class="create add-tasks-window " :show="false" >-->
<!--    <div  class="create__block">-->
<!--      <div class="create__content">-->
<!--        <h3 class="create__title">Создать новую задачу</h3>-->
<!--        <div-->
<!--            @click="closeModalWindow"-->
<!--            class="create__close"-->
<!--        >-->
<!--          <span class="create__close-icon"></span>-->
<!--        </div>-->
<!--      </div>-->
<!--          <create-form-tasks >-->
<!--            <slot></slot>-->
<!--          </create-form-tasks>-->
<!--        </div>-->
<!--      </div>-->
<!--      <slot></slot>-->
<!--</template>-->

<!--<script>-->
<!--import CreateFormTasks from "@/components/UI/CreateFormTasks";-->


<!--export default {-->
<!--  components:{CreateFormTasks},-->
<!--  name: 'add-tasks-window',-->
<!--  props: {-->
<!--    show: {-->
<!--      type: Boolean,-->
<!--      default: false,-->
<!--    }-->
<!--  }-->
<!--}-->
<!--</script>-->

<!--<style scoped>-->

<!--  .create{-->
<!--    width: 100%;-->
<!--    min-height: 100%;-->
<!--    background: rgba(255, 255, 255, 0.01);-->
<!--    backdrop-filter: blur(4px);-->
<!--    position: absolute;-->
<!--    display: flex;-->
<!--    justify-content: center;-->
<!--    align-items: center;-->
<!--    transform: translate(-50%);-->
<!--    left: 50%;-->
<!--    top: 0;-->
<!--    z-index: 2;-->

<!--    /*   _close-window" v-if="showModal" @close="showModal = true*/-->
<!--    /*  document.querySelector('.registration__back').addEventListener('click', () => document.querySelector('.registration').classList.toggle('reg-on-off'))*/-->
<!--  }-->
<!--  .create__block{-->
<!--    margin: 0 auto;-->
<!--    padding: 40px 40px 50px 40px;-->
<!--    background: #FFFFFF;-->
<!--    border: 1px solid #DDE2E4;-->
<!--    box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);-->
<!--    border-radius: 6px;-->
<!--    position: fixed;-->
<!--  }-->
<!--  .create__content{-->
<!--    display: flex;-->
<!--    justify-content: space-between;-->
<!--    margin-bottom: 30px;-->
<!--    width: 400px;-->
<!--  }-->
<!--  .create__title{-->
<!--    font-weight: 700;-->
<!--    font-size: 18px;-->
<!--    line-height: 132%;-->
<!--    color: #16191D;-->
<!--  }-->
<!--  .create__close{-->
<!--    background: #314B99;-->
<!--    border-radius: 5px;-->
<!--    width: 30px;-->
<!--    height: 30px;-->
<!--    position: relative;-->
<!--    cursor: pointer;-->
<!--  }-->
<!--  .create__close-icon{-->
<!--    background: #FFFFFF;-->
<!--    width: 18px;-->
<!--    height: 2px;-->
<!--    position: absolute;-->
<!--    top: 14px;-->
<!--    left: 6px;-->
<!--    transform: rotate(45deg);-->
<!--  }-->
<!--  .create__close-icon::before{-->
<!--    content: '';-->
<!--    transform: rotate(90deg);-->
<!--    background: #FFFFFF;-->
<!--    width: 18px;-->
<!--    height: 2px;-->
<!--    position: absolute;-->
<!--    top: 0;-->
<!--    left: 0;-->
<!--  }-->

<!--  .create__text{-->
<!--    font-weight: 400;-->
<!--    font-size: 14px;-->
<!--    line-height: 14px;-->
<!--    color: #16191D;-->
<!--    margin-bottom: 5px;-->
<!--  }-->
<!--  .create__task{-->
<!--    background: #FFFFFF;-->
<!--    border: 1px solid #DDE2E4;-->
<!--    border-radius: 8px;-->
<!--    width: 100%;-->
<!--    padding: 16px 11px;-->
<!--    color: #000000;-->
<!--    opacity: 0.5;-->
<!--    margin-bottom: 30px;-->
<!--  }-->
<!--  .create__btn{-->
<!--    display: flex;-->
<!--    background: #F0F5FF;-->
<!--    border-radius: 8px;-->
<!--    padding: 12px 40px;-->
<!--    font-weight: 400;-->
<!--    font-size: 18px;-->
<!--    line-height: 132%;-->
<!--    color: #314B99;-->
<!--    margin: 0 auto;-->
<!--    cursor: pointer;-->
<!--  }-->
<!--</style>-->