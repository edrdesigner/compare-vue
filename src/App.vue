<template>
  <div id="app">
    <div id="app">
      <div class="nav has-shadow">
          <div class="container">
             <div class="nav-left">
              
                <router-link to="/" class="nav-item">My Company</router-link>
             </div>
             <span class="nav-toggle" v-on:click="toggleNav" v-bind:class="{ 'is-active': isActive }">
                <span></span>
                <span></span>
                <span></span>
             </span>

             <div class="nav-right nav-menu" v-bind:class="{ 'is-active': isActive }">
                
                <router-link to="/" class="nav-item r-item">Home</router-link>
                <router-link to="/faq" class="nav-item r-item">Features</router-link>
                <router-link to="/faq" class="nav-item r-item">About</router-link>
                <router-link to="/faq" class="nav-item r-item">Faq</router-link>
                
                <div class="nav-item">
                  <p class="control">
                    <a class="button is-primary is-outlined">
                       <span class="icon">
                          <i class="fa fa-download"></i>
                       </span>
                       <span>
                         Join Now
                       </span>
                    </a>
                  </p>
                </div>

             </div>
          </div><!-- container -->
      </div>
    </div>
    
    <router-view></router-view>


    <footer class="footer is-primary">
        <div class="container">
          <div class="container">
            <div class="columns">
                <div class="column">
                  <p>
                    An this is here a spiff footer, where you can put stuff.
                  </p>
                </div>
                <div class="column has-text-right">
                  <a class="icon" href="https://www.facebook.com" target="_blank"><i class="fa fa-facebook"></i></a>
                  <a class="icon" href="https://www.twitter.com" target="_blank"><i class="fa fa-twitter"></i></a>
                </div>
               
            </div>
          </div>
        </div>
    </footer>

  </div>
</template>

<script>
export default {
  name: 'app',
  data: function(){
    return {
      isActive: false
    }
  }, 
  methods: {
    toggleNav: function() {
      this.isActive = !this.isActive;
    }
  }
}
</script>

<style lang="sass">

@import '../node_modules/bulma/bulma.sass'
@import 'mq.sass' 

.nav
  background-color: #383838
  a:hover 
    color: gray
  
.nav-left a
  color: #FFF
  font-weight: bold

a.r-item 
  color: #c1c1c1
  padding: 0.5rem 1.75rem
  +mobile
    color: gray
    &:hover
      background-color: #f1f1f1

.nav-toggle span
  background-color: #c1c1c1

footer
  background-color: $primary !important
  color: #FFF
  
  .icon
    color: #FFF
    margin-left: 20px



</style>
