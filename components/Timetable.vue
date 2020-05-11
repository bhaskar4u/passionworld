<template cl>
  <div class="table-head">
    <h1 class="sad">School Academic Details</h1>
    <h5 class="table">Time Table</h5>

    <a-row class="row">
      <a-col :span="3">#</a-col>
      <a-col :span="3">Sun</a-col>
      <a-col :span="3">Mon</a-col>
      <a-col :span="3">Tue</a-col>
      <a-col :span="3">Wed</a-col>
      <a-col :span="3">Thus</a-col>
      <a-col :span="3">Fri</a-col>
      <a-col :span="3">Sat</a-col>
    </a-row>
    <a-row type="flex" class="row-one">
      <a-col :span="3">8:30-9:30</a-col>
      <a-col :span="3">
        <a-button @click="info"></a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
    </a-row>
    <a-row class="row-two">
      <a-col :span="3">9:30-10:30</a-col>
      <a-col :span="3">
        <a-button @click="info"></a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
    </a-row>
    <a-row class="row-third">
      <a-col :span="3">10:30-11:30</a-col>
      <a-col :span="3">
        <a-button @click="info"></a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
    </a-row>
    <a-row class="row-four">
      <a-col :span="3">11:30-12:30</a-col>
      <a-col :span="3">
        <a-button @click="info"></a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
    </a-row>
    <a-row class="row-five">
      <a-col :span="3">1:30-2:30</a-col>
      <a-col :span="3">
        <a-button @click="info"></a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
    </a-row>
    <a-row class="row-six">
      <a-col :span="3">2:30-3:30</a-col>
      <a-col :span="3">
        <a-button @click="info"></a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
      <a-col :span="3">
        <a-button @click="info">Subject</a-button>
      </a-col>
    </a-row>
  </div>
</template>

<script>
import { Modal } from "ant-design-vue";
export default {
  methods: {
    info() {
      const h = this.$createElement;
      this.$info({
        title: "This is a notification message",
        content: h("div", {}, [
          h("p", "some messages...some messages..."),
          h("p", "some messages...some messages...")
        ]),
        onOk() {}
      });
    }
  }
};
</script>
<style>
.table-head {
  background-color: blue;
  color: white;
  height: 500px;
  width: 100%;
  margin-left: auto;
}
.sad {
  color: white;
}
.table {
  color: white;
}
.row {
  margin-top: 10px;
}
.row-one {
  margin-top: 20px;
}
.row-two {
  margin-top: 20px;
}
.row-third {
  margin-top: 20px;
}
.row-four {
  margin-top: 20px;
}
.row-five {
  margin-top: 20px;
}
.row-six {
  margin-top: 20px;
}
</style>