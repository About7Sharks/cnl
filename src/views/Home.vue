<template>
 <div class="home">
    <div class="panel1">
    <img style="margin-bottom:30vh;"  alt="Vue logo" src="../assets/codeSVG.svg">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <div class="text">
      <h4> An article a week to improve your coding skills</h4>
      <p>
        Here is a curated collection of 100+ articles & blog posts delivered to you, 1 article a week + a summary, in a
        free weekly newsletter</p>
        <span><input placeholder="elon@musk" type="email">&nbsp;<button>Subscribe Today</button></span>
    </div>
  </div>
  <div class="panel2">
 <div class="def">
  <h4>Def."Coder" /ˈkōdər/ noun</h4>
  <h5>1) a person who writes code for computer programs.</h5>
  <h5>2) the person reading this ;)</h5>
 </div>
  </div>
  <div class="panel3">
    <p>There are thousands of useful guides, tips, blog posts, and articles that you can read to help you improve as a coder.

But, I know how busy you are. Out there, building and growing your projects. Look at you go. I'm proud of you.

<strong>So I saved you the time and found the best ones for you</strong> and will send you one every week, along with a summary, in a free newsletter.</p>
  </div>
  <div class="panel4">
   <div style="margin:0 auto;">
      <p>Here are a <strong>few examples</strong> of the kind of articles that’ll appear in the newsletter:</p>
<p>🛠️ <a href="https://briancasel.com/full-stack-product-person/">Becoming a Full Stack Product Person by Brian Casel</a>
</p><p>📚 <a href="https://medium.com/galvanize/pixars-rules-of-storytelling-applied-to-product-managers-ux-designers-420cec0a18a6">Disney Pixar’s Rules of Storytelling Applied to Product Managers & UX Designers</a> 
</p><p>🚀  <a href="https://www.indiehackers.com/interview/quitting-our-tech-jobs-to-bootstrap-a-saas-business-512b5be159">Quitting Facebook to Bootstrap a SaaS Business</a>
</p>
   </div>
  </div>
  <div class="panel5">
    <img src="../assets/howItWorks.svg" alt="">
   <div class="text">
      <h4>How It Works</h4>
<p style="font-size:1.3rem;">Here's the same information that I said above but, this time, with colorful bullets and a pretty SVG image on the side.
</p>
<h5>The CNL is a weekly newsletter</h5><p>
Every week, you'll receive a summary and a link to 1 article that will help you become a better all-around “Coder.”
</p>
<h5>You'll get 1 article a week in your inbox</h5><p>
I know how much information load is on the internet. So I curate the articles and send you only 1 weekly to thoroughly digest.
</p>
<h5>Useful articles to improve your coding skills</h5><p>
Article subject matter ranges from how to storytell, how to start and grow a project, to how to build a project from scratch.
 </p> </div></div>
 <div class="panel6">
<div class="text">
  <h3>   Become A Coder 🛠️
</h3>
<p>Get 1 article + a summary every week in your inbox that'll improve your coding skills.
</p> 
</div>
        <span><input placeholder="elon@musk" type="email">&nbsp;<button>Subscribe Today</button></span>
</div>
<div class="footer">
  <p>© 2019 - Made with ❤️ by Zachary, inspired by </p><a href="https://theproductperson.com/">Anthony</a>

</div>
 </div>
</template>

<script>
  // @ is an alias to /src
  // import HelloWorld from '@/components/HelloWorld.vue'
  import axios from 'axios'
  export default {
    name: 'home',
    components: {
      // HelloWorld
    },
    mounted(){
      axios.get('https://cnl.netlify.com/.netlify/functions/hello').then(res=>{
        console.log(res)
      })
    }
  }
</script>
<style lang="scss" scoped>
.home{
  display: inline-flex;
  flex-direction: column;
  color: white;
  text-shadow: 2px 2px #292929;
}
  .panel1 {
    background: rgb(70, 70, 192);
    min-height: 100vh;
    width: 100vw;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    img {
      max-width: 500px;
    }
    .text{
      margin-bottom:30vh;
      max-width: 500px;
      font-size: 2.3rem;
      h4{
      text-align: left;
      margin-bottom:-8px;
      }
      input{
        min-width: 250px;
      }
    }
  }
  .panel2{
    height: 100vh;
    width: 100vw;
    background: rgb(70, 70, 192);
    display: inline-flex;
    align-items: center;
    font-size: 1.8rem;
    .def{
      max-width: 800px;
      margin: 0 auto;
      text-align: left;
      h4{
        font-size: 1.3em;
      }
    }
  }
  .panel3,.panel4{
     height: 55vh;
    width: 100vw;
    background: rgb(64, 24, 138);
       display: inline-flex;
    align-items: center;
    font-size: 1.5rem;
    p{
      max-width: 800px;
      margin: 0 auto;
    }
    a{
      color: white;
    }
  }
  .panel5{
    display: inline-flex;
    height: 100vh;
    background: rgb(112, 40, 179);
    justify-content: center;
    h4,h5,p{
      text-align: left;
    }
    h4{
      font-size: 1.68rem;
    }
    h5{
      font-size: 1.3rem;
    }
    img{
      max-width: 600px;
    }
    .text{
      margin-top: 15vh;
      max-width: 500px;
    }
  }
  .panel6{
    min-height: 35vh;
    background: rgb(70, 70, 192);
    .text{
      margin-top: 10vh;
    }
    
  }
  .footer{
      background-color: black;
      color:white;
      display: inline-flex;
      align-items: baseline;

      a{
        color: white;
      }
      
    }
</style>