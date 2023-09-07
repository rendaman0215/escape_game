<template>
  <div class="three">
    <p class="three__description">
      正解だ。扉をあける合言葉は「あんみち」だ。<br /><br />
      まずは二人の思い出の人形を調べるチャム。<br />
      結構私たち似たもの同士惹かれ合うってこと
    </p>
    <label class="three__label"> 回答： </label>
    <input v-model="answer" type="text" class="three__input" />
    <br />
    <button class="three__btn" @click="handle">送信</button>
    <br />
    <p class="three__msg">{{ msg }}</p>
  </div>
</template>

<script setup>
const msgInit = "";
const msg = ref(msgInit);

const answerInit = "";
const answer = ref(answerInit);

const handle = async () => {
  if (answer.value !== "0721") {
    msg.value = "どうやら違うようだ。。。";
  } else {
    await navigateTo({
      path: "/result",
    });
  }
};
</script>

<style lang="scss" scoped>
.three {
  text-align: center;
  align-items: center;
  &__label {
    color: #fff;
  }
  &__input {
    width: 50%;
    height: 36px;
    font-size: 32px;
    margin-top: 36px;
  }
  &__description {
    font-size: 24px;
    color: #fff;
  }
  &__btn {
    width: 80px;
    height: 40px;
    margin-top: 36px;
  }
  &__msg {
    color: #fff;
  }
}
</style>
