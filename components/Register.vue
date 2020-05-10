<template>
  <a-form-model
    @submit.prevent="handleSubmit"
    ref="ruleForm"
    :model="ruleForm"
    :rules="rules"
    v-bind="layout"
  >
    <a-form-model-item has-feedback label="Name">
      <a-input type="text" autocomplete="off" />
    </a-form-model-item>
    <a-form-model-item has-feedback label="Email">
      <a-input type="email" autocomplete="off" />
    </a-form-model-item>
    <a-form-model-item has-feedback label="PhoneNumber" prop="age">
      <a-input v-model.number="ruleForm.age" />
    </a-form-model-item>
    <a-form-model-item has-feedback label="Password" prop="pass">
      <a-input v-model="ruleForm.pass" type="password" autocomplete="off" />
    </a-form-model-item>
    <a-form-model-item has-feedback label="Confirm" prop="checkPass">
      <a-input v-model="ruleForm.checkPass" type="password" autocomplete="off" />
    </a-form-model-item>

    <a-form-model-item :wrapper-col="{ span: 14, offset: 4 }">
      <a-button type="primary" @click="submitForm('ruleForm')">Submit</a-button>
      <a-button style="margin-left: 10px" @click="resetForm('ruleForm')">Reset</a-button>
    </a-form-model-item>
  </a-form-model>
</template>
<script>
export default {
  data() {
    let checkPending;
    let checkAge = (rule, value, callback) => {
      clearTimeout(checkPending);
      if (!value) {
        return callback(new Error("Please input MobileNumber"));
      }
      checkPending = setTimeout(() => {
        if (!Number.isInteger(value)) {
          callback(new Error("Please input digits"));
        } else {
          if (value < 10) {
            callback(new Error("Phone numaber must be 10"));
          } else {
            callback();
          }
        }
      }, 1000);
    };
    let validatePass = (rule, value, callback) => {
      if (value === "") {
        callback(new Error("Please input the password"));
      } else {
        if (this.ruleForm.checkPass !== "") {
          this.$refs.ruleForm.validateField("checkPass");
        }
        callback();
      }
    };
    let validatePass2 = (rule, value, callback) => {
      if (value === "") {
        callback(new Error("Please input the password again"));
      } else if (value !== this.ruleForm.pass) {
        callback(new Error("Two inputs don't match!"));
      } else {
        callback();
      }
    };
    return {
      ruleForm: {
        pass: "",
        checkPass: "",
        age: ""
      },
      rules: {
        pass: [{ validator: validatePass, trigger: "change" }],
        checkPass: [{ validator: validatePass2, trigger: "change" }],
        age: [{ validator: checkAge, trigger: "change" }]
      },
      layout: {
        labelCol: { span: 4 },
        wrapperCol: { span: 14 }
      }
    };
  },
  methods: {
    submitForm(formName) {
      this.$refs[formName].validate(valid => {
        if (valid) {
          alert("submit!");
          window.location.href = "/";
        } else {
          console.log("error submit!!");
          return false;
        }
      });
    },
    resetForm(formName) {
      this.$refs[formName].resetFields();
    }
  }
};
</script>
<style>
</style>