<template>
  <div class='courses' id='courses'>
    <div class="container">
      <div class="row">
        <transition name="fade" mode="out-in">
        <div class="col-sm-12 offset-sm-0 col-10 offset-1 course__items course1" 
          :class="{'course1': selectedCourse.course1, 
            'course2': selectedCourse.course2, 
            'course3': selectedCourse.course3, 
            'course4': selectedCourse.course4, 
            'course5': selectedCourse.course5}"
          >
          <div class="container">
            <div class="row">
              <div class="col-xl-7 offset-xl-5 col-lg-8 offset-lg-4 col-12 item">
                <h2>Направления обучения</h2>
                <ul>
                  <li 
                    v-for='(course, index) in courses' 
                    :key='course.id' 
                    @click='selectedCourse = course' 
                    :class="{ active: course === selectedCourse, active2: selectedCourse.first === index }">
                    {{course.title}}
                  </li>
                </ul>
                <p>{{selectedCourse.content}}</p>   
                <!-- <img :src="course.img: require('./../assets/course-1.svg')" class='' alt="">  -->
              </div>
            </div>
          </div>
        </div>
        </transition> 
      </div>
    </div>
  </div>
</template>

<script>
export default{
  data(){
    return{
      courses: [
        {
          id: 1,
          title: 'Front-End',
          content: 'Создание интерфейсов, с которыми будут взаимодействовать пользователи, верстка сайтов по современным стандартам, обучение основам JavaScript, HTML, CSS.',
          course1: true
        },
        {
          id: 2,
          title: 'Back-End',
          content: 'Направление, в рамках которого проектируется и разрабатывается логика web-приложения, изучение основ Laravel, CRUD, MySQL.',
          course2: true
        },
        {
          id: 3,
          title: 'Mobile',
          content: 'Направление по разработке нативных приложений на платформу Android с использованием передового языка программирования Kotlin. Также будут изучены возможности хранения данных, работа с JSON (сервером) и другими фичами.',
          course3: true
        },
        {
          id: 4,
          title: 'Design',
          content: 'Проектирование интерфейсов от "А" до "Я". Здесь ты наконец-то научишься отличать UX от UI, освоишь Figma и попробуешь себя во всех основных этапах работы web-дизайнера.',
          course4: true
        },
        {
          id: 5,
          title: 'SMM',
          content: 'Мы научим не только создавать контент, оформлять и продвигать контент, но и взаимодействовать с алгоритмами социальных сетей так, чтобы они работали на тебя. Подготовлено совместно с Гуманитарным Факультетом СПБГУТ.',
          course5: true
        }
      ],
      selectedCourse: {
        id: 1,
        title: 'Front-End',
        content: 'Создание интерфейсов, с которыми будут взаимодействовать пользователи, верстка сайтов по современным стандартам, обучение основам JavaScript, HTML, CSS.',
        course1: true,
        first: 0
      },
    }
  },
  methods: {
    
  }
}
</script>

<style lang='scss' scoped>
.courses{
  margin-top: 60px;
  margin-bottom: 20px;
}
.course__items{
  border-radius: 40px;
  background-repeat: no-repeat;
  min-height: 480px;
  background-size: 101% 100%;  
  transition: background-image .6s linear .2s;
  // background: linear-gradient(300.85deg, #57944F 3.8%, #97B730 90.98%);
}
.course1{
  background-image: url('../assets/img/course-4.jpg');
}
.course2{
  background-image: url('../assets/img/course-1.jpg');
}
.course3{
  background-image: url('../assets/img/course-3.jpg');
}
.course4{
  background-image: url('../assets/img/course-2.jpg');
}
.course5{
  background-image: url('../assets/img/course-5.jpg');
}
.item{
  // padding-left: 20px;
  h2{
    color: #fff;
    font-family: 'Avenir Next Cyr Demi', sans-serif;
    font-size: 48px;
    line-height: 59px;
    margin-top: 60px;
    margin-bottom: 40px;
  }
  ul{
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-end;
  }
  li{
    font-family: 'Avenir Next Cyr Medium', sans-serif;
    color: #fff;
    font-size: 24px;
    line-height: 29px;
    text-decoration: none;
    padding: 5px 6px;
  }
  li:hover{
    cursor: pointer;
  }
  .active{
    background-color: #fff;
    color: #48545C;
    border-radius: 20px;
  }
  .active2{
    background-color: #fff;
    color: #48545C;
    border-radius: 20px;
  }
  li+li{
    margin-left: 25px;
  }
  p{
    color: #fff;
    margin-top: 56px;
    font-size: 20px;
    line-height: 35px;
    padding-left: 5px;
  }
}

@media (max-width: 992px){
  .item{
    ul{
      flex-direction: column;
      align-items: flex-end;
    }
    h2{
      margin-top: 40px;
    }
    li{
      padding: 5px 10px;
    }
  }
  .course__items{
    background: none;
  }
  .course1{
    background: linear-gradient(267.31deg, #F07D5A -14.54%, #FFBE56 90.16%);
    overflow: hidden;
    // transition: background 1s ease;
  }
  .course2{
    background: linear-gradient(301.16deg, #F78B2E 3.8%, #EF3B3B 90.98%);
    overflow: hidden;
  }
  .course3{
    background: linear-gradient(301.16deg, #51698D 3.8%, #70AAB8 90.98%);
    overflow: hidden;
  }
  .course4{
    background: linear-gradient(300.85deg, #57944F 3.8%, #97B730 90.98%);
    overflow: hidden;
  }
  .course5{
    background: linear-gradient(301.16deg, #6B925C 3.8%, #BDD339 82.36%);
    overflow: hidden;
  }
  .course1:before,
  .course2:before,
  .course3:before,
  .course4:before,
  .course5:before,{
    transition: background .5s linear .2s;
    content: '';
    position: absolute;
    background-size: 240px 240px; 
    width: 240px;
    height: 240px;
    left: 70px;
    top: 130px;
  }
  .course1:before{
    background-image: url('../assets/img/course-4.svg');
  }
  .course2:before{
    background-image: url('../assets/img/course-2.svg');
  }
  .course3:before{
    background-image: url('../assets/img/course-3.svg');
  }
  .course4:before{
    background-image: url('../assets/img/course-1.svg');
  }
  .course5:before{
    background-image: url('../assets/img/course-5.svg');
  }
}

@media (max-width: 768px){
  .item{
    h2{
      font-size: 40px;
      line-height: 50px;
    }
    li{
      font-size: 22px;
    }
  }
  .course1:before,
  .course2:before,
  .course3:before,
  .course4:before,
  .course5:before,{
    left: -60px;
  }
}

@media (max-width: 575px){
  .course1:before,
  .course2:before,
  .course3:before,
  .course4:before,
  .course5:before,{
    top: 175px;
  }
}

@media (max-width: 500px){
  .item{
    h2{
      font-size: 30px;
      line-height: 45px;
    }
    p{
      font-size: 18px;
      line-height: 26px;
    }
  }
}
</style>