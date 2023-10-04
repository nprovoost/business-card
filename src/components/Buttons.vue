<template>
<div id="business">
        <div v-if="dutch" class="body__profile__button-area" id="nl-BE">
          <transition name="fade" v-on:enter="enter">
                <Dutch />
                 </transition>
                <Social />
                <button class="body__profile__button github"><a href="https://github.com/nprovoost">GitHub</a></button>
        </div>
</div>
</template>
<script>
import Dutch from './Dutch';
import Social from './Social';

export default {
    
    name: "Buttons",
    el: '#business',
    components: {
      Dutch,
      Social,
    },
    data() {
      return {
        trans: Boolean(true),
        dutch: Boolean,
        show: false,
      }
    },
    methods: {
      translate() {
        this.dutch = !this.dutch;
        this.trans = !this.trans
      },

      fadeMe: function() {
          this.show = !this.show;
      },

      enter: function() {
          var that = this;
          
          setTimeout(function() {
            that.show = false;
          }, 3000); // hide the message after 3 seconds
      }
    },
    
    
}
</script>

<style>
    .fade-enter-active,
    .fade-leave-active {
      transition: opacity 1s
    }

    .fade-enter,
    .fade-leave-to
    /* .fade-leave-active in <2.1.8 */

    {
      opacity: 0
    }

    .body__profile__button-area {
      top: -40px;
      position: relative;
    }

    .body__profile button a {
      text-decoration: none;
      color: white;
    }

    .body__profile button {
      border: none;
      border-radius: 10px;
      font-family: Orkney;
      text-transform: uppercase;
      padding: 1.5em 1em;
      width: 100%;
      color: #545454;
      letter-spacing: 2px;
      font-weight: bold;
      margin: 0.5em 0;
      cursor: pointer;
      transition: all 0.5s;
    }

    .github {
      background-color: #D6DBD2;

    }

    .github:hover {
       background-color: #BBC7A4;
    }


</style>