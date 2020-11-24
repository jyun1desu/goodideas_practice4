<template>
    <div class="contact_information row no-gutters">
        <div class="col-12 col-md-4">
        <div class="contact_us">
            <h5>FOR ORDER AND INQUIRIES PLEASE CALL:</h5>
            <h4>{{ contact.phoneNumber }}</h4>
            <h5>OR YOU CAN VISIT US AT:</h5>
            <h4>{{ contact.address }}</h4>
        </div>
        </div>
        <div class="col-12 col-md-8">
        <div class="blog">
            <h5>FROM THE BLOG</h5>
            <div class="blog_window row">
            <div v-for="post in blogPost" :key="post.date" class="col-6">
                <div class="blog_link">
                <div class="blog_image">
                    <img :src="post.image" alt="" />
                </div>
                <div class="blog_detail">
                    <p class="date">{{ post.date }}</p>
                    <p class="text">{{ post.context }}</p>
                    <a href="#">READ MORE</a>
                </div>
                </div>
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
        contact: {
            phoneNumber: "760-962-9541",
            address: "THIS IS JUST A PLACE HOLDER.",
        },
        blogPost: [
            {
            date: "April 16, 2011",
            context: "THIS IS JUST A PLACEHOLDER.",
            image: require("../assets/img/carving-small.png"),
            },
            {
            date: "April 17, 2011",
            context: "THIS IS JUST A PLACEHOLDER.",
            image: require("../assets/img/resort-small.png"),
            },
        ],
        };
    },
    };
</script>

<style>
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
    background-image: url(../assets/img/separator-light.png);
    background-position: bottom;
    background-repeat: repeat-x;
    }

    @media (min-width: 768px) {
        .contact_us {
            padding: 15px 15px 30px;
            height: 100%;
            background-image: url(../assets/img/separator-light-vertical.png);
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
</style>