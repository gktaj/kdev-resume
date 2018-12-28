<template>
  
  <section class="o-section  t-section  ">

    <div class="o-section__header-bg  t-section__header"></div>
    <div class="o-section__content-bg  t-section__content"></div>

    <div class="o-container">
      <div class="o-section__container">

        <header class="o-section__header  t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">
              {{ aboutMe.title }}
            </h2>
            <div class="o-content__body  o-section__description">
              {{ aboutMe.description }}
            </div>
          </div>
        </header>

        <div class="o-section__content  t-section__content  ">
            
          <div class="o-content">
            <div class="c-intro">
              <div class="o-content__body">
                <span v-html="aboutMe.content"></span>
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
  name: "Introduction",
  computed: {
    ...mapState([
      "aboutMe"     
    ])
  }
};
</script>
