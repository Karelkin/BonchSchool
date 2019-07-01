<template>
  <div class='courses' id='courses'>
    <div class="container">
      <div class="row">
        <div class="col-12 course__items course1" 
          :class="{'course1': selectedCourse.course1, 
            'course2': selectedCourse.course2, 
            'course3': selectedCourse.course3, 
            'course4': selectedCourse.course4, 
            'course5': selectedCourse.course5}"
          >
          <div class="container">
            <div class="row">
              <div class="col-lg-7 offset-lg-5 col-12 item">
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
              </div>
            </div>
          </div>
        </div>
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
          content: 'Проектирование интерфейсов от "А" до "Я". Здесь ты наконец-то научишься отличать UX от UI, освоишь Figma и попробуешь себя во всех основных этапах работы web-дизайнера',
          course1: true,
        },
        {
          id: 2,
          title: 'Back-End',
          content: '3123213213',
          course2: true
        },
        {
          id: 3,
          title: 'Mobile',
          content: 'fdsfsdfdsfsd',
          course3: true
        },
        {
          id: 4,
          title: 'Design',
          content: 'gfdgfdghfgjytrutyurhuyrt',
          course4: true
        },
        {
          id: 5,
          title: 'SMM',
          content: '111111',
          course5: true
        }
      ],
      selectedCourse: {
        id: 1,
        title: 'Front-End',
        content: 'Проектирование интерфейсов от "А" до "Я". Здесь ты наконец-то научишься отличать UX от UI, освоишь Figma и попробуешь себя во всех основных этапах работы web-дизайнера',
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
.course__items{
  border-radius: 40px;
  background-repeat: no-repeat;
  background-size: cover;
  min-height: 480px;
}
.course1{
  background-image: url('../assets/img/course-2.jpg');
}
.course2{
  background-image: url('../assets/img/course-1.jpg');
}
.course3{
  background-image: url('../assets/img/course-3.jpg');
}
.item{
  // padding-left: 40px;
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
    padding: 5px;
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
    margin-left: 35px;
  }
  p{
    color: #fff;
    margin-top: 56px;
    font-size: 20px;
    line-height: 35px;
    padding-left: 5px;
  }
}
</style>