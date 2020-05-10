<template>
  <div>
    <a-layout id="components-layout-demo-top-side">
      <a-layout style="padding: 24px 0; background: #fff">
        <a-layout-sider width="200" style="background: #fff">
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
                  <a-icon type="more" />School Details
                </span>

                <a-menu-item key="1">Time Table/Periods/Calender</a-menu-item>
                <a-menu-item key="2">Digital Syllabus</a-menu-item>
                <a-menu-item key="3">Live Classroom</a-menu-item>
                <a-menu-item key="4">News</a-menu-item>
                <a-menu-item key="5">Notification</a-menu-item>
                <a-menu-item key="6">Notes-Search Google</a-menu-item>
                <a-menu-item key="7">Fee Details</a-menu-item>
                <a-menu-item key="8">Administrative connect</a-menu-item>
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
                  <a-menu-item key="11">State Govt. Entrance Exam</a-menu-item>
                  <a-menu-item key="12">Central Govt. Entrance Exam</a-menu-item>
                  <a-menu-item key="12">Private Organization EE</a-menu-item>
                  <a-menu-item key="12">School EE</a-menu-item>
                  <a-menu-item key="12">Other EE</a-menu-item>
                </a-sub-menu>
                <a-sub-menu key="sub3">
                  <span slot="title">
                    <a-icon type="exam" />Configuration(Settings)
                  </span>
                  <a-menu-item key="11">Talents</a-menu-item>
                  <a-menu-item key="12">Sports</a-menu-item>
                  <a-menu-item key="12">Any other physical activities</a-menu-item>
                </a-sub-menu>
              </a-sub-menu>
            </a-sub-menu>
            <a-sub-menu key="sub2">
              <span slot="title">
                <a-icon type="laptop" />Tour
              </span>
              <a-menu-item key="5"></a-menu-item>
            </a-sub-menu>
            <a-sub-menu key="sub2">
              <span slot="title">
                <a-icon type="laptop" />Market E-Commerce
              </span>
              <a-menu-item key="5"></a-menu-item>
            </a-sub-menu>
            <a-sub-menu key="sub2">
              <span slot="title">
                <a-icon type="laptop" />Job Details
              </span>
              <a-menu-item key="5"></a-menu-item>
            </a-sub-menu>
            <a-sub-menu key="sub2">
              <span slot="title">
                <a-icon type="laptop" />Bank Details
              </span>
              <a-menu-item key="5"></a-menu-item>
            </a-sub-menu>
            <a-sub-menu key="sub2">
              <span slot="title">
                <a-icon type="laptop" />News Students EO
              </span>
              <a-menu-item key="5"></a-menu-item>
            </a-sub-menu>
            <a-sub-menu key="sub2">
              <span slot="title">
                <a-icon type="laptop" />Talents
              </span>
              <a-menu-item key="5"></a-menu-item>
            </a-sub-menu>
            <a-sub-menu key="sub2">
              <span slot="title">
                <a-icon type="laptop" />Sports
              </span>
              <a-menu-item key="5"></a-menu-item>
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
            <h1 key="1">content</h1>
          </div>
        </a-layout-content>
      </a-layout>
    </a-layout>
  </div>
</template>

<style>
#components-layout-demo-top-side .logo {
  width: 120px;
  height: 31px;
  background: rgba(255, 255, 255, 0.2);
  margin: 16px 28px 16px 0;
  float: left;
}
</style>
