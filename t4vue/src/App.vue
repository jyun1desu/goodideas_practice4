<template>
    <header>
        <div class="wrap container-md"> 
          <Navbar />
        </div>
    </header>
    <main>
        <div class="wrap container-md">
          <MainIntroduce />
        </div>
    </main>
  
</template>

<script>
import Navbar from './components/Navbar.vue';
import MainIntroduce from './components/MainIntroduce.vue';
export default {
  name: "App",
  components: {
    Navbar,
    MainIntroduce,
  },
};
</script>

<style>
.background img {
  width: 100%;
  position: absolute;
  opacity: 0.2;
  top: 0;
  left: 0;
}

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

@media (min-width: 768px) {
  .main_introduce {
    border: 1px solid white;
    border-top: none;
  }
}



.yellow_line {
  background-image: url(./assets/img/separator-light.png);
  height: 6px;
}

.profile .brown_line_sm {
  background-image: url(./assets/img/separator-dark.png);
  height: 6px;
  margin: 15px 0;
}

@media (min-width: 768px) {
  .profile .brown_line_sm {
    display: none;
  }

  .profile .brown_line_md {
    display: block;
  }

  .showup {
    display: block;
  }

  .brown_line_vertical {
    background-image: url(./assets/img/separator-dark-vertical.png);
    flex: 0 0 6px;
  }

  .brown_line_sm {
    background-image: url(./assets/img/separator-dark.png);
    height: 6px;
    margin: 15px 0;
  }
}

.room_features {
  display: none;
}

.room_tour {
  height: 100%;
  padding: 15px;
  background-color: #4b3a33;
}

.bedroom {
  background-color: #241b18;
}

.room_tour img {
  width: 100%;
}

.room_tour .text {
  padding: 15px 0 0 0;
}

.room_tour h3 {
  color: #e2b241;
  font-family: "Oswald", sans-serif;
}

.room_tour p {
  margin-bottom: 0;
  color: white;
  text-align: justify;
}

@media (min-width: 576px) {
  .room_features {
    display: flex;
  }

  .room_slider {
    display: none;
  }

  .room_tour {
    padding: 0;
  }

  .room_tour .text {
    padding: 15px;
  }
}

.contact_information {
  background-color: white;
}

.contact_us {
  background-color: white;
  font-family: "Oswald", sans-serif;
  padding: 15px 15px 0 15px;
}

h5 {
  color: #7b7b7b;
  font-size: 18px;
  font-family: "Oswald", sans-serif;
}

.blog h5 {
  font-size: 20px;
  margin-bottom: 15px;
}

.contact_us h4 {
  color: #241b18;
  font-size: 30px;
  word-spacing: 15px;
}

.contact_us::after {
  content: " ";
  display: block;
  height: 5px;
  background-image: url(./assets/img/separator-light.png);
  background-position: bottom;
  background-repeat: repeat-x;
}

@media (min-width: 768px) {
  .contact_us {
    padding: 15px 15px 30px;
    height: 100%;
    background-image: url(./assets/img/separator-light-vertical.png);
    background-position: right;
    background-repeat: repeat-y;
  }

  .contact_us::after {
    display: none;
  }

  .contact_information {
    padding: 15px 0;
    box-shadow: inset 0px -11px 10px -11px grey;
  }

  .contact_us h4:nth-of-type(2) {
    background-image: none;
  }
}

.blog {
  padding: 15px;
}

.blog_link {
  background-color: #dddad3;
}

.blog_image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.blog_detail {
  color: #241b18;
  padding: 10px;
}

.blog_detail .date {
  margin-top: 10px;
  font-size: 12px;
}

.blog_detail .text,
.blog_detail a {
  font-weight: bold;
  color: #241b18;
  font-family: "Oswald", sans-serif;
}

@media (min-width: 576px) {
  .blog_link {
    display: flex;
  }

  .blog_image {
    flex: 0 0 45%;
    order: 2;
  }

  .blog_detail {
    flex: 0 0 55%;
    order: 1;
  }
}

footer {
  border-top: 1px solid white;
  background-color: #e2b241;
  padding-bottom: 15px;
}

@media (min-width: 768px) {
  .main_product_text {
    height: 100%;
  }

  footer {
    padding: 30px 15px;
  }
}

.profile {
  padding: 15px 15px 0 15px;
}

.profile_block {
  padding: 15px 0;
  background-image: url(./assets/img/separator-dark.png);
  background-position: bottom;
  background-repeat: repeat-x;
}

.profile_block h3 {
  font-family: "Oswald", sans-serif;
  color: #241b18;
  font-size: 22px;
  margin-bottom: 15px;
}

