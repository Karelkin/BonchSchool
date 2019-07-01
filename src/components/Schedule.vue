<template>
  <div class='schedule' id='schedule'>
    <div class="container">
      <div class="row">
        <div class="col-xl-11 offset-xl-1 schedule__title">
          <h2>Расписание школы 2019</h2>
        </div>
      </div>
      <div class="row">
        <div class="col-xl-8 offset-xl-2 schedule__list">
          <ul>
            <li class='item-1'>
              <h4>Регистрация участников 1-27 сентября</h4>
              <p>Команды 3-5 человек. В команде должно быть хотя бы двое участников, владеющих хотя бы одним промышленным языком программирования (Python, Ruby, JavaScript, C/C#/C++/Java/PHP и подобные — не Pascal и не Basic).</p>
            </li>
            <li class='item-2'>
              <h4>Отбор заявок до 1 октября</h4>
              <p>Организаторы и эксперты, рассмотрев все заявки, определяют команды, прошедшие на следующий этап.</p>
            </li>
            <li class='item-3'>
              <h4>Регистрация участников 1-27 сентября</h4>
              <p>Команды 3-5 человек. В команде должно быть хотя бы двое участников, владеющих хотя бы одним промышленным языком программирования (Python, Ruby, JavaScript, C/C#/C++/Java/PHP и подобные — не Pascal и не Basic).</p>
            </li>
            <li class='item-4'>
              <h4>Регистрация участников 1-27 сентября</h4>
              <p>Команды 3-5 человек. В команде должно быть хотя бы двое участников, владеющих хотя бы одним промышленным языком программирования (Python, Ruby, JavaScript, C/C#/C++/Java/PHP и подобные — не Pascal и не Basic).</p>
            </li>
            <li class='item-5'>
              <h4>Регистрация участников 1-27 сентября</h4>
              <p>Команды 3-5 человек. В команде должно быть хотя бы двое участников, владеющих хотя бы одним промышленным языком программирования (Python, Ruby, JavaScript, C/C#/C++/Java/PHP и подобные — не Pascal и не Basic).</p>
            </li>
            <li class='item-6'>
              <h4>Регистрация участников 1-27 сентября</h4>
              <p>Команды 3-5 человек. В команде должно быть хотя бы двое участников, владеющих хотя бы одним промышленным языком программирования (Python, Ruby, JavaScript, C/C#/C++/Java/PHP и подобные — не Pascal и не Basic).</p>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  
</script>

<style lang='scss' scoped>
.schedule{
  padding-top: 130px;
  padding-bottom: 110px;
}
.schedule__title{
  h2{
    font-family: 'Avenir Next Cyr Demi', sans-serif;
    font-size: 48px;
    line-height: 59px;
    margin-bottom: 78px;
  }
}
.schedule__list{
  ul{
    list-style: none;
    padding: 0;
    margin: 0;
    li{
      padding-left: 170px;
      position: relative;
    }
    li+li{
      margin-top: 80px;
    }
  }
}
.schedule__list{
  .item-1:before,
  .item-2:before,
  .item-3:before,
  .item-4:before,
  .item-5:before,
  .item-6:before{
    content: '';
    position: absolute;
    left: 0;
    background-size: 125px 115px;
    height: 115px;
    width: 125px;
  }
  .item-1:before{
    background-image: url('../assets/img/item-1.svg');
  }
  .item-2:before{
    background-image: url('../assets/img/item-2.svg');
  }
  .item-3:before{
    background-image: url('../assets/img/item-3.svg');
  }
  .item-4:before{
    background-image: url('../assets/img/item-4.svg');
  }
  .item-5:before{
    background-image: url('../assets/img/item-5.svg');
  }
  .item-6:before{
    background-image: url('../assets/img/item-6.svg');
  }
}
.item-1,
.item-2,
.item-3,
.item-4,
.item-5,
.item-6{
  h4{
    font-family: 'Avenir Next Cyr Demi', sans-serif;
    font-size: 36px;
    line-height: 44px;
  }
  p{
    font-size: 20px;
    line-height: 35px;
  }
}
</style>