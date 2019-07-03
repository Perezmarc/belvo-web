<template>
  <div>

    <!-- CLAIMS -->
    <section class="claim-wrapper">
      <div class="claim-info">
        <h1 class="title">{{$t('home_claim1')}}</h1>
        <h4 class="subtitle">{{$t('home_claim2')}}</h4>
        <a :href="`mailto:${email}`"><button class="primary">Get in touch!</button></a>
      </div>
      <div class="claim-bg">
        <img src="@/assets/img/bg/radar.svg" />
      </div>
    </section>

    <!-- HIGHLIGHTS -->
    <section class="highlights-wrapper">
      <article>
        <div class="article-container">
          <div>
            <img src="@/assets/img/icons/rocket.svg" alt />
          </div>
          <h3>{{$t('home_highlights_api_title')}}</h3>
          <p>{{$t('home_highlights_api_content')}}</p>
        </div>
      </article>
      <article>
        <div class="article-container">
          <div>
            <img src="@/assets/img/icons/latam.svg" alt />
          </div>
          <h3>{{$t('home_highlights_latam_title')}}</h3>
          <p>{{$t('home_highlights_latam_content')}}</p>
        </div>
      </article>
      <article>
        <div class="article-container">
          <div>
            <img src="@/assets/img/icons/security.svg" alt />
          </div>
          <h3>{{$t('home_highlights_security_title')}}</h3>
          <p>{{$t('home_highlights_security_content')}}</p>
        </div>
      </article>
    </section>

    <!-- FEATURES -->
    <section class="features-wrapper">
      <h1>{{$t('home_features_title')}}</h1>
      <div class="features-container">
        <div class="features-item" v-for="feature in features" :key="feature.title">
          <img :src="feature.img" alt />
          <h3>{{$t(feature.title)}}</h3>
        </div>
      </div>
    </section>

    <!-- DEVELOPERS -->
    <section class="claim-wrapper">
      <div class="claim-img" >
        <img src="@/assets/img/bg/api-response.png" />
      </div>
      <div class="claim-info right">
        <h1 class="title">{{$t('home_developers_title')}}</h1>
        <h4 class="subtitle">{{$t('home_developers_content')}}</h4>
        <a :href="`mailto:${email}`"><button class="primary">Get in touch!</button></a>
      </div>
    </section>

  </div>
</template>

<script>
import Logo from '~/components/Logo.vue';

export default {
  components: {
    Logo
  },
  data() {
    return {
      email: 'hello@belvo.co',
      features: [
        {
          img: require('assets/img/icons/credit-card.svg'),
          title: 'home_features_finance_management_title'
        },
        {
          img: require('assets/img/icons/money-bag.svg'),
          title: 'home_features_credit_title'
        },
        {
          img: require('assets/img/icons/money-bag.svg'),
          title: 'home_features_investment_title'
        },
        {
          img: require('assets/img/icons/graph-bars.svg'),
          title: 'home_features_accounting_software_title'
        },
        {
          img: require('assets/img/icons/diamond.svg'),
          title: 'home_features_savings_title'
        },
        {
          img: require('assets/img/icons/money-bag.svg'),
          title: 'home_features_account_authentication_title'
        }
      ]
    };
  }
};
</script>

<style lang="sass" scoped>
@import '@/assets/sass/vars.sass'
.claim-wrapper
  display: flex
  position: relative
  .claim-info
    max-width: 500px
    width: 100%
    display: flex
    flex-direction: column
    align-items: flex-start
    &.right
      align-items: flex-end
      text-align: right
      margin-left: auto
    .title
      margin: 0 0 40px 0
    .subtitle
      margin: 0 0 40px 0
      max-width: 440px

  .claim-bg
    position: absolute
    right: -80px
    top: 0

  .claim-img
    margin-left: -80px
    img
      max-width: 700px

.highlights-wrapper
  display: flex
  background: #ffffff
  border-radius: 4px
  box-shadow: 0 0 6px 0 rgba(0, 0, 0, 0.05)
  color: $color-grey-lighten-1
  padding: 80px 0
  article
    padding: 0 80px
    flex: 1 1 33.33%
    &:not(:first-child)
      border-left: 1px solid $color-grey-lighten-2
    .article-container
      padding: 20px 0
      h3
        color: #005485
.features-wrapper
  h1
    max-width: 900px
  .features-container
    display: flex
    flex-wrap: wrap
    .features-item
      display: flex
      flex-wrap: nowrap
      flex: 1 1 33.33%
      margin: 40px 0
      h3
        margin: auto 20px
        line-height: 1.5em

</style>
