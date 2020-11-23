<template>
    <nav class="menu navbar navbar-expand-md navbar-dark">
      
      <h1 class="logo">
          <a class="navbar-brand logo_image" href="#">
              <img src="../assets/img/logo.png" class="img-fluid" alt="brand logo">
          </a>
      </h1>

      <button class="link_button navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
      </button>

      <div class="menu_show collapse navbar-collapse" id="navbarNavAltMarkup">
          <div class="menu_list navbar-nav">
              <a 
              v-for="link in guideLinks"
              :key="link.title"
              class="menu_link nav-link" 
              :href="link.link">{{link.title}}
              </a>
          </div>
      </div>

  </nav>
</template>

<script>
export default {
  data(){
    return  {
      guideLinks:[
        {title:'HOME',link:'#'},
        {title:'ABOUT',link:'#'},
        {title:'GALLERY',link:'#'},
        {title:'BLOG',link:'#'},
        {title:'CONTACT',link:'#'}
      ],
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.logo {
  flex: 0 0 55%;
  font-size: 0;
  margin-left: 15px;
  margin-bottom: 0;
}

.logo_image {
  width: 100%;
  margin-right: 0;
  padding: 10px 0;
}

.logo_image img {
  width: 100%;
}

.menu {
  align-items: stretch;
  padding: 0;
}

.menu .menu_list .menu_link {
  font-family: "Oswald", sans-serif;
  text-align: center;
  color: white;
  border-bottom: 1px solid white;
}

.menu .menu_list .menu_link:hover {
  color: white;
  background-color: #e2b241;
  border-bottom: 1px solid white;
}

.menu .link_button {
  border: none;
}

@media (min-width: 768px) {
  .logo {
    margin-left: 0;
    flex: 0 0 40%;
  }

  .menu .menu_list {
    flex: 0 1 auto;
  }

  .menu {
    justify-content: space-between;
  }

  .menu .menu_list .menu_link {
    border-bottom: none;
  }

  .menu_show {
    flex: 0 0 auto;
  }

  .menu .menu_link:not(:last-child) {
    margin-right: 10px;
  }

  .menu .menu_list .menu_link:hover {
    color: #e2b241;
    background-color: #241b18;
    border-bottom: none;
  }
}
</style>
