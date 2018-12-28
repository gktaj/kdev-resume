<template>
  
  <section class="o-section  t-section  ">

    <div class="o-section__header-bg  t-section__header"></div>
    <div class="o-section__content-bg  t-section__content"></div>

    <div class="o-container">
      <div class="o-section__container">

        <header class="o-section__header  t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">
              {{ expertise.title }}
            </h2>
            <div class="o-content__body  o-section__description">
              {{ expertise.description }}
            </div>
          </div>
        </header>

        <div class="o-section__content  t-section__content  ">
          <div class="o-grid">

            <div class="o-grid__col-sm-6" v-for="(expertise, index) in expertise.expertises" v-bind:key="index">
              <div class="o-media  o-media--block  o-content">
                <div class="o-media__figure">
                  <div class="c-number  t-primary-color">
                    {{ pad(index + 1) }}
                  </div>
                </div>
                <div class="o-media__body  o-content__body">
                  <h3>{{ expertise.title }}</h3>
                  <p>{{ expertise.content }}</p>
                </div>
              </div>
            </div>

          </div>
        </div>
        
    </div>
  </div>

</section>

</template>

<script>
import { mapState } from "vuex";

export default {
  name: "Expertise",
  computed: {
    ...mapState([
      "expertise"
    ])
  },
  methods: {
    pad(d) {
      return (d < 10) ? '0' + d.toString() : d.toString();
    }
  }
};
</script>
