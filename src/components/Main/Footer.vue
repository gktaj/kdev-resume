<template>
  <section class="o-section t-section o-section--footer">
    <div class="o-section__header-bg t-section__header"></div>
    <div class="o-section__content-bg t-section__content"></div>

    <div class="o-container">
      <div class="o-section__container">
        <header class="o-section__header t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">{{ footer.title }}</h2>
            <div class="o-content__body o-section__description">{{ footer.description }}</div>
          </div>
        </header>

        <div class="o-section__content t-section__content">
          <div class="c-footer__contact">
            <div class="o-grid">
              <div
                class="o-grid__col-md-3 o-grid__col-sm-6"
                v-for="(info, index) in otherInfo"
                v-bind:key="index"
              >
                <div class="o-content">
                  <div class="o-content__body">
                    <h4>{{ info.item }}</h4>
                    <p v-for="(value, index) in info.values" v-bind:key="index">{{ value }}</p>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <hr class="c-footer__contact-divider">

          <div class="o-content">
            <div class="c-footer__bottom">
              <div class="c-footer__brand">
                <div class="c-brand">
                  <div class="o-content__body">
                    <h1 class="c-brand__title t-title">
                      <span class="c-brand__sizer c-brand__sizer--sm">
                        <span
                          class="a-footer c-brand__first-word t-title__first-word"
                        >{{ firstName }}</span>
                        <span
                          class="a-footer c-brand__second-word t-title__second-word"
                        >{{ lastName }}</span>
                      </span>
                    </h1>
                  </div>
                </div>
              </div>

              <ul class="c-footer__social-buttons c-social-buttons o-content__body">
                <li
                  class="a-footer"
                  v-for="(socialAccount, index) in socialAccounts"
                  v-bind:key="index"
                >
                  <a
                    v-bind:href="socialAccount.link"
                    target="_blank"
                    class="c-social-button t-social-button"
                  >
                    <i v-bind:class="socialAccount.className"></i>
                  </a>
                </li>                
              </ul>

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
  name: "Footer",
  computed: {
    ...mapState([
      "firstName",
      "lastName",
      "socialAccounts",
      "otherInfo",
      "footer"
    ])
  }
};
</script>
