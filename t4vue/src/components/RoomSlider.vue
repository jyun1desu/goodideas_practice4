<template>
    <div class="room_slider">
        <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
            <div class="carousel-inner">
            <div class="carousel-item active">
                <div class="room_tour">
                    <img 
                    src="../assets/img/living-room.jpg" 
                    alt="">
                    <div class="yellow_line"></div>
                    <div class="text">
                        <h3>LIVING ROOM</h3>
                        <p>This website template has been designed by Free Website Templates for you, for free. You can replace all this text with your own text.</p>
                    </div>
                </div>
            </div>
            <div class="carousel-item">
                <div class="room_tour bedroom">
                    <img src="../assets/img/bedroom.jpg" alt="">
                    <div class="yellow_line"></div>
                    <div class="text">
                        <h3>BEDROOM</h3>
                        <p>You can remove any link to our website form this website template, you're free to use this website template whthout linking back to us.</p>
                    </div>
                </div>
            </div>
            <div class="carousel-item">
                <div class="room_tour">
                    <img src="../assets/img/kitchen.jpg" alt="">
                    <div class="yellow_line"></div>
                    <div class="text">
                        <h3>KITCHEN</h3>
                        <p>If you're having problems editing this website template, then don't hesitate to ask for help on the Forums.</p>
                    </div>  
                </div>
            </div>
                <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
                    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                    <span class="sr-only">Previous</span>
                </a>
                <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
                    <span class="carousel-control-next-icon" aria-hidden="true"></span>
                    <span class="sr-only">Next</span>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default{
    data(){
    }
}
</script>

<style>
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
</style>