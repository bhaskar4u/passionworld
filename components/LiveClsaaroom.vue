<template>
  <div class="cls">
    <a-row class="class-room">
      <a-col :span="24">Live Clsaaroom</a-col>
      <a-dropdown>
        <a class="ant-dropdown-link" @click="e => e.preventDefault()">
          Hover me
          <a-icon type="down" />
        </a>
        <a-menu slot="overlay">
          <a-menu-item @click="skype">CONTACT VIA SKYPE</a-menu-item>
          <a-menu-item>
            <a href="javascript:;">CONTACT VIA HANGOUT</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">CONTACT VIA ZOOM</a>
          </a-menu-item>
        </a-menu>
      </a-dropdown>
      <div>
        <div>
          <h1>CONTACT VIA SKYPE</h1>
          {{social.skype}}
          <h1>CONTACT VIA HANGOUT</h1>
          {{social.hangout}}
          <h1>CONTACT VIA ZOOM</h1>
          {{social.zoom}}
        </div>
      </div>
    </a-row>
  </div>
</template>
 
<script>
export default {
  data() {
    return {
      social: { skype: "", hangout: "", zoom: "" }
    };
  },
  methods: {
    skype() {
      this.social.skype = "https://www.skype.com/en/features/skype-web/";
      this.show = true;
      // this.$nextTick(() => {
      //   this.show = true
    },
    hangout() {
      this.social.hangout = "https://hangouts.google.com/";
      this.show = true;
    },
    zoom() {
      this.social.zoom = "https://zoom.us/";
    }
  }
};
</script>
<style>
.cls {
  background-color: blue;
  height: 200px;
}
.class-room {
  color: white;
}
</style>