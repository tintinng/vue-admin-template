<!--  -->
<template>
  <div class="app-container">
      <el-row>
          <span style="margin: 20px 0;">Prediction of protein amphiphilic helix:</span>
          <div class="res">
              <span>{{ this.res }}</span>
              <div>325556555544444412222322221233410000023344321212213445587755</div>
              <div>544445543455451122111333222334322222233333344444423333333445</div>
              <div>423365433333445245544321233233331110111012111000233112221001</div>
              <div>010123332212234559888877788999898777765555444554445556667665</div>
              <div>433444455523223445555432433333333445546452231122245532111212</div>
              <div>232212344323231123344332332322442210043433456652221233321332</div>
              <div>100121113432102100010001332210000222234322000012111222222211</div>
              <div>122133322211222113222201000000000000000000000000011111223112</div>
              <div>242556554577766544444444455666555543333333422453222222222211</div>
              <div>221244333445122323222222323565422222234577665533345556664344</div>
              <div>430122222221122232100000013122221111000000001200012220002121</div>
              <div>211111112345987665445455645665654441112333334334665433333334</div>
              <div>466765467778888333122100000000111122333433434322211122244322</div>
              <div>222224587866653443333442222344543432323432102111232221222212</div>
              <div>333445433223322222111232222122222432200011223332200000100000</div>
          </div>
      </el-row>
      <el-row>
        <span style="margin: 20px 0;">Amphiphilic helix position info:</span>
        <el-table
        :data="list"
        element-loading-text="Loading"
        border
        >
            <el-table-column align="center" label="position:">
                <template slot-scope="scope">{{ scope.row.position }}</template>
            </el-table-column>
            <el-table-column align="center" label="score">
                <template slot-scope="scope">{{ scope.row.score }}</template>
            </el-table-column>
            <el-table-column align="center" label="H1">
                <template slot-scope="scope">{{ scope.row.h1 }}</template>
            </el-table-column>
            <el-table-column align="center" label="H2">
                <template slot-scope="scope">{{ scope.row.h2 }}</template>
            </el-table-column>
            <el-table-column align="center" label="P1">
                <template slot-scope="scope">{{ scope.row.p1 }}</template>
            </el-table-column>
            <el-table-column align="center" label="P2">
                <template slot-scope="scope">{{ scope.row.p2 }}</template>
            </el-table-column>
            <el-table-column align="center" label="N1">
                <template slot-scope="scope">{{ scope.row.n1 }}</template>
            </el-table-column>
            <el-table-column align="center" label="N2">
                <template slot-scope="scope">{{ scope.row.n2 }}</template>
            </el-table-column>
        </el-table>
        <el-button type="primary" @click="confirm" style="float: right;margin: 2%;">confirm</el-button>
      </el-row>
  </div>
</template>

<script>
export default {
    data() {
        return {
            res: `>sp|Q8CD54|PIEZ2_MOUSE Piezo-type mechanosensitive ion channel component 2 OS=Mus musculus OX=10090 GN=Piezo2 PE=1 SV=2`,
            list: [
                { position: '55-65', score: 8, h1:1.17, h2:-1.11, p1:0.08, p2:0.08, n1:4, n2:5 },
                { position: '202-211', score: 8, h1:1.17, h2:-1.34, p1:0.08, p2:0.07, n1:4, n2:5 },
                { position: '204-213', score: 9, h1:1.08, h2:-1.23, p1:0.06, p2:0.1, n1:5, n2:5 },
                { position: '616-625', score: 8, h1:1.39, h2:-1.07, p1:0.08, p2:0.08, n1:5, n2:5 },
                { position: '1202-1211', score: 8, h1:1.14, h2:-0.98, p1:0.07, p2:0.06, n1:5, n2:5 }
            ]
        }
    },
    methods: {
        confirm() {
            this.$router.push({ name: 'Input' })
        }
    }
}
</script>

<style lang="scss" scoped>
.el-row {
    margin-bottom: 20px;
    &:last-child {
        margin-bottom: 0;
    }
}

.res {
    padding: 2%;
    border: 1px solid gray;
}

.app-container {
  padding: 32px;
  background-color: rgb(249, 250, 252);
  position: relative;
}
</style>
