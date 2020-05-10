<template>
  <div class="main" style="background-color: #ececec; padding: 20px;">
    <a-row :gutter="16">
      <a-col :span="8">
        <a href="/register">
          <a-card hoverable style="width: 350px">
            <img slot="cover" alt="example" src="img/student.jpg" />
            <a-card-meta title="STUDENT">
              <template slot="description">www.instagram.com</template>
            </a-card-meta>
          </a-card>
        </a>
      </a-col>
      <a-col :span="8">
        <a href="/register">
          <a-card hoverable style="width: 400px">
            <img slot="cover" alt="example" src="img/parent.jpg" />
            <a-card-meta title="PARENT">
              <template slot="description">www.instagram.com</template>
            </a-card-meta>
          </a-card>
        </a>
      </a-col>
      <a-col :span="8">
        <a href="/register">
          <a-card hoverable style="width: 350px">
            <img slot="cover" alt="example" src="img/student.jpg" />
            <a-card-meta title="ORGANISATION">
              <template slot="description">www.instagram.com</template>
            </a-card-meta>
          </a-card>
        </a>
      </a-col>
    </a-row>
  </div>
</template>
