<template>
  <b-container>
    <b-container class="p-3">
      <b-row class="m-5">
        <span class="h1">Before Konnect...</span>
      </b-row>
      <b-row>
        <b-col class="h4" cols="12" md="8">
          "Very often, we find ourselves with the unsatiable desire to take a break
          from the perpetuating grind of our seemingly neverending quest for higher
          education. When the incessant drone of academia has reached its maximum
          saturation into our core, and the need to engage in a game of
          monopoly, poker, patty-cakes... ANYTHING... with some fellow human beings,
          has manifested into sheer
          desperation, a hiatus is necessary. The challenge remains in finding
          individuals at those specific brief spurts of time when it's essential,
          for a duration long enough to restore sanity to our existence, before
          returning to the relentless world of knowledge cultivation. Konnect handles
          that challenge.... it is the solution, by converting those awkward wasted
          moments into positive contributions towards our life balance."
        </b-col>
        <b-col cols="12" md="4">
          <img class="team" src="../assets/team.jpg">
          <img class="team" src="../assets/team3.jpg">
        </b-col>
      </b-row>
    </b-container>
    <hr>
    <b-row class="mid">
      <h1>Meet the Team</h1>
    </b-row>
    <b-container>
      <b-row>
        <b-col offset="4" cols="4">
          <b-carousel
            id="carousel-1"
            :interval="2700"
            controls
            indicators
            background="#ababab"
            style="text-shadow: 1px 1px 2px #333;"
            fade
          >
            <b-carousel-slide caption="Sam" text :img-src="require('../assets/sam.png')"></b-carousel-slide>
            <b-carousel-slide caption="Jam" text :img-src="require('../assets/jam.png')"></b-carousel-slide>
            <b-carousel-slide caption="Ani" text :img-src="require('../assets/ani.png')"></b-carousel-slide>
            <b-carousel-slide caption="Cha" text :img-src="require('../assets/cha.png')"></b-carousel-slide>
            <b-carousel-slide caption="Jes" text :img-src="require('../assets/jes.png')"></b-carousel-slide>
          </b-carousel>
        </b-col>
      </b-row>
    </b-container>

    <b-card
      no-body
      class="overflow-hidden bioBox m-3"
      :key="member.name"
      v-for="member in members"
    >
      <b-row no-gutters>
        <b-col lg="3">
          <b-card-img style="max-width: 250px;" :src="require(`../assets/${member.img}`)"></b-card-img>
        </b-col>
        <b-col class="p-3" lg="9">
          <b-card-body> 
          <span class="name h2">
            {{member.name}}
            <b-img :src="require(`../assets/${member.poke}`)" class="h-25"/>
          </span>
          <b-card-text class="h5">{{member.blurb}}</b-card-text>
          </b-card-body>
        </b-col>
      </b-row>
    </b-card>
    <b-container class="p-5">
      <b-img class="w-100" :src="require('../assets/blip.png')"/>
    </b-container>
  </b-container>
</template>

<script>
export default {
  name: "about",
  components: {},
  data() {
    return {
      members: [
        {
          name: "Sam",
          poke: "samPok.gif",
          img: "sam.png",
          blurb:
            "Born to race down the winding mountain passes, this sleek dude can plow through the forests' narrow paths with phenomenal speed and accuracy. The thrill is in the adventure, and the prize is beyond the single Bergmite that can be acquired after the multi-hour chase. Unbeknownst to those around him, he possesses powerful skills that surpasses all; these skills so intense that his peers cannot even fathom the possibility of their existence."
        },
        {
          name: "Jam",
          poke: "jamPok.png",
          img: "jam.png",
          blurb:
            "On the surface, a seemingly completely clueless, dazed and frazzled guy... often looking like he's unsure if he has his shirt on forwards or backwards. With an unprecedented degree of amiability and joviality, it is paradoxical to not be allured with this charm. Wynaut, always a good sport, and always supportive, even when you just can't figure out how to hold your chopsticks correctly to feed yourself some popcorn."
        },
        {
          name: "Ani",
          poke: "aniPok.png",
          img: "ani.png",
          blurb:
            "One's existence is nothing but a figment of imagination and will, where the fine lines that lay between truth, fabrication, and fantasy are blurred as we saunter on the edge of sanity... [~ C. Enga] With a weakness for a perfectly rare prime rib and Mantyke, it has been dictated that life must persevere. In conjunction with this Archilles heel, a common pastime includes meandering about without purpose."
        },
        {
          name: "Cha",
          poke: "chaPok.png",
          img: "cha.png",
          blurb:
            "A Shroomish fluffiness void of the ability of being conscious in the forenoon hours. Despite this decrepitude, the dedication and devotion to the challenges of life are unparalleled deep into the twilight hours. With massive overdosing on caffeine and monosaccharides on a daily basis, it is astonishing that the coccyx has not exploded into oblivion."
        },
        {
          name: "Jes",
          poke: "jesPok.png",
          img: "jes.png",
          blurb:
            "A perpetually punctual individual, bordering on being excessively early for every occasion. Considerable positive attitude, no matter how grim or destitute the present situation may seem or be. With astounding reliability to be present through any weather or calamity like a Finneon; always ready to battle any task that materializes, regardless of its expanse, complexity, or plausibility."
        }
      ]
    };
  }
};
</script>   

<style scoped>
.name {
  font-family: cursive;
}
.team {
  width: 100%;
  border-radius: 5%;
  margin: 10px;
}
.bioBox {
  border: 1px solid rgb(238, 234, 248);
  border-radius: 2%;
  background-color: #E2EBF0;
}
</style>