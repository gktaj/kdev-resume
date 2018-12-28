<template>
  <section class="o-section t-section">
    <div class="o-section__header-bg t-section__header"></div>
    <div class="o-section__content-bg t-section__content"></div>

    <div class="o-container">
      <div class="o-section__container">
        <header class="o-section__header t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">{{ education.title }}</h2>
            <div class="o-content__body o-section__description">{{ education.description }}</div>
          </div>
        </header>
        
        <div class="o-section__content t-section__content u-pt-0">
          <div class="o-content">
            <div class="a-education-timeline c-timeline t-border-color o-section__full-top-space">
              <div class="c-timeline__end t-border-color"></div>

              <div class="c-timeline__item" v-for="(education, index) in education.educations" v-bind:key="index">
                <div class="c-timeline__point t-timeline__point t-primary-bg"></div>
                <div class="o-content">
                  <div class="o-grid">
                    <div class="o-grid__col-md-5">
                      <div class="c-work__timeframe">{{ education.year }}</div>
                      <h3 class="c-work__heading">{{ education.title }}</h3>
                      <h4 class="c-work__title">{{ education.position }}</h4>
                      <div class="c-work__location">{{ education.location }}</div>
                    </div>
                    <div class="o-grid__col-md-7">
                      <p>{{ education.content }}</p>
                    </div>
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
    ...mapState(["education"])
  }
};
</script>
