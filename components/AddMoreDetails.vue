<template>
  <div class="main">
    <a-form-model-item has-feedback label="Name">
      <a-input type="date" autocomplete="off" />
    </a-form-model-item>
    <a-upload
      name="file"
      :multiple="true"
      action="https://www.mocky.io/v2/5cc8019d300000980a055e76"
    >
      <a-button>
        <a-icon type="upload" />Upload Your Image
      </a-button>
    </a-upload>
    <div style="margin: 24px" />
    <a-textarea v-model="value" placeholder="Address" :auto-size="{ minRows: 3, maxRows: 5 }" />

    <a-button type="primary" @click="submitForm('ruleForm')">Submit</a-button>
    <a-button style="margin-left: 10px" @click="resetForm('ruleForm')">Reset</a-button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      value: ""
    };
  },
  methods: {
    submitForm() {
      window.location.href = "/login";
    }
  }
};
</script>
