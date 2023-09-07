<template>
  <div class="top">
    <p class="top__title">束縛彼氏の部屋からの脱出</p>
    <p class="top__description">
      あなたは普通の生活を送っていたが、最近彼氏の態度が急変し、束縛心が強くなってきたことに気づいた。<br />
      彼の部屋に入った瞬間、何かが違うことに気づく。ドアが外からの開けることができないようになっている<br />
      あなたは自分が彼の監視下に置かれ、彼によって縛り付けられてしまったことを知る。<br />
      あなたはパニックになりながらも、この部屋からの脱出を試みることに決めた。<br />
      今、ここから脱出するんだ。
    </p>
    <nuxt-link class="top__link" to="/one">問題をとく</nuxt-link>
  </div>
</template>

<style lang="scss" scoped>
.top {
  color: #fff;
  &__title {
    font-size: 48px;
  }
  &__description {
    font-size: 24px;
  }
  a {
    color: #639bb7;
    text-decoration: none;
    font-size: 24px;
  }
}
</style>
