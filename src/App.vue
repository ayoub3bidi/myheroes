<template>
  <nav class="navbar navbar-expand-md navbar-dark">

    <a class="navbar-brand display-4" href="#">My Heroes</a>

    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#collapsibleNavbar">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="collapsibleNavbar">
      <ul class="navbar-nav">
      </ul>
    </div>
  </nav>
  <br>
  <div class="container">
    <div class="row">
      <div class="col-lg-5">
        <h3 class="text-center"> {{ intro }}</h3>
      </div>
      <div class="col-lg-7">
        <img class="img-fluid" src="./assets/undraw_Code_thinking_re_gka2.png">
      </div>
    </div>
    <br>
    <div>
      <img class="Hero img-fluid" @click="showData(0)" src="./assets/Heroes/ada-lovelace.jpg">
      <img class="Hero img-fluid" @click="showData(1)" src="./assets/Heroes/Alan-Turing.jpg">
      <img class="Hero img-fluid" @click="showData(2)" src="./assets/Heroes/hedy-lamarr.jpg">
      <img class="Hero img-fluid" @click="showData(3)" src="./assets/Heroes/grace-hopper.jpg">
      <img class="Hero img-fluid" @click="showData(4)" src="./assets/Heroes/Ken-Thompson.jpg">
      <img class="Hero img-fluid" @click="showData(5)" src="./assets/Heroes/niklaus_wirth.jpg">
      <img class="Hero img-fluid" @click="showData(6)" src="./assets/Heroes/adele-goldberg.jpg">
      <img class="Hero img-fluid" @click="showData(7)" src="./assets/Heroes/steve-wozniak.jpg">
      <img class="Hero img-fluid" @click="showData(8)" src="./assets/Heroes/donald-knuth.jpg">
      <img class="Hero img-fluid" @click="showData(9)" src="./assets/Heroes/radia-perlman.jpg">
      <img class="Hero img-fluid" @click="showData(10)" src="./assets/Heroes/james-gosling.jpg">
      <img class="Hero img-fluid" @click="showData(11)" src="./assets/Heroes/bjarne_stroustrup.jpg">
      <img class="Hero img-fluid" @click="showData(12)" src="./assets/Heroes/Richard-stallman.jpg">
      <img class="Hero img-fluid" @click="showData(13)" src="./assets/Heroes/guido_van_rossum.jpg">
      <img class="Hero img-fluid" @click="showData(14)" src="./assets/Heroes/Anders_Hejlsberg.jpg">
      <img class="Hero img-fluid" @click="showData(15)" src="./assets/Heroes/Brian_Kernighan.jpg">
      <img class="Hero img-fluid" @click="showData(16)" src="./assets/Heroes/Dennis_Ritchie.jpg">
      <img class="Hero img-fluid" @click="showData(17)" src="./assets/Heroes/bill_gates.jpg">
      <img class="Hero img-fluid" @click="showData(18)" src="./assets/Heroes/tim_berners_lee.jpg">
      <img class="Hero img-fluid" @click="showData(19)" src="./assets/Heroes/linus_torvalds.jpg">
    </div>
  </div>
  <div v-if="dataShowing">
    <Data @hide="showData" :heroName="heroName" :description="description" />
  </div>
  <footer class="py-5">
    <div class="container">
      <div class=" text-center text-muted">
        Copyright © 2021
        <img class="mx-auto d-block" src="./assets/GitHub-Mark-32px.png">
        <a class="text-muted" href="https://github.com/ayoub3bidi/myHeroes">Ayoub Abidi</a>
      </div>
    </div>
  </footer>
</template>

