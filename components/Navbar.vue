<template>
    <div>
        <b-navbar toggleable="md" type="primary" variant="faded">

        <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

        <b-navbar-brand href="/">小壳科技</b-navbar-brand>

        <b-collapse is-nav id="nav_collapse">

          <b-navbar-nav>
            <b-nav-item href="#service">服务与支持</b-nav-item>
            <b-nav-item href="#about">关于我们</b-nav-item>
            
          </b-navbar-nav>

          <!-- Right aligned nav items -->
          <!-- <b-navbar-nav class="ml-auto">

            <b-nav-form>
              <b-form-input size="sm" class="mr-sm-2" type="text" placeholder="Search"/>
              <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
            </b-nav-form> -->

            <!-- <b-nav-item-dropdown text="Lang" right>
              <b-dropdown-item href="#">EN</b-dropdown-item>
              <b-dropdown-item href="#">ES</b-dropdown-item>
              <b-dropdown-item href="#">RU</b-dropdown-item>
              <b-dropdown-item href="#">FA</b-dropdown-item>
            </b-nav-item-dropdown> -->

            <!-- <b-nav-item-dropdown right> -->
              <!-- Using button-content slot -->
              <!-- <template slot="button-content">
                <em>User</em>
              </template>
              <b-dropdown-item href="#">Profile</b-dropdown-item>
              <b-dropdown-item href="#">Signout</b-dropdown-item>
            </b-nav-item-dropdown> -->
          <!-- </b-navbar-nav> -->

          <b-navbar-nav class="ml-auto">
            <b-nav-item target="_blank" href="https://fsxchen.github.io" right>博客</b-nav-item>
              
          </b-navbar-nav>

        </b-collapse>
      </b-navbar>
    </div>
</template>


<style>
    .navbar {
        height: 65px;
    }
</style>
