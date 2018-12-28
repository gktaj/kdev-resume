<template>
  <section class="o-section t-section">
    <div class="o-section__header-bg t-section__header"></div>
    <div class="o-section__content-bg t-section__content"></div>

    <div class="o-container">
      <div class="o-section__container">
        <header class="o-section__header t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">{{ profiles.title }}</h2>
            <div class="o-content__body o-section__description">{{ profiles.description }}</div>
          </div>
        </header>
        
        <div class="o-section__content t-section__content">
          <div class="o-grid">

            <div class="o-grid__col-xl-4 o-grid__col-sm-6" v-for="(profile, index) in profiles.profiles" v-bind:key="index">
              <div class="o-content">
                <a
                  v-bind:href="profile.link"
                  target="_blank"
                  class="t-link-container"
                >
                  <div class="o-media o-media--block">
                    <div class="o-media__figure">
                      <div class="c-profile__icon">
                        <i v-bind:class="profile.icon"></i>
                      </div>
                    </div>
                    <div class="o-media__body o-content__body">
                      <h3 class="t-link-container__item">{{ profile.title }}</h3>
                      <p>{{ profile.description }}</p>
                    </div>
                  </div>                  
                </a>
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
  name: "Profile",
  computed: {
    ...mapState([
      "profiles"
    ])
  }
};
</script>
