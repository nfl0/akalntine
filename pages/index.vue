<template>
  <div>
    <div class="row home-top">
      <div class="home-top-mobile">
        <div class="col s12 m12 l6 home-college-img-div hide-on-large-only">
          <img class="home-college-image-mobile" src="~/assets/images/banner.png">
        </div>
        <div class="col s12 m12 l6 center-align hide-on-large-only">
          <img id="logo-mobile" src="~/assets/images/logo4.png">
          <div class="home-logo-h2">
            <h2>Association Akal N'tine Dartanout</h2>
            <h5>Pour la Coopération et de Développement Rural</h5>
          </div>
        </div>
      </div>
      <div class="home-top-large">
        <div class="col s12 m12 l5 hide-on-med-and-down">
          <img id="logo-large" src="~/assets/images/logo4.png">
          <div class="home-logo-h2">
            <h2>Association Akal N'tine Dartanout</h2>
            <h5>Pour la Coopération et de Développement Rural</h5>
          </div>
        </div>
        <div class="col s12 m12 l7 home-college-img-div hide-on-med-and-down">
          <img class="home-college-image" src="~/assets/images/banner.png">
        </div>
      </div>
    </div>
    <div class="home-notice-box flow-text #80d8ff light-blue accent-1 hidden">
      <div class="row valign-wrapper">
        <div class="arrow-right"></div>
        <a class="left-align" :href="`${notice[current_notice].link}`">
          {{ notice[current_notice].title }}
        </a>
        <div class="button1-margin hide-on-med-and-down">
          <button class="button1-large " @click="down">
            <i class="material-icons left">chevron_left</i>
          </button>
        </div>
        <div class="button2-margin hide-on-med-and-down">
          <button class="button2-large">
            <i class="material-icons right" @click="up">chevron_right</i>
          </button>
        </div>
      </div>
    </div>
    <div class="row #e3f2fd blue lighten-5">
      <div class="col s12 m12 l6 home-about-stacs">
        <h1 class="home-about-stacs-h1">
          À Propos De L'association Akal N'tine Dartanout
        </h1>
        <p class="flow-text">
          <p>L'Association Akal Ntine Dartanout de Coopération et de Développement Rural est une organisation à but non lucratif créée pour soutenir les communautés rurales en matière de développement économique et social. Nous nous concentrons sur l'amélioration des moyens de subsistance des agriculteurs, l'accès à l'éducation et à la santé, ainsi que sur la promotion de la participation citoyenne.</p>

          <p>Notre association est dirigée par un conseil d'administration composé de membres de la communauté et de partenaires locaux, et travaille en étroite collaboration avec les autorités locales, les ONG et les organisations internationales pour atteindre nos objectifs.</p>

          <p>Nous croyons que le développement durable est essentiel pour assurer un avenir prospère pour les communautés rurales, et nous mettons en œuvre des projets innovants pour atteindre cet objectif. Nous sommes convaincus que la coopération et la participation active des communautés sont les clés pour assurer le succès de nos initiatives.</p>

          <p>Nous sommes fiers de notre engagement en faveur de la durabilité et de l'égalité, et nous sommes déterminés à continuer à travailler pour améliorer la vie des personnes dans les communautés rurales. Rejoignez-nous dans notre mission pour construire un avenir meilleur pour tous.</p>
      </div>
      <div class="col s12 m12 l6 home-about-stacs">
        <div class="carousel">
          <a class="carousel-item" href="#one!"><img src="~/assets/images/carroussel/about1.jpg"></a>
          <a class="carousel-item" href="#two!"><img src="~/assets/images/carroussel/about2.jpg"></a>
          <a class="carousel-item" href="#three!"><img src="~/assets/images/carroussel/about3.jpg"></a>
          <a class="carousel-item" href="#four!"><img src="~/assets/images/carroussel/about4.jpg"></a>
          <a class="carousel-item" href="#five!"><img src="~/assets/images/carroussel/about5.jpg"></a>
          <a class="carousel-item" href="#six!"><img src="~/assets/images/carroussel/about6.jpg"></a>
          <a class="carousel-item" href="#seven!"><img src="~/assets/images/carroussel/about7.jpg"></a>
          <a class="carousel-item" href="#eight!"><img src="~/assets/images/carroussel/about8.jpg"></a>
          <a class="carousel-item" href="#nine!"><img src="~/assets/images/carroussel/about9.jpg"></a>
          <a class="carousel-item" href="#ten!"><img src="~/assets/images/carroussel/about10.jpg"></a>

        </div>
      </div>
    </div>
    <div>
      <div class="row">
        <div class="col s12 m12 l6 left-align hide-on-large-only home-about-cse">
          <h1 class="home-about-cse-h1">
            À Propos Du Douar
          </h1>
          <p class="flow-text">
            Akal N'tine Dartanout est un petit village situé dans les montagnes de l'Atlas au Maroc. Il est connu pour son architecture traditionnelle berbère et est situé dans une région montagneuse reculée. Le village est entouré de champs en terrasse et la principale source de revenus pour les habitants est l'agriculture. Le village est également populaire pour ses vues panoramiques des montagnes et des vallées environnantes. Il est situé dans la province de Sous Massa Daraa, près de la ville de Tafraout. Le village est également connu pour ses belles kasbahs et ksours, qui sont des maisons fortifiées ou des greniers traditionnels de la région. Les visiteurs peuvent également découvrir le mode de vie traditionnel des Berbères et participer à des activités telles que la randonnée et <a href="http://www.eauxetforets.gov.ma/ChassePeche/Chasse/Pages/Chasse.aspx" target="_blank">pratiquer la chasse</a>.        
          </p>
        </div>
        <div class="col s12 m12 l6 hide-on-large-only home-about-cse-padding">
          <img src="~/assets/images/home-about-akal.jpg" class="responsive-img ">
        </div>
      </div>
      <div class="row">
        <div class="col s12 m12 l6 hide-on-med-and-down home-about-cse ">
          <img src="~/assets/images/home-about-akal.jpg" class="responsive-img">
        </div>
        <div class="col s12 m12 l6 left-align hide-on-med-and-down home-about-cse">
          <h1 class="home-about-cse-h1">
            À Propos Du Douar
          </h1>
          <p class="flow-text">
            Akal N'tine Dartanout est un petit village situé dans les montagnes de l'Atlas au Maroc. Il est connu pour son architecture traditionnelle berbère et est situé dans une région montagneuse reculée. Le village est entouré de champs en terrasse et la principale source de revenus pour les habitants est l'agriculture. Le village est également populaire pour ses vues panoramiques des montagnes et des vallées environnantes. Il est situé dans la province de Sous Massa Daraa, près de la ville de Tafraout. Le village est également connu pour ses belles kasbahs et ksours, qui sont des maisons fortifiées ou des greniers traditionnels de la région. Les visiteurs peuvent également découvrir le mode de vie traditionnel des Berbères et participer à des activités telles que la randonnée et <a href="http://www.eauxetforets.gov.ma/ChassePeche/Chasse/Pages/Chasse.aspx" target="_blank">pratiquer la chasse</a>.        
          </p>
        </div>
      </div>
    </div>
    <div class="home-achivement-events">
      <div class="home-achivement-events-container">
        <h1 class="home-achivement-events-h1">
          Réalisations Et Événements
        </h1>
        <div class="row">
          <div class="home-achivement-events-display">
            <div class="col s12 m12 l6">
              <h3 class="home-achivement-events-h3">
                Réalisations Récentes
              </h3>
              <div class="home-achivement-events-innerbox">
                <dl v-for="achivement in achivements" :key="achivement">
                  <li>{{ achivement }}</li>
                </dl>
              </div>
            </div>
            <div class="col s12 m12 l6 home-achivement-events-inner-right-box">
              <h3 class="home-achivement-events-h3">
                Recent Events
              </h3>
              <div class="home-achivement-events-innerbox">
                <dl v-for="event in events" :key="event">
                  <li>{{ event }}</li>
                </dl>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import axios from 'axios'

