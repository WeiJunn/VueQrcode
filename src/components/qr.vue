<template>
  <div class="box">
    <vue-qr
      :logoSrc="logoSrc"
      :size="200"
      :margin="0"
      :auto-color="true"
      :dot-scale="1"
      :text="appSrc"
    />
    <div class="input">
      <el-button type="primary" @click="generate()">生成</el-button>
      <el-input
        placeholder="请输入内容"
        v-model.lazy="undetermined"
        clearable
        @keyup.enter.native="generate()"
      >
      </el-input>
    </div>
  </div>
</template>

<script>
import VueQr from "vue-qr";

export default {
  data() {
    return {
      // logoSrc: require("@/assets/logo.png"),
      logoSrc: "",
      appSrc: "你输东西再识别啊，你是不是傻的",
      undetermined: "", //待定生成 和输入框双向绑定 点击生成把值赋给appSrc
    };
  },
  components: {
    VueQr,
  },
  methods: {
    generate() {
      this.appSrc = this.undetermined;
    },
  },
};
</script>


<style scoped>
.box {
  flex-direction: column;
  width: 20rem;
  height: 20rem;
  background-color: rgb(255, 255, 255);
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50px;
  padding: 20px;
}
.input {
  margin: 15px 15px 0 15px;
  display: flex;
  flex-direction: row-reverse;
}
</style>