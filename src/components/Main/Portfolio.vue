<template>
  <section class="o-section t-section">
    <div class="o-section__header-bg t-section__header"></div>
    <div class="o-section__content-bg t-section__content"></div>

    <div class="o-container">
      <div class="o-section__container">
        <header class="o-section__header t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">{{ portfolio.title }}</h2>
            <div class="o-content__body o-section__description">{{ portfolio.description }}</div>
          </div>
        </header>

        <div class="o-section__content t-section__content o-section__full-bottom-space">
          <div class="o-grid o-grid--gallery">
            <div
              class="o-grid__col-sm-6"
              v-for="(portfolio, index) in portfolio.portfolioes"
              v-bind:key="index"
            >
              <a
                class="c-image-overlay t-image-overlay js-lightbox"
                v-bind:href="portfolio.link"
                data-lightbox-hidpi
                v-bind:title="portfolio.titlle"
                data-lightbox-gallery="portfolio"
              >
                <img v-bind:src="portfolio.avatar" alt>
                <div class="c-image-overlay__content">
                  <h3>{{ portfolio.title }}</h3>
                  <hr class="c-image-overlay__deco-line t-image-overlay__deco-line">
                  <p>{{ portfolio.description }}</p>
                </div>
              </a>
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
  name: "Portfolio",
  computed: {
    ...mapState(["portfolio"])
  }
};
</script>