export default {
  mounted () {
    this.$materialize.carousel()
    this.notification()
    setInterval(this.notification, 10000)
  },
  head () {
    return {
      title: 'STACS | Department of Computer Science And Engineering | NSSCE',
      meta: [
        { hid: 'description', name: 'description', content: 'An association of students in Department of Computer Science at NSS College of Engineering where they can develop their technical knowledge and share their talents within' }
      ]
    }
  },
  data () {
    return {
      notice: {title: "", link: ""},
      current_notice: 0,
      achivements: [],
      events: []
    }
  },
  async asyncData (context) {
    const {notice} = await axios
      .get(
        'https://raw.githubusercontent.com/stacsnssce/webdata/master/notice.json',
      )
      .then(({ data }) => {
        return {
          notice: data
        }
      })
      .catch(()=>[])
    const recent = await axios
    .get(
      'https://raw.githubusercontent.com/stacsnssce/webdata/master/recent.json',
    )
    .then(({ data }) => {
      return {
        data
      }
    })
    .catch(()=>{return {achivements: [], events: []}})

    const {achivements, events} = recent.data
    return {notice, achivements, events}
  },
  methods: {
    up(){
      if(this.current_notice === this.notice.length - 1 ) {
        this.current_notice = 0
      }
      else {
        this.current_notice ++
      }
    },
    down(){
      if(this.current_notice === 0 ) {
        this.current_notice = this.notice.length - 1
      }
      else {
        this.current_notice --
      }
    },
    notification(){
      if(this.current_notice === this.notice.length - 1) {
        this.current_notice = 0
      }
      else {
        this.current_notice ++
      }
    }
  }
}
</script>
<style lang='scss' scoped>
$button1: #40c4ff;
$button2: #00b0ff;
.home-top{
  &-mobile{
    padding-left: 0px;
    margin-left: -5px;
  }
  &-large{
    padding-left: 6%;
    text-align: center;
  }
  #logo-mobile{
    max-height: 200px;
    max-width: 200px;
    height: 30vw;
  }
  #logo-large{
    margin: 0 auto;
    margin-top: 32px;
    height: 240px;
  }
  .home-logo-h2{
    margin: 0px;
    padding: 0px;

    h2 {
      font-size: 40px;
      line-height: 50px;
      text-shadow: #000000 1px 0px,
                   #000000 -1px 0px;
      font-weight: bolder;
      letter-spacing: 1.2px;
    }
  @media screen and (max-width: 600px) {
    h2{
      text-align: center;
      font-size: 30px;
      line-height: 40px;
    }
  }

    h5 {
      font-size: 20px;
      font-weight: bolder;
    }
  }
  .home-college-image{
    min-height: 400px !important;
    max-width:100%;
    max-height:100%;
    margin: 0px;
    padding-bottom: 85px;
    object-fit: cover;
  }
  .home-college-image-mobile{
  min-height: 300px !important;
    width: 100%;
    margin: 0px;
    padding: 0px 0px 50px 0px;
    object-fit: cover;
  }
  .home-college-img-div{
    padding: 0px;
  }
}
.home-notice-box{
  background-color: rgb(198, 231, 229);
  text-align: right;
  font-size: 18px;
  font-weight: bolder;
  list-style-type:none;
  padding: 0;
  margin-top: 10px;

  a {
    color: #000000
  }
  
  .arrow-right {
    width: 0;
    height: 0;
    font-size: 10px;
    border-top: 1rem solid transparent;
    border-bottom: 1rem solid transparent;
    border-left: 1rem solid #13A59B;
    padding-left: 7%;
    margin-left: 7%;
  }

  .button1-large{
    background-color: $button1;
    padding: 16px;
    border: none;
  }
  
  .button2-large{
    background-color: $button2;
    padding: 16px;
    border: none;
  }
  
  .button1-margin{
    margin: 0px 0px 0px auto;
  }
  
  .button2-margin{
    margin: 0px;
  }
  
  .noticeItem-fontSize{
    padding-right: 10px;
    font-weight: bolder;
  }
}
.home-about-stacs{
  padding: 6%;
  
  p {
    padding-top: auto 0;
    font-size: 20px;
    line-height: 40px;
  }
  
  &-h1{
    text-align: left;
    margin: 0px;
    padding-bottom: 1.5rem;
    display: inline-block;
    border-bottom: solid 4px #0DBDE8;
    font: Bold 40px/43px Source Sans Pro;
  }
}


