<template>
    <div class="header">
        <nav class="nav-bar">
            <img src="../assets/Logo2.png" class="img1"/>
            
            <div class="searchBox">
            <input class="searchInput" :class="{active: isActive}" type="text" name="" placeholder="Search" @click="holder">
            <button class="searchButton" href="#">
            </button>
            </div>

            <div class="menu" @click="dropper()">
              <span class="one"></span>
              <span class="two"></span>
              <span class="three"></span>
            </div>
        </nav>

        <div class="menu-items" :class="{dropper: isDropped}">
            <ul>
              <li><router-link to="/">Home</router-link></li>
              <li><router-link to="/about">About</router-link></li>
            </ul>
        </div>

        <div class="hdr-cont">
            <div class="box1">
                <div>
                    <p class="hdr-txt-lg">
                        The 21st Century has a language - <br>
                        does your business speak it?
                    </p>
                    <p>
                        from ads that dance or sing
                        to MTV-like commercials, online advertisers
                        are now using a new type of technology: "rich media"
                        to attract new customers.<br><br>
                        vibrant colors, sharp contrast, stop-motion<br><br>
                        <span class="hdr-txt-sm">"normal" is so last century<br>
                        has your business kept up?</span>
                    </p>
                    <button>Get Started</button>
                </div>
                <div></div>
            </div>
            <div class="box2">

            </div>
            <div class="box3"></div>
        </div>
    </div>
</template>

<script>
import '../styles/Header.css'

export default {
  name: 'Header',

  data () {
    return {
      isActive: false,
      isDropped: true
    }
  },

  methods: {
    holder () {
      this.isActive = !this.isActive
    },
    dropper () {
      this.isDropped = !this.isDropped
    }
  }
}
</script>
