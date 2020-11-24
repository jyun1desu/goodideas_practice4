<template>
    <div class="room_features row no-gutters">
        <div 
        v-for="room in rooms"
        :key="room.type"
        class="room_features col-12 col-sm-4">
            <div class="room_tour">
                <img :src="room.image" alt="">
                <div class="yellow_line"></div>
                <div class="text">
                <h3>{{room.type}}</h3>
                <p>{{room.intro}}</p>
            </div>
            </div>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            rooms:[
                {type:'LIVING ROOM',image:require('../assets/img/living-room.jpg'),intro:`This website template has been designed by Free Website Templates for you, for free. You can replace all this text with your own text.`},
                {type:'BEDROOM',image:require('../assets/img/bedroom.jpg'),intro:`You can remove any link to our website form this website template, you're free to use this website template whthout linking back to us.`},
                {type:'KITCHEN',image:require('../assets/img/kitchen.jpg'),intro:`If you're having problems editing this website template, then don't hesitate to ask for help on the Forums.`}
                ],
        }
    }
}
</script>

<style>
.room_features {
    display: none;
}

@media (min-width: 576px) {

    .room_features {
        display: flex;
    }

    .room_slider  {
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

