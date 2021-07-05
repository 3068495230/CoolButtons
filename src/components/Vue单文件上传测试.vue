<template>
  <div>
    <label for="fileInput">
      <i aria-hidden="true" class="cursor">单文件上传文件</i>
    </label>
    <input
      v-show="false"
      type="file"
      id="fileInput"
      @change="handleFileChange"
      name="file"
      ref="file"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    handleFileChange(e) {
      // let _this = this;
      let file = e.target.files;
      console.log(file,"单文件流文件流");
    }
  }
};
</script>

<style scoped>
.cursor {
  cursor: pointer;
  color: #409eff;
  font-size: 16px;
}
</style>