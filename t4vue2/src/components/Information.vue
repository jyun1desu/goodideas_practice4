<template>
    <div class="information">
        <nav>
            <a 
            v-for="link in guideLinks"
            :key="link.title"
            :href="link.link">
            {{link.title}}
            </a>
            <span>|</span>
        </nav>
        <div class="copyrights">&copy; COPYRIGHT 2012. ALL RIGHT RESERVED.</div>
    </div>
</template>

<script>
    export default {
    data() {
        return {
        guideLinks: [
            { title: "HOME", link: "#" },
            { title: "ABOUT", link: "#" },
            { title: "GALLERY", link: "#" },
            { title: "BLOG", link: "#" },
            { title: "CONTACT", link: "#" },
        ],
        };
    },
    };
</script>

<style>
.information {
  font-family: "Oswald", sans-serif;
  color: #ab7d0f;
  text-align: center;
  font-size: 14px;
  font-weight: bold;
  margin-top: 15px;
}

.information a {
  color: #241b18;
}

.information a:hover {
  color: #ab7d0f;
  text-decoration: none;
}

.information span {
  font-weight: normal;
  margin: 0 5px;
}

.information span:last-child{
    display: none;
}

@media (min-width: 768px) {
  .information {
    display: flex;
    justify-content: space-between;
    background-image: url(../assets/img/separator-dark.png);
    background-position: top;
    background-repeat: repeat-x;
    padding-top: 15px;
  }

  .information span {
    display: none;
  }

  .information nav {
    order: 1;
    font-size: 0;
  }

  .information a {
    display: inline-block;
    color: #ab7d0f;
    padding: 0 10px;
    font-size: 14px;
  }
}
</style>