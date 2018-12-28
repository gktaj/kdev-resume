<template>
  <section class="o-section t-section">
    <div class="o-section__header-bg t-section__header"></div>
    <div class="o-section__content-bg t-section__content"></div>

    <div class="o-container">
      <div class="o-section__container">
        <header class="o-section__header t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">{{ awards.title }}</h2>
            <div class="o-content__body o-section__description">{{ awards.description }}</div>
          </div>
        </header>
        
        <div class="o-section__content t-section__content">
          <div class="o-grid">

            <div class="o-grid__col-md-4 o-grid__col-sm-6" v-for="(award, index) in awards.awards" v-bind:key="index">
              <div class="o-content">
                <hr class="c-deco-line t-primary-color-line">
                <div class="o-content__body">
                  <h3>{{ award.title }}</h3>
                  <p>{{ award.content }}</p>
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
  name: "Awards",
  computed: {
    ...mapState([
      "awards"
    ])
  }
};
</script>
