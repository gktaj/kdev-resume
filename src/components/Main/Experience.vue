<template>
  <section class="o-section t-section">
    <div class="o-section__header-bg t-section__header"></div>
    <div class="o-section__content-bg t-section__content"></div>

    <div class="o-container">
      <div class="o-section__container">
        <header class="o-section__header t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">{{ experience.title }}</h2>
            <div class="o-content__body o-section__description">{{ experience.description }}</div>
          </div>
        </header>
        
        <div class="o-section__content t-section__content u-pb-0">
          <div class="a-experience-timeline c-timeline t-border-color">
            
            <div class="c-timeline__item" v-for="(experience, index) in experience.experiences" v-bind:key="index">
              <div class="c-timeline__point t-timeline__point t-primary-bg"></div>              
              <div class="o-content">
                <div class="o-grid">
                  <div class="o-grid__col-md-5">
                    <div class="c-work__timeframe">{{ experience.year }}</div>
                    <h3 class="c-work__heading">{{ experience.title }}</h3>
                    <h4 class="c-work__title">{{ experience.position }}</h4>
                    <div class="c-work__location">{{ experience.location }}</div>
                  </div>
                  <div class="o-grid__col-md-7">
                    <p>{{ experience.content }}</p>
                  </div>
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
  name: "Skills",
  computed: {
    ...mapState([
      "experience"
    ])
  }
};
</script>
