<template>
  <div id="app" class="container-fluid">


    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand href="#">
        <img src="./assets/logo.png" class="d-inline-block align-top w-25" alt="Kitten">
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item class="nav-item">
            <router-link to="/" class="nav-link">Home</router-link>
          </b-nav-item>

          <b-nav-item class="nav-item">
            <router-link to="/testing" class="nav-link">Testing</router-link>
          </b-nav-item>

          <b-nav-item class="nav-item">
            <router-link to="/exercise" class="nav-link">Exercise</router-link>
          </b-nav-item>
        </b-navbar-nav>

        
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
            <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
          </b-nav-form>

          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown right>
            <!-- Using 'button-content' slot -->
            <template v-slot:button-content>
              <em>User</em>
            </template>
            <b-dropdown-item href="#">Profile</b-dropdown-item>
            <b-dropdown-item href="#">Sign Out</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
 

  <router-view>    
  </router-view>
</div>
</template>

<script>


  export default {
    name: 'App',
    components: {

    }
  }
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;

  }
</style>
