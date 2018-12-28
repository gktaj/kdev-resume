<template>
  <section class="o-section o-section--header t-section t-section--header">
    <div class="c-header">
      <div class="o-section__header-bg t-section__header"></div>
      <div class="o-section__content-bg t-section__content"></div>

      <div class="o-container">
        <div class="o-section__container">

          <header class="o-section__header c-header__header t-section__header">
            <div class="c-header__inner-header">
              <div class="c-header__avatar">
                <div class="a-header c-avatar">
                  <img class="c-avatar__img" v-bind:src="avatar" alt>
                </div>
              </div>
            </div>
          </header>
          
          <div class="o-section__content c-header__content t-section__content">
            <div class="c-header__inner-content">
              <div class="c-header__top">

                <div class="c-header__brand">
                  <div class="c-brand">
                    <h1 class="c-brand__title t-title">
                      <span class="c-brand__sizer">
                        <span class="a-header c-brand__first-word t-title__first-word">{{ firstName }}</span>
                        <span class="a-header c-brand__second-word t-title__second-word">{{ lastName }}</span>
                      </span>
                    </h1>
                    <h2 class="a-header c-brand__sub-title t-sub-title">
                      <span class="c-brand__sizer">{{ title }}</span>
                    </h2>
                  </div>
                </div>
                
                <ul class="c-header__social-buttons c-social-buttons">
                  <li class="a-header" v-for="(socialAccount, index) in socialAccounts" v-bind:key="index">
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
              
              <div class="c-header__contact">
                <hr class="a-header c-header__contact-divider">

                <div class="o-grid">

                  <div class="o-grid__col-md-3 o-grid__col-sm-6" v-for="(info, index) in otherInfo" v-bind:key="index">
                    <div class="a-header o-content">
                      <div class="o-content__body">
                        <h4>{{ info.item }}</h4>
                        <p v-for="(value, index) in info.values" v-bind:key="index">{{ value }}</p>
                      </div>
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
  name: "Header",
  computed: {
    ...mapState([
      "avatar",
      "firstName",
      "lastName",
      "title",
      "socialAccounts",
      "otherInfo"
    ])
  }
};
</script>
