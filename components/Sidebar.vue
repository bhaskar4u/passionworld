<template>
  <a-select
    v-decorator="[
    'race',
    {
      initialValue: profile.race,
      rules: [
       {
         required: true, message: 'Race is required.'
       },
      ]
     },
    ]"
  >
    <a-select-option value="1">Malay</a-select-option>
    <a-select-option value="2">Chinese</a-select-option>
    <a-select-option value="3">Indian</a-select-option>
    <a-select-option value="4">Others</a-select-option>
  </a-select>
</template>

<script>
export default {
  data() {
    return {
      race: ""
    };
  },
  methods: {
    race() {
      this.form.setFieldsValue({
        race: `Hi, ${value === "male" ? "man" : "lady"}!`
      });
    }
  }
};
</script>


