<template>
  <section class="o-section t-section">
    <div class="o-section__header-bg t-section__header"></div>
    <div class="o-section__content-bg t-section__content"></div>

    <div class="o-container">
      <div class="o-section__container">
        <header class="o-section__header t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">{{ skills.title }}</h2>
            <div class="o-content__body o-section__description">{{ skills.description }}</div>
          </div>
        </header>

        <div class="o-section__content t-section__content">
          <div class="o-grid">

            <div class="o-grid__col-sm-6" v-for="(skill, index) in skills.skills" v-bind:key="index">
              <div class="o-content">
                <div class="o-media o-media--block">
                  <div class="o-media__figure">
                    <div class="c-number t-primary-color">{{ skill.percent }}
                      <small>%</small>
                    </div>
                  </div>
                  <div class="o-media__body">
                    <h3>{{ skill.title }}</h3>
                  </div>
                </div>
                <div class="c-progress-bar o-content__body t-border-color-bg u-mt-text">
                  <div class="a-progress-bar c-progress-bar__filler t-primary-bg" v-bind:data-percent="skill.percent"></div>
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
      "skills"
    ])
  }
};
</script>
