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
        <!--sendP是为提交题目的意思-->
        <div class="mainbody" id="sendP">
          <div class="general-style">
            <div class="mgb">
              <span class="title-size">题目标题</span>
            </div>
            <div>
              <input type="text" name="title" class="col-md-width fontWeight ip-pad" required autofocus>
            </div>
          </div>
          <div class="general-style">
            <div class="mgb">
              <span class="title-size">题目描述</span>
            </div>
            <div>
              <textarea name="description" class="input ip-pad" required></textarea>
            </div>
          </div>
          <div class="general-style">
            <div class="pull-left mgb2" style="width: 50%;padding-right: 10px;">
              <div class="mgb">
                <span class="title-size">时间限制<span style="font-size: 16px;">（ms，1-10000ms）</span></span>
              </div>
              <div>
                <input type="number" class="col-md-width ip-pad" required/>
              </div>
            </div>
            <div class="pull-right mgb2" style="width: 50%;padding-left: 10px;">
              <div class="mgb">
                <span class="title-size">内存限制<span style="font-size: 16px;"> ( MB, 最低16M, Java不能低于32M )</span></span>
              </div>
              <div>
                <input type="number" class="col-md-width ip-pad" required/>
              </div>
            </div>
          </div>
          <div class="general-style">
            <div class="pull-left mgb2" style="width: 50%;">
              <div class="mgb">
                <span class="title-size">难易度</span>
              </div>
              <div>
                <select name="difficulty" class=" ip-pad" style="width: 150px;" required>
                  <option value="1" selected="selected">Easy</option>
                  <option value="2">Middle</option>
                  <option value="3">Difficult</option>
                </select>
              </div>
            </div>
            <div class="pull-right mgb2" style="width: 50%;padding-left: 10px;">
              <div class="mgb">
                <span class="title-size">标签</span>
              </div>
              <div>
                <input type="text" class="col-md-width ip-pad" required/>
              </div>
            </div>
          </div>
          <div class="general-style">
            <div class="mgb">
              <span class="title-size">输入描述</span>
            </div>
            <div>
              <textarea name="input" class="input1 ip-pad"></textarea>
            </div>
          </div>
          <div class="general-style">
            <div class="mgb">
              <span class="title-size">输出描述</span>
            </div>
            <div>
              <textarea name="output" class="input1 ip-pad" required></textarea>
            </div>
          </div>
          <div class="general-style">
            <div class="mgb">
              <span class="title-size">样例</span>
            </div>
            <div class="panel">
              <div class="panel-body">
                <div class="pull-left pdr" style="width: 50%;">
                  <div>
                    <span class="title-size">样例输入</span>
                  </div>
                  <div>
                    <textarea name="templein" class="input1" required></textarea>
                  </div>
                </div>
                <div class="pull-right pdr" style="width: 50%;">
                  <div>
                    <span class="title-size">样例输出</span>
                  </div>
                  <div>
                    <textarea name="templeout" class="input1" required></textarea>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="general-style">
            <button class="btn btn-success item-btn">
              创建
            </button>
          </div>
        </div>
        <div id="manageP" class="mainbody" style="border: solid;height: 100px;display: none">


        </div>

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
  </div>

</template>
<script>
  //  var s1 = document.getElementById("sendP");
  //  var m1 = document.getElementById("manageP");
  //
  //  function guestShow() {
  //    s1.style.display = "none";
  //    m1.style.display = "block";
  //
  //  }

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

  .body a {
    text-decoration: none;

  }

  .li-style {
    font-size: 15px;
    padding: 8px 20px;
    position: relative;
    display: block;
    color: black;
    text-decoration: none;
  }

  .li-hover:hover {
    background-color: #ebe9ea;
    width: 50%;
    text-decoration: none;

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
