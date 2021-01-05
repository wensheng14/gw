<template>
  <nav>
    <ul class="w">
      <li v-for="(item, index) in data" :key="index">
        <template v-if="item.sub">
          <el-dropdown>
            <span class="el-dropdown-link">
              {{ item.title }}
            </span>
            <el-dropdown-menu slot="dropdown">
              <el-dropdown-item v-for="item in item.sub" :key="item.id">
                <a href="#">{{item.name}}</a>
              </el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
        </template>
        <template v-else>
          <a href="#">{{ item.name }}</a>
        </template>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      data: [
        {
          id: 1,
          path: "",
          name: "首页",
        },
        {
          id: 2,
          path: "",
          title: "学校概况",
          sub: [
            {
              id: 21,
              path: "",
              name: "学校简介",
            },
            {
              id: 22,
              path: "",
              name: "办学优势",
            },
            {
              id: 23,
              path: "",
              name: "学校架构",
            },
            {
              id: 24,
              path: "",
              name: "学校领导",
            },
            {
              id: 25,
              path: "",
              name: "学校荣誉",
            },
            {
              id: 26,
              path: "",
              name: "校园风景",
            },
            {
              id: 27,
              path: "",
              name: "教育质量报告",
            },
          ],
        },
        {
          id: 3,
          path: "",
          name: "教学管理",
        },
        {
          id: 4,
          path: "",
          name: "学生工作",
        },
        {
          id: 5,
          path: "",
          title: "招生就业",
          sub: [
            {
              id: 51,
              path: "",
              name: "招生工作",
            },
            {
              id: 52,
              path: "",
              name: "就业工作",
            },
          ],
        },
        {
          id: 6,
          path: "",
          title: "党团建设",
          sub: [
            {
              id: 61,
              path: "",
              name: "党建工作",
            },
            {
              id: 62,
              path: "",
              name: "团委工作",
            },
          ],
        },
        {
          id: 7,
          path: "",
          name: "校企合作",
        },
        {
          id: 8,
          path: "",
          name: "人事管理",
        },
        {
          id: 9,
          path: "",
          name: "联系我们",
        },
      ],
    };
  },
  methods: {},
};
</script>

<style>
/* 引入初始化 */
@import url("../../assets/CSS/init.css");
/* nav 背景 */
nav {
  background-color: #eee;
  height: 42px;
}

nav ul {
  display: flex;
  justify-content: space-between;
  height: 42px;
  line-height: 42px;
}
/* 设置下拉菜单跟a标签的样式 */
nav a,
.el-dropdown-link {
  display: inline-block;
  width: 132px;
  color: #333;
  text-align: center;
  line-height: 42px;
}
/* 鼠标移入的效果 */
nav a:hover,
.el-dropdown-link:hover {
  background-color: #ddd;
}
/* 下拉菜单添加小手 */
.el-dropdown-link {
  cursor: pointer;
}
</style>