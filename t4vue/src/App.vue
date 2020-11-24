<template>
    <header>
        <div class="wrap container-md"> 
          <Navbar />
        </div>
    </header>
    <main>
        <div class="wrap container-md">
          <MainProduct />
          <RoomSlider />
          <RoomTour />
          <ContactInfo />
        </div>
    </main>
    <footer>
        <div class="wrap container-md">
          <Profile />
          <Information />
        </div>
    </footer>
  
</template>

<script>
  import Navbar from './components/Navbar.vue';
  import MainProduct from './components/MainProduct.vue';
  import RoomSlider from './components/RoomSlider.vue';
  import RoomTour from './components/RoomTour.vue';
  import ContactInfo from './components/ContactInfo.vue';
  import Profile from './components/Profile.vue';
  import Information from './components/Information.vue';
  export default {
    name: "App",
    components: {
      Navbar,
      MainProduct,
      RoomSlider,
      RoomTour,
      ContactInfo,
      Profile,
      Information,
    },
  };
</script>

<style>
.wrap {
  padding: 0;
  max-width: 1050px;
}

header {
  background-color: #241b18;
  border-bottom: 1px solid white;
}

@media (min-width: 768px) {
  header {
    padding: 25px 15px;
  }
}

main {
  background-image: url(./assets/img/bg-body.png);
}

main .wrap {
  box-shadow: 0 0 30px black;
}

footer {
  border-top: 1px solid white;
  background-color: #e2b241;
  padding-bottom: 15px;
}

@media (min-width: 768px) {
  footer {
    padding: 30px 15px;
  }
}
</style>


