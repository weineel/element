<template>
  <div class="play">
    <el-button @click="drawerVisible = true">
      Show Main Drawer
    </el-button>
    <el-drawer :visible.sync="drawerVisible" title="Main Drawer">
      <el-radio-group v-model="showNumber">
        <el-radio label="1"> Show 1 </el-radio>
        <el-radio label="2"> Show 2 </el-radio>
        <el-radio label="3"> Show 3 </el-radio>
      </el-radio-group>

      <div v-if="showNumber === '1'">
        <el-button @click="dialogVisible = true">
          Show Main Dialog 1
        </el-button>
        <el-dialog :visible.sync="dialogVisible" append-to-body> 1 </el-dialog>
      </div>
      <div v-if="showNumber === '2'">
        2
      </div>
      <div v-if="showNumber === '3'">
        3
      </div>
    </el-drawer>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        drawerVisible: false,
        dialogVisible: false,
        showNumber: '1',
      };
    }
  };
</script>

<style>
  .play {
    margin: 20px;
    height: 2000px
  }
</style>