@media (min-width: 768px) {
  .profile {
    padding: 0;
  }

  .profile_block {
    height: 100%;
  }
}

.showroom img {
  width: 100%;
  margin-bottom: 15px;
}

.showroom a {
  color: #241b18;
  text-decoration: underline;
}

@media (min-width: 576px) {
  .showroom {
    display: flex;
  }

  .showroom h3 {
    flex: 0 0 100%;
  }

  .showroom img {
    flex: 0 0 50%;
    margin-bottom: 0;
  }

  .showroom .text {
    flex: 0 0 50%;
    padding-left: 15px;
  }
}

@media (min-width: 768px) {
  .showroom {
    display: block;
  }

  .showroom img {
    margin-bottom: 15px;
  }

  .showroom .text {
    padding-left: 0px;
  }

  .profile > div:nth-child(1) .profile_block,
  .profile > div:nth-child(2) .profile_block {
    background-image: url(./assets/img/separator-dark-vertical.png);
    background-position: right;
    background-repeat: repeat-y;
  }

  .profile > div:nth-child(1) .profile_block {
    padding: 0 15px 0 0;
  }

  .profile > div:nth-child(2) .profile_block {
    padding: 0 15px;
  }

  .profile > div:nth-child(3) .profile_block {
    padding: 0 0 0 15px;
    background-image: none;
  }
}

.recent_post {
  display: flex;
}

.recent_post:not(:last-child) {
  margin-bottom: 30px;
}

.recent_post .time {
  text-align: center;
  flex: 0 0 60px;
  height: 60px;
  margin-right: 15px;
  background-image: url(./assets/img/bg-time.png);
  background-repeat: no-repeat;
  background-size: 102% 102%;
}

.recent_post .time p {
  font-weight: bold;
  font-family: "Oswald", sans-serif;
  color: white;
  margin-bottom: 0;
  font-size: 19px;
}

.recent_post .text h6 {
  font-family: "Oswald", sans-serif;
  font-weight: bold;
  color: #241b18;
  letter-spacing: 2px;
}

.recent_post .text p {
  margin-bottom: 0px;
}

.recent_post .text p,
.showroom p {
  font-size: 14px;
}

.subscription {
  text-align: right;
  padding-bottom: 15px;
  background-image: url(./assets/img/separator-dark.png);
  background-position: bottom;
  background-repeat: repeat-x;
}

@media (min-width: 768px) {
  .subscription {
    text-align: left;
    background-image: url(./assets/img/separator-dark.png);
    background-position: bottom;
    background-repeat: repeat-x;
  }
}

.subscription h3 {
  text-align: left;
}

.subscription .type_in {
  display: block;
  width: 100%;
}

@media (min-width: 768px) {
  .subscription {
    padding-bottom: 15px;
  }

  .social_media {
    padding-top: 15px;
  }
}

input[type="email"] {
  border: 3px solid #af8112;
}

.submit {
    margin-top: 5px;
}

input[type=submit] {
    font-family: 'Oswald', sans-serif;
    color: white;
    width: 90px;
    height: 35px;
    background-color: #E2B241;
    background-image: url(./assets/img/buttons.png);
    background-position: -10px -35px;
    background-repeat: no-repeat;
    border: none;
    font-size: 14px;
}

input[type=submit]:focus {
    outline: none;
}

input[type=submit]:hover {
    background-position: -124px -35px;
}

.social_media {
    padding-top: 15px;
}

.social_media_links {
    font-size: 0px; 
    
}

.social_media_links a {
    display: inline-block;
    color: #241B18;
}

.social_media_links a:not(:last-child) {
    margin-right: 15px;
}

.social_media_links i {
    font-size: 30px; 
}

@media (min-width: 768px) {
    .social_media_links i {
        font-size: 45px; 
    } 

    .social_media_links a:not(:last-child) {
        margin-right: 30px;
    }
}




.information {
    font-family: 'Oswald', sans-serif;
    color: #AB7D0F;
    text-align: center;
    font-size: 14px;
    font-weight: bold;
    margin-top: 15px;
}

.information a {
    color: #241B18;
}

.information a:hover {
    color: #AB7D0F;
    text-decoration: none;
}

.information span {
    font-weight: normal;
}

@media (min-width: 768px) {

    .information {
        display: flex;
        justify-content: space-between;
        background-image: url(./assets/img/separator-dark.png);
        background-position: top;
        background-repeat: repeat-x;
        padding-top: 15px;
    }

    .information span{
        display: none;
    }

    .information nav {
        order: 1 ;
        font-size: 0;
    }

    .information a {
        display: inline-block;
        color: #AB7D0F;
        padding: 0 10px;
        font-size: 14px;
    }
}
</style>


