<template>
  <div id="app">
    <div id="nav">
      <b-navbar class="navi-navbar" toggleable="lg" type="dark" variant="info">
        <b-navbar-brand class="navi-brand" href="#">
          <router-link to="/">Home</router-link>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-item class="navi-item">
              <router-link class="navi-item__link" to="/about">About us</router-link>
            </b-nav-item>
            <b-nav-item class="navi-item">
              <router-link class="navi-item__link" to="/how-we-help">How we help</router-link>
            </b-nav-item>
            <b-nav-item class="navi-item">
              <router-link class="navi-item__link" to="/contact">Contact</router-link>
            </b-nav-item>
            <!-- navigation dropdown -->
            <!-- <b-nav-item-dropdown class="navi-dropdown" text="services" right>
              <b-dropdown-item class="navi-dropdown__item" href="#">SEO</b-dropdown-item>
              <b-dropdown-item class="navi-dropdown__item" href="#">PPC</b-dropdown-item>
              <b-dropdown-item class="navi-dropdown__item" href="#">SMM</b-dropdown-item>
              <b-dropdown-item class="navi-dropdown__item" href="#">EM</b-dropdown-item>
            </b-nav-item-dropdown> -->

            <b-nav-form>
              <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
              <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
            </b-nav-form>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  font-family: 'Raleway', sans-serif;
  font-size: 13px;
  font-weight: 500;
  .navi-navbar{
    padding: 10px 40px;
    .navi-item{
      &__link {
        color: #fff;
        padding: 5px 0;
        text-transform: uppercase;
        border-bottom: 2px solid transparent;
        transition: .2s ease-in;
        &.router-link-exact-active {
          border-bottom: 2px solid #f5f5f5;
        }
        &:hover{
          text-decoration: none;
        }
      }
    }
    .navi-dropdown{
      text-transform: uppercase;
      a#__BVID__18__BV_toggle_{
        color: #fff;
      }
    }
  }
}

@media screen and (max-width: 768px){
  #nav{
    .navi-navbar{
      .navi-item{
        text-align: left;
      }
    }
  }
}
</style>
