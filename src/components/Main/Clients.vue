<template>
  <section class="o-section t-section">
    <div class="o-section__header-bg t-section__header"></div>
    <div class="o-section__content-bg t-section__content"></div>

    <div class="o-container">
      <div class="o-section__container">
        <header class="o-section__header t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">{{ clients.title }}</h2>
            <div class="o-content__body o-section__description">{{ clients.description}}</div>
          </div>
        </header>

        <div class="o-section__content t-section__content">
          <ul class="c-clients o-content">
            <li v-for="(client, index) in clients.clients" v-bind:key="index">
              <a v-bind:href="client.link" target="_blank">
                <img v-bind:src="client.logo" alt>
              </a>
            </li>
          </ul>
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
    ...mapState(["clients"])
  }
};
</script>
