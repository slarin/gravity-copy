<template>
    <div class="bdy-cont">
        <div class="box15">
            <p class="txt-sm">Testimonials</p>
            <p class="txt-lgr">
               "Professionals at their craft!
               All products were super great with strong attention to details,
                and overall vibe"
            </p>
            <div>
            <Profile 
                name="Polina Kuzina"
                position="Manager at Craftwork"
            />
            <img src="../assets/Arrowleft.png"/>
            <img src="../assets/Arrowright.png"/>
            </div>
        </div>
        <div class="box16">
        </div>
        <div class="box17">
            <div class="flex">
                <p class="txt-lg txt-bld">Our clients</p>
                <div>
                    <p class="txt-sm txt-grey">Our favorite brands are our friends! We help them to achieve their goals,
                         they help us to stay sharp.</p>
                </div>
            </div>
            <div class="flex icons">
               <img src="../assets/xiaomi.png"/>
               <img src="../assets/tinder.png"/>
               <img src="../assets/apple.png"/>
               <img src="../assets/nike.png"/>
               <img src="../assets/amd.png"/> 
            </div>
        </div>
        <div class="box18">
          <nav>
            <img src="../assets/Logosm.png"/>
            <ul>
              <li class="txt-sm">Travel</li>
              <li class="txt-sm">Explore</li>
              <li class="txt-sm">Works</li>
              <li class="txt-sm">About Us</li>
              <li class="txt-sm">Contact Us</li>
            </ul>
            <input type="text" placeholder="Your message here" @click="modal">
            <button>SEND</button>
          </nav>
          <br>
          <hr>
          <div>
            <ul>
              <li class="txt-sm">Terms</li>
              <li class="txt-sm">Promo</li>
              <li class="txt-sm">Download</li>
              <li class="txt-sm">News</li>
            </ul>
            <div>
              <img src="../assets/twitter.png"/>
              <img src="../assets/linkedin.png"/>
              <img src="../assets/google.png"/>
              <img src="../assets/facebook.png"/> 
            </div>
          </div>
        </div>
        <div class="modal" :class="{modaler: isModal}">
			    <span class="close" @click="modal(); reset();">&times;</span>
          <div class="modal-div">
          <div class="modal-content" :class="{curtain: drapes}">
          <h4>Send Us a message. We'd love to hear from you!</h4>
          <label for="name">Name</label><input type="text" required v-model="name">
          <label for="msg">Message</label><textarea cols="10" required></textarea>
          <button @click="exit" :disabled="disabler">Send Message</button>
          </div>
          <div class="exit" :class="{exiter: isExit}">
            <h3>Thank you, {{ name }}</h3>
            <p>We've recieved your message and will get back to you as soon
              as possible.
            </p>
          </div>
          </div>
        </div>
    </div>
</template>

<script>
import Profile from './Profile'
import '../styles/Footer.scss'

export default {
    name: 'Footer',

    data(){
      return {
        isModal: false,
        name: "",
        isExit: false,
        drapes: false
      }
    },

    methods: {
      modal(){
        this.isModal = !this.isModal
        this.drapes = false
      },
      exit(){
        this.isExit = !this.isExit
        this.drapes = true
      },
      reset(){
        this.isExit = false
        this.name = ''
      }
    },

    computed: {
      disabler(){
        if(this.name !== ''){
          return false
        }else{
          return true
        }
      }
    },

    components: {
      Profile
    }

}
</script>
