<template>
  <div class="Vresult col-12 col-md-6 mb-5">
    <div class="cTitle d-flex">
      <h2 class="mb-5 fw-bolder">결과발표</h2>
      <a href="#">

      <div class="plus">
        <div class="bar01"></div>
        <div class="bar02"></div>
      </div>
      </a>
    </div>
    <div class="cContent">
      <div class="creCon d-flex" v-for="(item, i) in result" :key="i">
        <div class="cCon">
          <strong>{{ item.title }}</strong>
          <p>{{ item.date }}</p>
        </div>
        <div></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["result"],
};
</script>

<style lang="scss" scoped>
body {
  display: block;
}
.Vresult {
  height: 544px;
  overflow: hidden;
  padding: 0 25px;
  h2 {
    font-size: 35px;
  }
}
.cTitle {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
 .cTitle{
    width: 100%;position: relative;margin-bottom: 10px;
  }
    .cTitle:after{
        width: 100%;height: 2px;background: #333;
        content: "";display: block;position: absolute;bottom:10px;
    }
.plus {
  cursor: pointer;
  &:hover .bar01 {
    transform: rotate(90deg);
    background: #333;
  }
  &:hover .bar02 {
    transform: rotate(90deg);
    background: #333;
  }
  width: 40px;
  height: 40px;
  position: relative;
  .bar01 {
    width: 100%;
    height: 1px;
    transition: 0.3s;
    background: #a1a1a1;
    transform: rotate(0deg);
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
  }
  .bar02 {
    width: 1px;
    height: 100%;
    position: absolute;
    transition: 0.3s;
    background: #a1a1a1;
    transform: rotate(0deg);
    left: 50%;
    transform: translateX(-50%);
  }
}
.cContent {
 
    .creCon{border-bottom: 1px solid rgb(128, 127, 127);width: 100%; padding-top: 10px;padding-left: 15px;
    &:hover{box-shadow: 0 0 17px 6px rgb(0 0 0 / 9%);border-radius: 20px;

    }
    }
  .cCon {
    width: 80%;
    height: 100px;
    display: block;
    strong {
      white-space: nowrap;
      overflow: hidden;
      width: 100%;
      height: 50%;
      display: block;
      text-overflow: ellipsis;
      font-size: 22px;
      font-weight: bold;
    }
    p {
      font-size: 16px;
      color: #7f7f7f;
    }
  }
}
</style>