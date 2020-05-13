<template>
  <div>
    <a-page-header class="head" title="School Fee Details & payments" />

    <a-table :columns="columns" :data-source="data" bordered></a-table>
    <a-button type="primary" @click="pay">Pay Online</a-button>
  </div>
</template>
<script>
const columns = [
  {
    title: "School Fee",
    dataIndex: "name"
  },
  {
    title: "Tuation Fee",
    className: "column-money",
    dataIndex: "money"
  },
  {
    title: "Online Class Fee"
    //dataIndex: "address"
  },
  {
    title: "ARTechnologyFee"
    //dataIndex: "address"
  },
  {
    title: "Compulsory Fee"
    //dataIndex: "address"
  }
];

const data = [
  {
    name: "Main Fee",
    money: "300,0.00"
  },
  {
    name: "Tuation Fee"
  },
  {
    name: "Management/Scholarship"
  },
  {
    name: "Dues Fee"
  },
  {
    name: "Paid Fee"
  }
];

export default {
  data() {
    return {
      data,
      columns
    };
  },
  methods: {
    pay() {
      this.$confirm({
        title: "Make Your Payment",
        content: "Do You Want to proceed...",
        okText: "Yes",
        okType: "danger",
        cancelText: "No",
        onOk() {
          console.log("OK");
        },
        onCancel() {
          console.log("Cancel");
        }
      });
    }
  }
};
</script>
<style>
.head {
  background-color: blue;
}
</style>