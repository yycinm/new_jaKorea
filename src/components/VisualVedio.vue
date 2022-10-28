<template>
  <div class="Vvvedio mb-5">
    
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
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.Vvvedio {
  width: 100%;
  height: 881px;
  overflow: hidden;
  .vvedio {
    width: 100%;
  }
  .container{ 
    position: relative;
    .VeTitle{
        position: absolute; top: 50%;height: 100%;transform:translateY(-50%)
        p{
            font-size: 36px;background: #00BEC6;color:white;
            width: 82%;padding: 0px 0px 0px 3px;font-weight: lighter;
        }
        strong{
            color:white;_font-size: 75px;margin-bottom: 100px;
        }
        .Vebtn{
            
            display: flex;justify-content: center;align-items: center;
            width: 200px;padding: 20px;    background-image: linear-gradient( -45deg,#00a0af,#00c0ca, #008b9c, #28708b,#285f74,#285f74,#28708b, #008b9c,#00c0ca,#00a0af);border-radius: 30px;
            a{color:white;
            &:hover{
                background: white;color: #00BEC6;width: 100%;height: 100%;
            }
            }


        }
    }
  }
}
</style>