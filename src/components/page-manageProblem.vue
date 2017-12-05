<template>
  <div>
    <myheader></myheader>
    <div class="path">
      <div class="path-wrap">
        <span>管理者页面</span>
      </div>
    </div>
    <div class="body d-flex">
      <div class="body-width">
        <!-- 主体框 -->
        <!--manageP是为管理题目的意思-->

        <div id="manageP" class="mainbody">
          <h1>Problem List</h1><br>
          <table id="pList" class="table table-hover table-striped" style="width: 800px;">

            <thead>

            <tr>
              <th>ID</th>
              <th>Problem</th>
              <th>Time</th>
              <th>Master</th>
              <th>Pass Time</th>
              <th></th>
            </tr>
            </thead>
            <tbody>
            <tr>
              <td>xYM</td>
              <td>Problem1</td>
              <td>xym</td>
              <td>xYM</td>
              <td width="100">xYM</td>
              <td width="200">
                <router-link to="/entrying">
                  <button class="btn"
                          style="background-color: deepskyblue;color: white">Change
                  </button>
                </router-link>&nbsp;&nbsp;
                <button class="btn" onclick="subShow()"
                        style="background-color:#5cb85c;color: white">Submitte
                </button>
              </td>
            </tr>
            <tr>
              <td>xYM</td>
              <td>xym</td>
              <td>xym</td>
              <td>xYM</td>
              <td>xYM</td>
              <td>
                <router-link to="/entrying">
                  <button class="btn"
                          style="background-color: deepskyblue;color: white">Change
                  </button>
                </router-link>&nbsp;&nbsp;
                <button class="btn" onclick="subShow()"
                        style="background-color:#5cb85c;color: white">Submitte
                </button>
              </td>
            </tr>
            <tr>
              <td>xYM</td>
              <td>xym</td>
              <td>xym</td>
              <td>xYM</td>
              <td>xYM</td>
              <td>
                <router-link to="/entrying">
                  <button class="btn"
                          style="background-color: deepskyblue;color: white">Change
                  </button>
                </router-link>&nbsp;&nbsp;
                <button class="btn" onclick="subShow()"
                        style="background-color:#5cb85c;color: white">Submitte
                </button>
              </td>
            </tr>
            </tbody>
          </table>
        </div>

        <!--这块是已提交题目-->
        <div id="subList">
          <h1>Submitted List</h1>
          <table class="table table-hover table-striped" style="width: 800px">
            <thead>
            <tr>
              <th>ID</th>
              <th>Time</th>
              <th>Master</th>
              <th>Result</th>
              <th></th>
            </tr>
            </thead>
            <tbody>
            <tr>
              <td>xYM</td>
              <td>xym</td>
              <td>xym</td>
              <td>xYM</td>
              <td>
                <button class="btn"
                        style="background-color: deepskyblue;color: white">Detail
                </button>
                &nbsp;&nbsp;
                <button class="btn"
                        style="background-color:#5cb85c;color: white">Recycle
                </button>
              </td>
            </tr>
            </tbody>

          </table>

        </div>
        <!--<input type="number">-->
        <!-- 侧边栏 -->
        <div class="asidebar">
          <div>
            <h5 class="title-size">通用</h5>
            <ul style="padding: 0px">
              <li class="li-hover li-style"><a>用户管理</a></li>
            </ul>
          </div>
          <div>
            <h5 class="title-size">题目</h5>
            <ul style="padding: 0px">
              <li class="li-hover li-style"><a href="http://localhost:8080/#/manageProblem">题目列表</a></li>
              <li class="li-hover li-style"><a href="http://localhost:8080/#/entrying">创建题目</a></li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <myfooter></myfooter>
    <script type="application/javascript">
      var s1 = document.getElementById("subList");

      function subShow() {
        s1.style.display = "block"

      }

    </script>
  </div>

</template>

<script>


  import myheader from './app/app-header.vue'
  import myfooter from './app/app-footer.vue'

  export default {
    name: 'entrying',
    data() {
      return {}
    },
    methods: {},
    components: {
      myheader,
      myfooter
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /*#pList th {*/
  /*width: 150px;*/
  /*font-size: x-large;*/
  /*}*/
  #subList {
    display: none;
    width: 70%;
    float: right;
    padding-left: 10px;
    padding-right: 10px;
  }

  #pList td {
    height: 10px;
  }

  #pList {
    padding: 0px;
    /*padding-bottom: 0px;*/
    /*padding-top: 60px;*/
  }

  #pList button {
    background-color: deepskyblue;
  }

  .body {
    margin: 0 0 65px 0;
  }

  .ip-pad {
    padding: 5px 10px;
  }

  .pull-left {
    float: left;
  }

  .pull-right {
    float: right;
  }

  .col-md-width {
    width: 100%;
  }

  .fontWeight {
    font-weight: normal;
  }

  .pdr {
    padding-right: 20px;
  }

  .mgb {
    margin-bottom: 10px;
  }

  .mgb2 {
    margin-bottom: 20px;
  }

  .pad {
    padding: 10px 10px 10px 0px;
  }

  .pad1 {
    padding: 6px;
  }

  .path {
    height: 65px;
    width: 100%;
    /*background-color: royalblue;*/
    border-bottom: 1px solid #e0e4e8;
    padding-left: 20px;
  }

  .path-wrap {
    width: 1440px;
    margin: 0 auto;
    line-height: 65px;
    color: #979faf;
  }

  .d-flex {
    display: flex;
    justify-content: center;
  }

  .body-width {
    width: 1440px;
    margin-top: 20px;
    font-weight: bold;
  }

  .mainbody {
    width: 70%;
    float: right;
    padding-left: 10px;
    padding-right: 10px;
  }

  .general-style {
    padding-left: 10px;
    padding-right: 10px;
    margin-bottom: 20px;
  }

  .input {
    font-weight: normal;
    font-size: 16px;
    width: 100%;
    height: 300px;
    resize: none;
    line-height: 1.6;
  }

  .input1 {
    font-weight: normal;
    font-size: 16px;
    width: 100%;
    height: 130px;
    line-height: 1;
  }

  .panel {
    border: 1px solid #a8a6a7;
    border-radius: 2px;

  }

  .panel-body {
    padding: 20px;
  }

  .asidebar {
    width: 30%;
    padding-right: 10px;
  }

  ul li {
    list-style-type: none;
    display: block;
  }

  .li-style {
    font-size: 15px;
    padding: 8px 20px;
    position: relative;
    display: block;
    color: black;
  }

  .li-hover:hover {
    background-color: #ebe9ea;
    width: 50%;
  }

  .title-size {
    font-size: large;
  }

  a {
    text-decoration: none;
    cursor: pointer;
  }

  a:visited {
    border-left: 3px solid #4691f6;
  }
</style>
