<template>

    <div class="common-layout">
      <el-container>
        <el-aside width="200px">

          <el-menu
              default-active="2"
              class="el-menu-vertical-demo"
              @open="handleOpen"
              @close="handleClose"
          >
            <el-sub-menu index="1">
              <template #title>
                <el-icon><location /></el-icon>
                <span>Navigator One</span>
              </template>
              <el-menu-item-group title="Group One">
                <el-menu-item index="1-1">
                  <router-link :to="`/`">数据管理</router-link>
                </el-menu-item>
                <el-menu-item index="1-2">
                  <router-link :to="`/room`">数据管理11</router-link>
                </el-menu-item>
              </el-menu-item-group>
<!--              <el-menu-item-group title="Group Two">
                <el-menu-item index="1-3">item three</el-menu-item>
              </el-menu-item-group>
              <el-sub-menu index="1-4">
                <template #title>item four</template>
                <el-menu-item index="1-4-1">item one</el-menu-item>
              </el-sub-menu>-->
            </el-sub-menu>
<!--            <el-menu-item index="2">
              <el-icon><icon-menu /></el-icon>
              <span>Navigator Two</span>
            </el-menu-item>
            <el-menu-item index="3" disabled>
              <el-icon><document /></el-icon>
              <span>Navigator Three</span>
            </el-menu-item>
            <el-menu-item index="4">
              <el-icon><setting /></el-icon>
              <span>Navigator Four</span>
            </el-menu-item>-->
          </el-menu>

        </el-aside>
        <el-main>

<!--          <nav>
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/room">About</RouterLink>
          </nav>
          <div class="logo-box">
            <img style="height:140px;" src="./assets/electron.png" >
            <span/>
            <img style="height:140px;" src="./assets/vite.svg" >
            <span/>
            <img style="height:140px;" src="./assets/vue.png" >
          </div>
          &lt;!&ndash;  <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />&ndash;&gt;
          <div class="static-public">
            Place static files into the <code>/public</code> folder
            <img style="width:77px;" :src="'./node.png'" >
          </div>-->

          <!-- 路由出口 -->
          <router-view />

        </el-main>
      </el-container>
    </div>


</template>

<script lang="ts" setup>
import {
  Document,
  Menu as IconMenu,
  Location,
  Setting,
} from '@element-plus/icons-vue'
const handleOpen = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
const handleClose = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
</script>

<style>
/*#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}*/

.logo-box {
  display: flex;
  width: 100%;
  justify-content: center;
}
.logo-box span {
  width: 74px;
}
.static-public {
  display: flex;
  align-items: center;
  justify-content: center;
}
.static-public code {
  background-color: #eee;
  padding: 2px 4px;
  margin: 0 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