.home-about-cse{
  padding: 8% 6%;

  p {
    padding-top: auto 0;
    font-size: 20px;
    line-height: 40px;
  }

  &-h1{
    margin: 0px;
    padding-bottom: 1.5rem;
    text-align: left;
    color: #2E2E38;
    display: inline-block;
    border-bottom: solid 4px #0DBDE8;
    font: Bold 40px/43px Source Sans Pro;
  }
}


.home-about-cse-padding{
  padding: 15vw;
}
.responsive-img{
  box-shadow: 4vw 4vw gainsboro;
}
.flow-text{
  text-align: justify;
}

.home-achivement-events{
  background-image: url("../assets/images/home-achivement-events-background-image.png");
  background-size:cover;
  background-color: rgb(226, 243, 243);
  .home-achivement-events-container{
    padding: 6%;
    .home-achivement-events-h1{
    display: inline-block;
    margin: 0px;
    padding: 1.5rem 0rem;
    text-align: left;
    font: Bold 40px/43px Source Sans Pro;
    color: #2E2E38;
    border-bottom: solid 4px #0DBDE8;
    }
    .home-achivement-events-h3{
      margin: 0px;
      padding: 50px 0px;
      text-align: left;
      font: Bold 28px/28px Source Sans Pro;
      color: #2E2E38;
    }
    .home-achivement-events-innerbox{
      background-color: #F5F7F8;
      max-width: 770px;
      height: 550px;
      padding: 50px;
      color: #155CB4;
      font-size: 19px;
      line-height: 1.9;
      box-sizing: border-box;
      overflow-y: scroll;
    }
    .home-achivement-events-inner-right-box{
      padding-left: 3%;
    }
  }
}

.row{
  margin: 0px;
}
* {
  box-sizing: border-box;
}
</style>
