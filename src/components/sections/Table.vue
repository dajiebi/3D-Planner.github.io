<script lang="ts" setup>

// 表格数据
const tableData = [
{
    model: 'Put Rubbish In Bin',
    params: '100% | 3.6 steps',
    value_a: '90%  | 4.2 steps',
    value_b: '100% | 3.0 steps',
},
{
    model: 'Push Button',
    params: '100% | 1.0 steps',
    value_a: '100% | 1.0 steps',
    value_b: '100% | 2.0 steps',
},
{
    model: 'Open/Tighten Bottle',
    params: '60% | 3.5 steps',
    value_a: '50%  | 2.4 steps',
    value_b: '70% | 2.8 steps',
},
    {
    model: 'Put Vegetables in Basket',
    params: '70% | 9.0 steps',
    value_a: '0%   | *',
    value_b: '90% | 6.0 steps',
},
    {
    model: 'Boil Eggs in a Pan',
    params: '80% | 8.2 steps',
    value_a: '30%  | 3.3 steps',
    value_b: '80% | 4.8 steps',
},
    {
    model: 'Take out an Apple in Drawer',
    params: '50% | 5.0 steps',
    value_a: '0%   | *',
    value_b: '90% | 4.0 steps',
},
    {
    model: 'ALL',
    params: '76.7% | 5.1 steps',
    value_a: '46.7% | *',
    value_b: '88.3% | 3.8 steps',
},
]
const tableData2 = [
{
    model: 'Grasp (25 trials)',
    params: '36%',
    value_a: '90%  | 4.2 steps',
    value_b: '88%',
},
{
    model: 'Place (25 trials)',
    params: '84%',
    value_a: '100% | 1.0 steps',
    value_b: '80%',
},
{
    model: 'Rotate',
    params: '100%',
    value_a: '50%  | 2.4 steps',
    value_b: '100%',
},
    {
    model: 'Open',
    params: '50%',
    value_a: '0%   | *',
    value_b: '70%',
},
    {
    model: 'Close',
    params: '30%',
    value_a: '30%  | 3.3 steps',
    value_b: '40%',
},
]
const tableData3 = [
{
    model: 'Put Rubbish In Bin',
    params: '90%',
    value_a: '50%',
    value_b: '90%',
},
{
    model: 'Push Button',
    params: '80%',
    value_a: '70%',
    value_b: '90%',
},
{
    model: 'Open/Tighten Bottle',
    params: '60%',
    value_a: '40%',
    value_b: '70%',
},
    {
    model: 'Put Vegetables in Basket',
    params: '40%',
    value_a: '0%',
    value_b: '70%',
},
    {
    model: 'Boil Eggs in a Pan',
    params: '40%',
    value_a: '20%',
    value_b: '60%',
},
    {
    model: 'Take out an Apple in Drawer',
    params: '20%',
    value_a: '0%',
    value_b: '60%',
},
    {
    model: 'ALL',
    params: '55.0%',
    value_a: '30.0%',
    value_b: '76.7%',
},
]
</script>

<template>
    <div>
        <el-divider />

        <el-row justify="center">
            <h1 class="section-title">More Results</h1>
        </el-row>
        <!-- 数据表格 -->
        <el-row justify="center">
            <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
                <!-- 卡片 -->
                <el-card class="card">
                    <!-- 默认tab -->
                    <el-tabs class="demo-tabs" model-value="High-level Planning">

                    <!-- 第一个tab -->
                    <el-tab-pane label="High-level Planning" name="High-level Planning">

                        <!-- 表格数据 -->
                        <el-table 
                            :data="tableData"
                            :default-sort="{ prop: 'value_b', order: 'descending' }"
                            scrollbar-always-on
                        >
                            <el-table-column prop="model" label="Task" width="220" sortable/>
                            <el-table-column prop="params" label="Voxposer" min-width="120" sortable/>
                            <el-table-column prop="value_a" label="SayCan" min-width="120" sortable/>
                            <el-table-column prop="value_b" label="Ours" min-width="120" sortable/>
                        </el-table>
                    </el-tab-pane>

                    <el-tab-pane label="Low-level Skills" name="Low-level Skills">
                        <el-table
                            :data="tableData2"
                            :default-sort="{ prop: 'value_b', order: 'descending' }"
                            scrollbar-always-on
                        >
                            <el-table-column prop="model" label="Task" width="220" sortable/>
                            <el-table-column prop="params" label="Voxposer" min-width="120" sortable/>
                            <el-table-column prop="value_b" label="Ours" min-width="120" sortable/>
                        </el-table>
                    </el-tab-pane>

                    <el-tab-pane label="Success rate Comparison" name="Success rate Comparison">
                        <el-table
                            :data="tableData3"
                            :default-sort="{ prop: 'value_b', order: 'descending' }"
                            scrollbar-always-on
                        >
                            <el-table-column prop="model" label="Task" width="220" sortable/>
                            <el-table-column prop="params" label="Voxposer" min-width="120" sortable/>
                            <el-table-column prop="value_a" label="SayCan" min-width="120" sortable/>
                            <el-table-column prop="value_b" label="Ours" min-width="120" sortable/>
                        </el-table>
                    </el-tab-pane>

                    </el-tabs>

                </el-card>
            </el-col>
        </el-row>

    </div>
</template>

<style scoped>
.card {
    margin-top: 20px;
}
</style>
  