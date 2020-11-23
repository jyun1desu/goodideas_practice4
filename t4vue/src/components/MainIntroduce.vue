<template>
    <div class="main_introduce row no-gutters">
        <div class="col-12 col-sm-6">
        <div class="main_product">
            <img src="../assets/img/chair.jpg" alt="" />
            <div class="discount_text">
            <p>{{flagship.product}}</p>
            <p class="price">{{flagship.price}}</p>
            <a class="ad_link" 
            :href="flagship.link">VIEW DETAILS</a>
            </div>
        </div>
        </div>
        <div class="col-12 col-sm-6">
        <div class="main_product_text">
            <div>
            <h2>{{mainAdvertisingContext.title}}</h2>
            <p>{{mainAdvertisingContext.context}}</p>
            </div>
        </div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return  {
            flagship:{
                product: 'Whicker Chair',
                price: '$250.00',
                link: '#'
            },
            mainAdvertisingContext:{
                title: 'THIS IS JUST PLACE HOLDER.',
                context: `You can remove any link to our website from this website template,
                    you're free to use this website template without linking back to us.
                    This is just a place holder, so you can see what the site would look
                    like. This is just a place holder.`
            }
        }
    },
}

</script>

<style>
.main_product {
  position: relative;
  height: 100%;
}

.main_product img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

@media (min-width: 768px) {
  .main_introduce {
    border: 1px solid white;
    border-top: none;
  }
}

.discount_text {
  position: absolute;
  bottom: 20px;
  right: 20px;
  text-align: center;
}

.discount_text p {
  font-size: 16px;
  line-height: 1.2;
  margin: 0;
  font-family: "Montserrat", sans-serif;
}

.discount_text .price {
  font-weight: 400;
  font-size: 27px;
}

.discount_text a {
  font-family: "Oswald", sans-serif;
}

.ad_link {
  display: block;
  font-size: 14px;
  background-image: url(../assets/img/buttons.png);
  width: 110px;
  height: 35px;
  line-height: 35px;
  color: #966a03;
}

.ad_link:focus {
  text-decoration: none;
  color: #966a03;
}

.ad_link:hover {
  background-position: -114px 0;
  text-decoration: none;
  color: #241b18;
}

.main_product_text {
  background-image: url(../assets/img/bg-pattern.jpg);
  background-size: cover;
  padding: 30px;
  height: 100%;
}

.main_product_text h2 {
  font-family: "Oswald", sans-serif;
  font-size: 30px;
  text-align: center;
  text-shadow: 1px 1px 0 white;
}

.main_product_text p {
  text-align: center;
  margin: 0;
}

@media (min-width: 768px) {
  .main_product_text h2 {
    font-size: 50px;
    margin-bottom: 30px;
  }

  .main_product_text p {
    text-align: justify;
    line-height: 2;
  }
}

@media (min-width: 992px) {
  .main_product_text {
    padding: 60px;
  }
}
</style>