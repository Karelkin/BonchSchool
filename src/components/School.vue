<template>
  <div class='school' id='school'>
    <div class="container">
      <img src="@/assets/img/school-back.svg" class='school-back' alt="">
      <div class="row">
        <div class="col-xl-7 offset-xl-1 school__info">
          <h1>Школа разработки <br> IT-проектов</h1>
          <p class='text-1'>Образовательный проект от студентов студентам, призванный распространить любовь к современным технологиям и IT-разработке, передать опыт, знания и просто с пользой провести время!</p>
          <h3>Занятия начнутся в сентябре 2019!</h3>
          <p class='text-2'>Следи за новостями в нашей группе</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  
</script>

<style lang='scss' scoped>
.school{
  position: relative;
}
.school-back{
  position: absolute;
  top: 0;
  right: 0;
  width: 40%;
}
.school__info{
  padding-top: 110px;
  // padding-bottom: 150px;
  h1{
    font-family: 'Avenir Next Cyr Demi', sans-serif;
    font-size: 64px;
    line-height: 78px;
  }
  h3{
    font-family: 'Avenir Next Cyr Demi', sans-serif;
    font-size: 36px;
    line-height: 44px;
  }
  .text-1{
    font-size: 20px;
    line-height: 35px;
  }
  .text-2{
    font-size: 24px;
    line-height: 29px;
  }
}

@media (max-width: 768px){
  .school-back{
    top: 36px;
  }
}
</style>