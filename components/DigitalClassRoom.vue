<template>
  <div>
    <a-page-header class="header" title="DigitalClassRoom" />
    <a-page-header class="sub-header">
      <a-dropdown>
        <a class="ant-dropdown-link" @click="e => e.preventDefault()">
          Classroom Unit
          <a-icon type="down" />
        </a>
        <a-menu slot="overlay">
          <a-menu-item>
            <a href="javascript:;">Section</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">Lab/Practicl</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">Assignments</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">Feedback/Comment</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">Share</a>
          </a-menu-item>
        </a-menu>
      </a-dropdown>
      <a-dropdown>
        <a class="ant-dropdown-link" @click="e => e.preventDefault()">
          Online Unit
          <a-icon type="down" />
        </a>
        <a-menu slot="overlay">
          <a-menu-item>
            <a href="javascript:;">Free Vedios</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">Paid Vedio</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">Discovery Vedio</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">Chating With Teacher</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">Complete unit Online/Google</a>
          </a-menu-item>
        </a-menu>
      </a-dropdown>
      <a-dropdown>
        <a class="ant-dropdown-link" @click="e => e.preventDefault()">
          Vedio Lactctures
          <a-icon type="down" />
        </a>
        <a-menu slot="overlay">
          <a-menu-item>
            <a href="javascript:;">Classroom Lectures</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">Topic Discussion</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">Spacial Class/Lab</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">Project/Research</a>
          </a-menu-item>
          <a-menu-item>
            <a href="javascript:;">Life/Film.</a>
          </a-menu-item>
        </a-menu>
      </a-dropdown>
    </a-page-header>
  </div>
</template>

<style>
.header {
  background-color: lightblue;
  color: white;
}
.sub-header {
  margin-left: 90px;
  margin-top: 15px;
  background-color: rgb(3, 3, 27);
  height: 80px;
  width: 850px;
  color: rgb(145, 201, 154);
}
</style>