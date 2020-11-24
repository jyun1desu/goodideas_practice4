<template>
    <div class="profile row no-gutters">
        <div class="col-12 col-md-4">
        <div class="profile_block">
            <h3>VISIT OUR SHOWROOM</h3>
            <div class="showroom">
            <img src="../assets/img/show-room.png" alt="" />
            <div class="text">
                <p>
                This is just a place holder, so you can see what the site would
                look like.
                </p>
                <p>760-962-9541</p>
                <a href="mailto:info@carvedcration.com">info@carvedcration.com</a>
            </div>
            </div>
        </div>
        </div>

        <div class="col-12 col-md-4">
        <div class="profile_block">
            <div class="blog_posts">
            <h3>RECENT BLOG POSTS</h3>
            <div
                v-for="(post, index) in recentPost"
                :key="index + post.title"
                class="recent_post"
            >
                <div class="time">
                <p>{{ post.month }}</p>
                <p>{{ post.date }}</p>
                </div>
                <div class="text">
                <h6>{{ post.title }}</h6>
                <p>{{ post.context }}</p>
                </div>
            </div>
            </div>
        </div>
        </div>
        <div class="col-12 col-md-4">
        <div class="profile_block">
            <div class="subscription">
            <h3>JOIN OUR NEWS LETTER</h3>
            <input
                class="type_in"
                type="email"
                placeholder="Enter Email Address Here for Updates"
            />
            <input class="submit" type="submit" value="SIGN UP" />
            </div>
            <div class="social_media">
            <h3>SOCIAL MEDIA</h3>
            <div class="social_media_links">
                <a
                v-for="media in socialMedias"
                :key="media.platform"
                :href="media.link"
                >
                <font-awesome-icon class="icon" :icon="media.icon" />
                </a>
            </div>
            </div>
        </div>
        </div>
    </div>
</template>

<script>
    export default {
    data() {
        return {
        socialMedias: [
            {
            platform: "facebook",
            link: "#",
            icon: ["fab", "facebook-square"],
            },
            {
            platform: "googlePlus",
            link: "#",
            icon: ["fab", "google-plus-square"],
            },
            { platform: "twitter", link: "#", icon: ["fab", "twitter"] },
        ],
        recentPost: [
            {
            month: "APR",
            date: "16",
            title: "This is just a place holder",
            context:
                "This is just a place holder, so you can see what the site would look like.",
            },
            {
            month: "APR",
            date: "15",
            title: "This is just a place holder",
            context:
                "This is just a place holder, so you can see what the site would look like.",
            },
            {
            month: "APR",
            date: "14",
            title: "This is just a place holder",
            context:
                "This is just a place holder, so you can see what the site would look like.",
            },
        ],
        };
    },
    };
</script>

<style>
    .yellow_line {
    background-image: url(../assets/img/separator-light.png);
    height: 6px;
    }

    .profile .brown_line_sm {
    background-image: url(../assets/img/separator-dark.png);
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
        background-image: url(../assets/img/separator-dark-vertical.png);
        flex: 0 0 6px;
    }

    .brown_line_sm {
        background-image: url(../assets/img/separator-dark.png);
        height: 6px;
        margin: 15px 0;
    }
    }

    .profile {
  padding: 15px 15px 0 15px;
}

.profile_block {
  padding: 15px 0;
  background-image: url(../assets/img/separator-dark.png);
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
    background-image: url(../assets/img/separator-dark-vertical.png);
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
  background-image: url(../assets/img/bg-time.png);
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
  background-image: url(../assets/img/separator-dark.png);
  background-position: bottom;
  background-repeat: repeat-x;
}

@media (min-width: 768px) {
  .subscription {
    text-align: left;
    background-image: url(../assets/img/separator-dark.png);
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
    background-image: url(../assets/img/buttons.png);
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

.social_media_links .icon {
    font-size: 30px; 
}

@media (min-width: 768px) {
    .social_media_links .icon {
        font-size: 45px; 
    } 

    .social_media_links a:not(:last-child) {
        margin-right: 30px;
    }
}
</style>