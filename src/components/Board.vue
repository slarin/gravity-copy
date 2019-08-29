<template>
  <div class="board-grid">
    <Navigation />
    <div class="top">
      <div class="brand">
        <div>
          <p><span>Branding</span></p>
          <p>Do you know whom you are?</p>
        </div>
        <div>
          <img class="tny" src="../assets/facebook.svg">
          <img class="tny" src="../assets/google.svg">
          <img class="tny" src="../assets/twitter.svg">
        </div>
      </div>
      <div class="hero">
        
      </div>
      <div class="tg-line">
        <p>In a century where history announces that 'everything has been done!'
            standing out has never been easier for those in the know.<br>
          Question is, are you? 
        </p> 
      </div>
    </div>
    <div class="mid">
      <div class="images">
        <img class="image-cont" src="../assets/Placeholdertny1.jpg" >
        <img class="image-cont" src="../assets/Placeholdertny2.jpg" >
        <img class="image-cont" src="../assets/Placeholdertny3.jpg" >
      </div>
      <div class="bttn">
        <p>
          There's a design language for every business<br> 
          the market will not be sympathetic if yours doesn't match<br>
        </p>
        <button>EXPLORE</button> 
      </div>
    </div>
    <div class="bottom">
      <hr>
      <div class="windlass">
        <p>AWARDS</p>
        <p>SITE OF THE DAY</p>
        <p>
          <span>Singleton UI Kit</span>
          Application that helps<br> to find nearest sport centres
in your area
        </p>
        <p>2018</p>
      </div>
      <div class="windlass">
        <p style="opacity: 0;">AWARDS</p>
        <p>BEST NAVIGATION</p>
        <p>
          <span>Middleton Headers</span>
          Application that helps<br> to find nearest sport centres
in your area
        </p>
        <p>2018</p>
      </div>
    </div>
  </div>
</template>

<script>
import '../styles/Board.css'
import Navigation from './Navigation'

export default {
  name: 'board',

  components: {
    Navigation
  }
}
</script>