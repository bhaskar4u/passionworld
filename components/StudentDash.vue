<template>
  <div>
    <a-layout id="components-layout-demo-top-side">
      <a-layout style="padding: 24px">
        <a-layout-sider width="200">
          <a-menu
            mode="inline"
            :default-selected-keys="['1']"
            :default-open-keys="['sub1']"
            style="height: 100%"
          >
            <a-sub-menu key="sub1">
              <span slot="title">
                <a-icon type="user" />School/Education Notification
              </span>
              <a-sub-menu key="school-Details">
                <span slot="title">
                  <a-icon type="laptop" />School Details
                </span>

                <a-menu-item @click="option1">Time Table/Periods/Calender</a-menu-item>
                <a-menu-item @click="option2">Live Classroom</a-menu-item>
                <a-menu-item @click="option3">Digital Syllabus</a-menu-item>

                <a-menu-item>News</a-menu-item>
                <a-menu-item>Notification</a-menu-item>
                <a-menu-item>Notes-Search Google</a-menu-item>
                <a-menu-item @click="option4">Fee Details</a-menu-item>
                <a-menu-item>Administrative connect</a-menu-item>
                <a-sub-menu key="sub2">
                  <span slot="title">
                    <a-icon type="more" />More..
                  </span>
                  <a-menu-item key="9">Scholarship News</a-menu-item>
                  <a-menu-item key="10">Others</a-menu-item>
                </a-sub-menu>
                <a-sub-menu key="sub3">
                  <span slot="title">
                    <a-icon type="exam" />Entrance Exam Details
                  </span>
                  <a-menu-item>State Govt. Entrance Exam</a-menu-item>
                  <a-menu-item>Central Govt. Entrance Exam</a-menu-item>
                  <a-menu-item>Private Organization EE</a-menu-item>
                  <a-menu-item>School EE</a-menu-item>
                  <a-menu-item>Other EE</a-menu-item>
                </a-sub-menu>
                <a-sub-menu key="sub3">
                  <span slot="title">
                    <a-icon type="exam" />Configuration(Settings)
                  </span>
                  <a-menu-item>Talents</a-menu-item>
                  <a-menu-item>Sports</a-menu-item>
                  <a-menu-item>Any other physical activities</a-menu-item>
                </a-sub-menu>
              </a-sub-menu>
            </a-sub-menu>
            <a-sub-menu key="sub2">
              <span slot="title">
                <a-icon type="laptop" />Tour
              </span>
              <a-menu-item></a-menu-item>
            </a-sub-menu>
            <a-sub-menu>
              <span slot="title">
                <a-icon type="laptop" />Market E-Commerce
              </span>
              <a-menu-item></a-menu-item>
            </a-sub-menu>
            <a-sub-menu>
              <span slot="title">
                <a-icon type="laptop" />Job Details
              </span>
              <a-menu-item></a-menu-item>
            </a-sub-menu>
            <a-sub-menu>
              <span slot="title">
                <a-icon type="laptop" />Bank Details
              </span>
              <a-menu-item></a-menu-item>
            </a-sub-menu>
            <a-sub-menu>
              <span slot="title">
                <a-icon type="laptop" />News Students EO
              </span>
              <a-menu-item></a-menu-item>
            </a-sub-menu>
            <a-sub-menu>
              <span slot="title">
                <a-icon type="laptop" />Talents
              </span>
              <a-menu-item></a-menu-item>
            </a-sub-menu>
            <a-sub-menu>
              <span slot="title">
                <a-icon type="laptop" />Sports
              </span>
              <a-menu-item></a-menu-item>
            </a-sub-menu>

            <a-sub-menu key="sub3">
              <span slot="title">
                <a-icon type="notification" />More
              </span>
              <a-menu-item key="9">Comedy</a-menu-item>
              <a-menu-item key="10">Motivation</a-menu-item>
              <a-menu-item key="11">Technology</a-menu-item>
              <a-menu-item key="12">Startup Ideas</a-menu-item>
              <a-menu-item key="13">Page Create</a-menu-item>
              <a-menu-item key="14">Feedback</a-menu-item>
            </a-sub-menu>
          </a-menu>
        </a-layout-sider>
        <a-layout-content :style="{ padding: '0 24px', minHeight: '280px' }">
          <div>
            <LiveClsaaroom v-show="LiveClsaaroom"></LiveClsaaroom>
            <Timetable v-show="Timetable"></Timetable>
            <DigitalClassRoom v-show="DigitalClassRoom"></DigitalClassRoom>
            <FeePayments v-show="FeePayments"></FeePayments>
          </div>
        </a-layout-content>
      </a-layout>
    </a-layout>
  </div>
</template>

<script>
import Timetable from "~/components/Timetable";
import LiveClsaaroom from "~/components/LiveClsaaroom";
import DigitalClassRoom from "~/components/DigitalClassRoom";
import FeePayments from "~/components/FeePayments";
export default {
  components: {
    Timetable,
    LiveClsaaroom,
    DigitalClassRoom,
    FeePayments
  },
  data() {
    return {
      Timetable: false,
      LiveClsaaroom: false,
      DigitalClassRoom: false,
      FeePayments: false
    };
  },
  methods: {
    option1() {
      this.Timetable = true;
      this.LiveClsaaroom = false;
      this.DigitalClassRoom = false;
      this.FeePayments = false;
    },
    option2() {
      this.LiveClsaaroom = true;
      this.Timetable = false;
      this.DigitalClassRoom = false;
      this.FeePayments = false;
    },
    option3() {
      this.DigitalClassRoom = true;
      this.Timetable = false;
      this.LiveClsaaroom = false;
      this.FeePayments = false;
    },
    option4() {
      this.FeePayments = true;
      this.DigitalClassRoom = false;
      this.Timetable = false;
      this.LiveClsaaroom = false;
    }
  }
};
</script>

<style>
#components-layout-demo-top-side .logo {
  width: 120px;
  height: 31px;
  /* background: rgba(235, 28, 28, 0.2); */
  margin: 16px 28px 16px 0;
  float: left;
}
</style>
