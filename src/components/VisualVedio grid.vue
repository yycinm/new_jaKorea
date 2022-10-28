<template>
  <div class="wrapper">
    <div class="video">
      <video src="images/main-home-01-2.mp4" autoplay loop></video>
    </div>

    <div class="text">
      <h3>우리 청소년들이 미래의 인재로 성장하도록</h3>
      <p>JA KOREA가 함께합니다.</p>
    </div>
  </div>

  <!-- <div class="Vvvedio mb-5">
    
    <div class="container">
        <div class="row">

            <div class="VeTitle">
              <p>우리 청소년들이 미래의 인재로 성장하도록</p>
              <strong class="display-1 display-md-6 fw-bold">JA KOREA가 함께합니다.</strong>
                <div class="Vebtn">
                  <a href="#"> 자세히 보기 →   </a>
                </div>
            </div>
      </div>
    </div>
    <video class="vvedio" autoplay loop>
      <source src="images/main-home-01-2.mp4" type="" />
    </video>
  </div> -->
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.wrapper {
  height: 80vh;
  position: relative;
  overflow: hidden;

  .video {
    position: absolute;
    z-index: -1;

      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    video {
     
    }
  }

  .text {
    height: 100%;

    display: grid;
    grid-template-columns: repeat( 12, 1fr);
    grid-template-rows: repeat( 12, 1fr );

    h3 {
      grid-column: 3 / span 8;
      grid-row: 3 / span 8;
      color: #FFFFFF;font-size: 38px;

    }
    p {
      grid-column: 3 / span 8;
      grid-row: 6 / span 5;
      color: #FFFFFF;font-size: 75px;
    }
  }
}
</style>