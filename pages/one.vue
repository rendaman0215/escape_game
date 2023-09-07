<template>
  <div class="one">
    <p class="one__description">
      彼がかつてプレゼントしたコスメになにかヒントがあるかもしれない。。。
    </p>
    <label class="one__label"> 回答： </label>
    <input v-model="answer" type="text" class="one__input" />
    <br />
    <button class="one__btn" @click="handle">送信</button>
    <br />
    <p class="one__msg">{{ msg }}</p>
  </div>
</template>

<script setup>
const msgInit = "";
const msg = ref(msgInit);

const answerInit = "";
const answer = ref(answerInit);

const handle = async () => {
  if (answer.value !== "グラシャリ") {
    msg.value = "どうやら違うようだ。。。";
  } else {
    await navigateTo({
      path: "/two",
    });
  }
};
</script>

<style lang="scss" scoped>
.one {
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
