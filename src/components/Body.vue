<template>
   <div>
       <div class="bdy-cont">
           <div class="box3">

           </div>
           <div class="box4">
            
           </div>
           <div class="box5">
                <p class="txt-lg">
                    We solve digital problems with an outstanding
                    creative flair.
                </p>
                <p class="txt-sm">
                    The best time to view the moon, obviously, is at 
                    night when there are few clouds and the weather is 
                    accommodating for a long and lasting study.<br><br>
                </p>
                <Profile 
                    :src= "Ellipse"
                    name= "Denis Shepovalov"
                    position= "Co-Founder & CEO"
                />
            </div>
           <div></div>
           <div></div>
           <div></div>
           <div class="box9">
               <!--<hr><p class="txt-sm">SERVICES</p>-->
               <p class="txt-lg">
                   We love to work hard and explore new things.<br> 
                   Check our service list and view details.
               </p>
               <p class="txt-sm">

               </p>
           </div>
           <div class="box10">
               <hooper :itemsToShow="1.5" :centerMode="true">
                    <slide>
                        <img src="../assets/Placeholdersld1.jpg"/>
                    </slide>
                    <slide>
                        <img src="../assets/Placeholdersld2.jpg"/>
                    </slide>
                <hooper-navigation slot="hooper-addons"></hooper-navigation>
                </hooper>
           </div>
           <div class="box9"></div>
           <div></div>
           <div class="box13"></div>
           <div class="box14">
               <p class="txt-lg">
                    Well thought out and super easy to use.
                </p>
                <p class="txt-sm">
                   Tenets of this new age are<br><br>
                   <span>Simplicity</span> and <span>Minimalism</span><br><br>
                    Why do in twelve moves what you can do in <span>four</span>?
                </p>
                <Profile 
                    :src="hunedicon"
                    position="Ultimate Result"
                />
                <Profile 
                    :src="Bagicon"
                    position="Minimal Design"
                />
            </div>
       </div>
   </div> 
</template>

<script>
import Profile from './Profile'
import '../styles/Body.css'
import { Hooper, Slide, Navigation as HooperNavigation } from 'hooper';
import 'hooper/dist/hooper.css';
import Ellipse from '../assets/Ellipse.jpg'
import Bagicon from '../assets/Bagicon.png'
import hunedicon from '../assets/hunedicon.png'

export default {
    name: 'Body',

    components: {
        Profile,
        Hooper,
        HooperNavigation,
        Slide
    },

    data(){
        return{
         Ellipse: Ellipse,
         Bagicon: Bagicon,
         hunedicon: hunedicon,
         itemsToShow: 1.5, 
         centerMode: true 
        }
    }
}
</script>