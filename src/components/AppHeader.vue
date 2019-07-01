<template>
  <div class='app-header'>
    <div class="background">
    </div>
    <div class="header">
      <div class="container">
        <div class="row">
          <div class="col-xl-3 col-md-3 col-6 header__logo">
            <img src="@/assets/img/logo.svg" alt="">
          </div>
          <div class="col-xl-9 col-md-9 col-6 header__nav">
            <nav>
              <a href="#school">О школе</a>
              <a href="#courses">Направления</a>
              <a href="#schedule">Расписание</a>
              <a href="#">Контакты</a>
            </nav>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default{
  data() {
    return {

    }
  },
}
</script>

<style lang='scss' scoped>
*{
  padding-left: 0;
  padding-right: 0;
}
.app-header{
  min-height: 96px;
}
.background{
  background: linear-gradient(90deg, #639A49 0%, #B1C527 13.02%, #FCD23F 31.87%, #E77230 53.73%, #4FC2D0 77.6%, #222487 94.27%);
  filter: blur(40px);
  height: 65px;
  width: 100%;
}
.header{
  display: flex;
  align-items: center;
  position: absolute;
  top: 0;
  left: 0;
  min-height: 96px;
  background-color: #fff;
  width: 100%;
}
.header__logo{
  display: flex;
  align-items: center;
  img{
    max-width: 173px;
    width: 100%;
    height: auto;
  }
}
.header__nav{
  display: flex;
  align-items: center;
  justify-content: flex-end;
  a{
    color: #48545C;
    font-size: 20px;
    line-height: 25px;
  }
  a+a{
    margin-left: 35px;
  }
}

@media (max-width: 768px){
  .header__nav{
    nav{
      display: flex;
      flex-direction: column;
      padding: 8px 0;
      a+a{
        margin-top: 5px;
        margin-left: 0;
      }
    }
  }
  .background{
    height: 95px;
  }
}
</style>