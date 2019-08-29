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
    </div>
</template>

<script>
import '../styles/Header.css'

export default {
  name: 'navigation',

  data() {
    return {
      isActive: false,
      isDropped: true
    }
  },

  methods: {
    holder() {
      this.isActive = !this.isActive
    },
    dropper() {
      this.isDropped = !this.isDropped
    }
  }
}
</script>