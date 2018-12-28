<template>
  <div id="app">
    <div class="c-main-container js-main-container">
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
                      <img class="c-avatar__img" src="assets/images/header/avatar.jpg" alt>
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
                            <span class="a-header c-brand__first-word t-title__first-word">Desmond</span>
                            <span
                              class="a-header c-brand__second-word t-title__second-word"
                            >Rambowski</span>
                          </span>
                        </h1>
                        <h2 class="a-header c-brand__sub-title t-sub-title">
                          <span class="c-brand__sizer">Web Developer &amp; Front-end Expert</span>
                        </h2>
                      </div>
                      <!-- /c-brand -->
                    </div>
                    <!-- /c-header__brand -->
                    <ul class="c-header__social-buttons c-social-buttons">
                      <li class="a-header">
                        <a
                          href="https://www.facebook.com/RuvenThemes/"
                          target="_blank"
                          class="c-social-button t-social-button"
                        >
                          <i class="fa fa-lg fa-facebook"></i>
                        </a>
                      </li>
                      <li class="a-header">
                        <a
                          href="https://dribbble.com/"
                          target="_blank"
                          class="c-social-button t-social-button"
                        >
                          <i class="fa fa-lg fa-dribbble"></i>
                        </a>
                      </li>
                      <li class="a-header">
                        <a
                          href="https://twitter.com/_Ruven"
                          target="_blank"
                          class="c-social-button t-social-button"
                        >
                          <i class="fa fa-lg fa-twitter"></i>
                        </a>
                      </li>
                    </ul>
                    <!-- /c-header__social-buttons -->
                  </div>

                  <div class="c-header__contact">
                    <hr class="a-header c-header__contact-divider">

                    <div class="o-grid">
                      <div class="o-grid__col-md-3 o-grid__col-sm-6">
                        <div class="a-header o-content">
                          <div class="o-content__body">
                            <h4>Location</h4>
                            <address>Portland, OR</address>
                          </div>
                        </div>
                        <!-- /o-content -->
                      </div>

                      <div class="o-grid__col-md-3 o-grid__col-sm-6">
                        <div class="a-header o-content">
                          <div class="o-content__body">
                            <h4>Phone</h4>
                            <p>534.456.886</p>
                          </div>
                        </div>
                      </div>

                      <div class="o-grid__col-md-3 o-grid__col-sm-6">
                        <div class="a-header o-content">
                          <div class="o-content__body">
                            <a href="#" target="_blank" class="t-link-container">
                              <h4>Web</h4>
                              <p>
                                <span class="t-link-container__item--blended">ruventhemes.com</span>
                              </p>
                            </a>
                          </div>
                        </div>
                      </div>

                      <div class="o-grid__col-md-3 o-grid__col-sm-6">
                        <div class="a-header o-content">
                          <div class="o-content__body">
                            <a href="#" target="_blank" class="t-link-container">
                              <h4>Email</h4>
                              <p>
                                <span class="t-link-container__item--blended">hello@example.com</span>
                              </p>
                            </a>
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
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  components: {}
};
</script>
