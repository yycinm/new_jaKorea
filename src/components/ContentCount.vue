<template>
  <div class="countBg py-5 mb-5">
    <div class="container">
      <div class="row">
        <div class="col-12 col-md-4 p-5">
          <img src="images/main-number-1.jpg" alt="" class="img-fluid" />
        </div>
        <div class="col-12 col-md-8 p-5">
          <div class="couBar">
            <div class="bars d-flex">
              <div class="bar"></div>
              <div class="barCount"><h2>+200</h2></div>
            </div>
            <div class="barTitle d-flex">
              <h5>지역 네트워크</h5>
              <h6>전국 17개 시도 200개이상의 지역에서 교육하고 있습니다.</h6>
            </div>
          </div>
          <div class="couBar">
            <div class="bars d-flex">
              <div class="bar"></div>
              <div class="barCount"><h2>+1000</h2></div>
            </div>
            <div class="barTitle d-flex">
              <h5>학교 및 기관</h5>
              <h6>전국 1,000여개 학교 및 기관, 단체와 협업하여 교육을 진행합니다.</h6>
            </div>
          </div>
          <div class="couBar">
            <div class="bars d-flex">
              <div class="bar"></div>
              <div class="barCount"><h2>+3000</h2></div>
            </div>
            <div class="barTitle d-flex">
              <h5>교육 진행자</h5>
              <h6>3,000여명의 전문 지식을 갖춘 봉사자와 교사, 강사가 함께 교육을 진행하고 있습니다.</h6>
            </div>
          </div>
          <div class="couBar">
            <div class="bars d-flex">
              <div class="bar"></div>
              <div class="barCount"><h2>+90000</h2></div>
            </div>
            <div class="barTitle d-flex">
              <h5>교육 수혜자</h5>
              <h6>전국 90,000여명의 청소년들이 교육 프로그램에 참여합니다.</h6>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.countBg {
  background: linear-gradient(270deg, #1c5663 2.45%, #06afbc 100%);
  width: 100%;
  height: 100%;
  .couBar{height:25%;}
  .bars{
    width: 100%;height: 50%;display: flex;justify-content: center;align-items: center;
    .barCount{height: 100%;
        h2{font-size: 30px;color: white;}
    }
      .bar{width: 90%;height: 6px;background: #00A0AF;margin-right: 20px;
      border-radius: 2px;}
  }
  .barTitle{
    width: 100%;height: 50%;
    h5{font-size: 16px;color: #fff;margin-right: 30px;height: 100%;line-height: 100%;font-weight: bold;}
    h6{font-size: 14px;color: white; opacity: 0.8;height: 100%;line-height: 100%;}
  }
}
</style>