<template>

<div>
<nav class="navbar navbar-dark bg-dark fixed-top">
  <div class="container-fluid">
    <router-link class="navbar-brand jmvuelog-logo" to="/">Jaemaning vuelog</router-link>
    <div class="jmvuelog-rightbutton">
      <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasDarkNavbar" aria-controls="offcanvasDarkNavbar">
        <span class="navbar-toggler-icon"></span>
      </button>
    </div>
    <div class="offcanvas offcanvas-end text-bg-dark" tabindex="-1" id="offcanvasDarkNavbar" aria-labelledby="offcanvasDarkNavbarLabel">
      <div class="offcanvas-header">
        <h5 class="offcanvas-title" id="offcanvasDarkNavbarLabel">Dark offcanvas</h5>
        <button type="button" class="btn-close btn-close-white" data-bs-dismiss="offcanvas" aria-label="Close"></button>
      </div>
      <div class="offcanvas-body">
        <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
          <li class="nav-item">
            <router-link class="nav-link active" aria-current="page" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/list">List</router-link>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              Dropdown
            </a>
            <ul class="dropdown-menu dropdown-menu-dark">
              <li><a class="dropdown-item" href="#">Action</a></li>
              <li><a class="dropdown-item" href="#">Another action</a></li>
              <li>
                <hr class="dropdown-divider">
              </li>
              <li><a class="dropdown-item" href="#">Something else here</a></li>
            </ul>
          </li>
        </ul>
        <form class="d-flex mt-3" role="search">
          <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
          <button class="btn btn-success" type="submit">Search</button>
        </form>
      </div>
    </div>
  </div>
</nav>

<div>
  <button class="mr-1 wd-10">
    <router-link to="/">????????????</router-link>
  </button>
  <button class="mr-1 wd-10">
    <router-link to="/list">??????????????????</router-link>
  </button>
  <button class="mr-1 wd-10">
    <router-link to="/detail">??????????????????</router-link>
  </button>
</div>


<router-view :data="data"></router-view>

</div>

</template>


<script>
import List from './components/List.vue' ;
import data from './assets/blog';
import Home from './components/Home.vue';
import Detail from './components/Detail.vue';

export default {
  name: 'App',
  data(){
    return {
      data : data
    }
  },
  components: {
    List : List,
    Home : Home,
    Detail : Detail
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
  margin-top: 60px;
}

.jmvuelog-logo {
  margin:0%;
  text-align: center;
  margin-left:5px;

}

.jmvuelog-rightbutton{
  width:10%;
  margin:0%;
  text-align: right;
}

.wd-10{
  width: 30%;
}

.float{
  float: left;
}

.block{
  display: block;
}

</style>