<script>
  import Data from './components/Data.vue'
  export default {
    name: 'App',
    components: {
      Data
    },
    data() {
      return {
        intro: "They say you should never meet your heroes, but sometimes you need to know them first before considering them as your heroes. This is why i'm introducing to you my 20 heroes and maybe you can consider them yours too after checking their mini biographies below.",
        dataShowing: false,
        heroName: "",
        description: "",
        pic: "",
        hero: [{
            name: "Ada Lovelace (The Woman Who Wrote The World's First Computer Program)",
            "description": "She is the daughter of the famous romantic poet Lord Byron, and her mother encouraged her to study mathematics at an early age, and in 1840 she wrote Babbage's analytical algorithm, which was not tested in her life, but was widely recognized as the first written computer program in the world.",
          },
          {
            name: "Alan Turing (inventor of the CAPTCHA codes)",
            "description": "Alan Turing made important contributions to his army and country in World War II, and he is an exceptional computer scientist and mathematician, who in 1950 wrote books on artificial intelligence and devised the experience of the ability of computers to think, which we know today with what is called the Turing experiment. Today, reverse Turing codes are used in CAPTCHA codes to find out if the user is human or automatic.",
          },
          {
            name: "Hedy Lamarr (Hollywood Star Who Invented WIFI)",
            "description": "One of the brightest stars of Hollywood in both the thirties and forties of the last century, she was the inventor of the concept of radio frequency signals during World War II in the hope of using it with Axis missiles. Although her invention never came to fruition during the war, her technology helped create the Bluetooth and WIFI we know today.",
          },
          {
            name: "Grace Hopper (Navy Admiral and Software Mother)",
            "description": "She is a member of the US Navy and an amazing computer scientist, and she is the first to suggest a computer programming language in the English language, as she built her first translator on the world on systems based on letters and numbers. In 1959, she led the CODASYL Alliance (the Committee for Data Systems Languages, established to develop standard programming languages) to create the COBOL programming language. She was called the mother of software.",
          },
          {
            name: "Ken Thompson (Hacker and Inventor of the B Programming Language)",
            "description": "Ken Thompson is a multi-talented hacker who is responsible for designing the Unix system, inventor of the B and Go programming language that was used in some of the apps we know today like: SoundCloud and Twitch.",
          },
          {
            name: "Niklaus Wirth (Writer of some of the most important scripts)",
            "description": "Responsible for authoring a number of important programming languages, the most important of which is Pascal, which was designed to develop the programming language ALGOL 60, as it is a standard introductory programming language for students. His works are key to very important scripts that still exist today.",
          },
          {
            name: "Adele Goldberg (the woman who inspired Steve Jobs)",
            "description": "Smaltalk-80 and Simula 67 were paved with her work in building graphical interfaces in computers that are very similar to those present today, and thus she was Steve Jobs' inspiration to build a desktop environment for Mac. She also predicted the development and rise of social media in her article “Personal Dynamic Media”.",
          },
          {
            name: "Steve Wozniak (The Genius Behind the Apple Legend)",
            "description": "He built his first fast Macintosh computer manually in 1976, and was also one of the first to work on Atari video games, working on intricate electronic board designs. His work on video games inspired him to design the Apple II color graphics interface, which would become the most successful computer of the time.",
          },
          {
            name: "Donald Knuth (Pioneer in Modern Computer Programming)",
            "description": "One of the brightest pioneers in computer science, in terms of coding and his art of computer programming, he created both WEB and CWEB software systems. He also created TeX typesetting systems that help any user to write everything they need in a simple, effective and amazing way.",
          },
          {
            name: "Radia Perlman (The Woman Who Made Big Networks possible)",
            "description": "Its invention of the STP protocol made it impossible for networks to connect to each other. Connecting this protocol between different Internet networks, that is, the presence of any link that does not follow its address range to the address tree has become possible to connect to it, so the existence of both the Bridge and the Router is the best guide. Therefore, they connect the different networks, thus expanding the network in an extraordinary way.",
          },
          {
            name: "James Gosling (The Scientist Who Invented Java)",
            "description": "The scientist James Gosling, who has developed the world's programmers, so the Java language is a language that is able to work in any existing system environment, and it is the most important language for most programmers, especially web and Android programmers!",
          },
          {
            name: "Bjarne Stroutrup (designer of the most important programming language used)",
            "description": "Byarn Strostrup is a Danish computer scientist and creator of the C ++ programming language, who has been working on it since 1979. He persevered until it became one of the most important and widely used C languages ​​in the world, being used for nearly everything from desktop applications to spaceflight applications.",
          },
          {
            name: "Richard Stallman (open source software programmer)",
            "description": "He is responsible for free and open source software, in addition to his creation of the GNU System project, which is huge in its kind and relies on the idea that software should be free for everyone (you don't how much we love you, man). He is also the creator of Emacs that includes an enormous number of text editors, which are still in use today.",
          },
          {
            name: "Guido van Rossum (Creator of the Python language)",
            "description": "He is a Dutch programmer and creator of the Python programming language, which was designed with a simple structure, small in size, and at the same time very effective.",
          },
          {
            name: "Anders Hejlsberg (The Scientist Who Groundbreaking JavaScript)",
            "description": "Danish scientist and creator of the j ++ language, and among his achievements is the TypeScript language, which was used by Microsoft, and which is also the cornerstone of the creation of the JavaScript language.",
          },
          {
            name: "Brain Kernighan (one of the three minds who invented the Unix system)",
            "description": "He is one of the main contributors to building the Unix system, as he authored many programs for this system such as: AWK and AMPL. AMPL has been used by thousands of companies, educational institutions and governments, even to this day.",
          },
          {
            name: "Dannis Ritchie (Creator of C Language)",
            "description": "Besides being the creator of the C language, Dennis Richie is one of the minds that worked with Ken to create the Unix system. Today the C language exists in all the applications and systems we know, and it is an easy, fast and stable language.",
          },
          {
            name: "Bill Gates (do i need to introduce him to you?)",
            "description": "We all know who Gates is and his career that began in 1975 after he left Harvard University. Gates and his friend Paul Allen developed the Altair 8800 emulator, the BASIC compiler for their Altair system. Then Microsoft established one of the largest technology empires in the world, to market their computers in the global market.",
          },
          {
            name: "Tim Berners-Lee (The Man Who Created The World Wide Web)",
            "description": "Tim Berners-Lee is known as the creator of the global web and the first browser in the world, in addition to creating basic languages ​​for the web such as: HTML, creating the HTTP protocol and what we today call the link or URL. HTML is an introductory language for many programmers, and it enjoyed a lot of popularity in the early 2000s, especially after the rise of social media.",
          },
          {
            name: "Linus Torvalds (mastermind of Linux, Android, and Chrome)",
            "description": "He is a software engineer, and the creator of the Linux kernel, and he used the GNU project to create the second version of this kernel, and without his work, we would not have seen all of the Linux, Android and Chrome systems.",
          }
        ]
      }
    },
    methods: {
      showData(i) {
        this.dataShowing = !this.dataShowing;
        this.heroName = this.hero[i].name;
        this.description = this.hero[i].description;
      }
    }
  }
</script>

<style scoped>
  nav {
    background: #3f3d56;
  }
  template {
      scroll-behavior: smooth;
  }
  .Hero {
    border-radius: 50%;
    height: auto;
    width: 200px;
    padding: 5px;
  }
</style>