<template>
  <div class="two">
    <p class="two__description">
      正解だ。扉をあける合言葉は「OPEN」だ。<br /><br />
      彼はすごく寂しがり屋だった。<br />
      まるで私は飼い主で彼は犬のようだった。<br />
      彼の心満たすにはどうしたらよいか。<br />
    </p>
    <label class="two__label"> 回答： </label>
    <input v-model="answer" type="number" class="two__input" />
    <br />
    <button class="two__btn" @click="handle">送信</button>
    <br />
    <p class="two__msg">{{ msg }}</p>
  </div>
</template>

<script setup>
const msgInit = "";
const msg = ref(msgInit);

const answerInit = "";
const answer = ref(answerInit);

const handle = async () => {
  if (answer.value !== 727) {
    msg.value = "どうやら違うようだ。。。";
  } else {
    await navigateTo({
      path: "/three",
    });
  }
};
</script>

<style lang="scss" scoped>
.two {
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
