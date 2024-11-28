<script>
import axios from 'axios';
export default {
    name: 'NewsLetter',
    data() {
       return {
        result: [],
    };
  },
    props: {
        msg: String
    },
    mounted() {

        this.GetNews();

    },
    methods: {
        GetNews() {
            axios.get('https://www.onestopcar.somee.com/WeatherForecast/getFeedback').then(res => {
                console.log(res.data);
                this.result=res.data;
                console.log(this.result);
            })
        }
    }
}
</script>
<template>
<!-- NewsLetter Section -->
<section id="Newletter" class="newsletter section">

<!-- Section Title -->
<div class="container section-title" data-aos="fade-up">
  <h2>NewsLetter</h2>
  <p>A newsletter is a printed or electronic report containing news concerning the activities of a business.</p>
</div>
<!-- End Section Title -->

<div class="accordion accordion-flush" id="accordionFlushExample">
  <div class="accordion-item">
    <h2 class="accordion-header" id="flush-headingOne">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseOne" aria-expanded="false" aria-controls="flush-collapseOne">
        Offer #1
      </button>
    </h2>
    <div id="flush-collapseOne" class="accordion-collapse collapse" aria-labelledby="flush-headingOne" data-bs-parent="#accordionFlushExample">
      <div class="accordion-body newsoff">{{result}}</div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="flush-headingTwo">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseTwo" aria-expanded="false" aria-controls="flush-collapseTwo">
        Offer #2
      </button>
    </h2>
    <div id="flush-collapseTwo" class="accordion-collapse collapse" aria-labelledby="flush-headingTwo" data-bs-parent="#accordionFlushExample">
      <div class="accordion-body newsoff2">Placeholder content for this accordion, which is intended to demonstrate the <code>.accordion-flush</code> class. This is the second item's accordion body. Let's imagine this being filled with some actual content.</div>
    </div>
  </div>
</div>
</section><!-- /NewsLetter Section -->
</template>

<style>
#Newletter
  {
    background-color: lightgray;
  }
  .newsoff{
    background-color: yellow;
  }
  .newsoff2{
    background-color: orchid;
  }
</style>