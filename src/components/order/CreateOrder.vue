<template>
    <el-row>
        <el-col :span="12">
            <el-container>
                <el-header>
                    <el-row>
                        <el-col :span="24"> <p>货物信息</p> </el-col>
                    </el-row>
                </el-header>
                <el-main>
                    <el-row>
                        <el-col :span="24">
                            <el-form ref="form" :model="form" label-width="110px">
                                <el-form-item label="货物名称">
                                    <el-input v-model="form.name"></el-input>
                                </el-form-item>
                                <el-form-item label="货物重量">
                                    <el-input v-model="form.name"></el-input>
                                </el-form-item>
                                <el-form-item label="货物信息">
                                    <el-input v-model="form.name"></el-input>
                                </el-form-item>
                                <el-form-item label="接受签收时间段">
                                    <el-col :span="11">
                                    <el-date-picker type="date" placeholder="选择日期" v-model="form.date1" style="width: 100%;"></el-date-picker>
                                    </el-col>
                                    <el-col class="line" :span="2">-</el-col>
                                    <el-col :span="11">
                                    <el-time-picker placeholder="选择时间" v-model="form.date2" style="width: 100%;"></el-time-picker>
                                    </el-col>
                                </el-form-item>
                                <el-form-item label="预估距离">
                                    <el-input v-model="form.name"></el-input>
                                </el-form-item>
                                <el-form-item label="出价">
                                    <el-input v-model="form.name"></el-input>
                                </el-form-item>
                                <el-form-item>
                                    <el-button type="primary" @click="onSubmit">立即创建</el-button>
                                    <el-button>取消</el-button>
                                </el-form-item>
                            </el-form>
                        </el-col>
                    </el-row>
                </el-main>
            </el-container>
        </el-col>
        <el-col :span="12">
            <div class="grid-content bg-purple-dark">
                <el-row>
                    <el-col :span="24">
                        <el-container>
                <el-header>
                    <el-row>
                        <el-col :span="24"> <p>寄件人信息</p> </el-col>
                    </el-row>
                </el-header>
                <el-main>
                    <el-row>
                        <el-col :span="24">
                            <el-form ref="form" :model="form" label-width="100px">
                                <el-form-item label="寄件人姓名">
                                    <el-input v-model="form.name"></el-input>
                                </el-form-item>
                                <el-form-item label="寄件人地址">
                                    <el-input v-model="form.name"></el-input>
                                </el-form-item>
                                <el-form-item label="寄件人手机号">
                                    <el-input v-model="form.name"></el-input>
                                </el-form-item>
                                <el-form-item>
                                    <el-button type="primary" @click="onSubmit">立即创建</el-button>
                                    <el-button>取消</el-button>
                                </el-form-item>
                            </el-form>
                        </el-col>
                    </el-row>
                </el-main>
            </el-container>
                    </el-col>
                </el-row>
            </div>
            <div class="grid-content bg-purple">
                <el-row>
                    <el-col :span="24">
                        <el-container>
                <el-header>
                    <el-row>
                        <el-col :span="24"> <p>收件人信息</p> </el-col>
                    </el-row>
                </el-header>
                <el-main>
                    <el-row>
                        <el-col :span="24">
                            <el-form ref="form" :model="form" label-width="100px">
                                <el-form-item label="收件人姓名">
                                    <el-input v-model="form.name"></el-input>
                                </el-form-item>
                                <el-form-item label="收件人地址">
                                    <el-input v-model="form.name"></el-input>
                                </el-form-item>
                                <el-form-item label="收件人手机号">
                                    <el-input v-model="form.name"></el-input>
                                </el-form-item>
                                <el-form-item>
                                    <el-button type="primary" @click="onSubmit">立即创建</el-button>
                                    <el-button>取消</el-button>
                                </el-form-item>
                            </el-form>
                        </el-col>
                    </el-row>
                </el-main>
            </el-container>
                    </el-col>
                </el-row>
            </div>
        </el-col>
    </el-row>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          name: '',
          region: '',
          date1: '',
          date2: '',
          delivery: false,
          type: [],
          resource: '',
          desc: ''
        }
      }
    },
    methods: {
      onSubmit() {
        console.log('submit!');
      }
    }
  }
</script>

<style>
  .el-col {
    border-radius: 4px;
  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-purple {
    background: #0e54a4;
  }
  .bg-purple-light {
    background: #c30a51;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
</style>