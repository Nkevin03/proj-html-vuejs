<template>
  <section class="slider">
    <div class="slider-title">
        <h3>What Studenents Say</h3>
    </div>
    <div class="image-slide">
        <div class="arrow-left">
            <i class="fas fa-arrow-left"></i>
        </div>
        <div class="images-slider">
            <img src="../assets/img/1-100x100.jpg" alt="">
            <img src="../assets/img/2-100x100.jpg" alt="">
            <img src="../assets/img/4-100x100.jpg" alt="">
        </div>  
        <div class="arrow-right">
            <i class="fas fa-arrow-right"></i>
        </div>
    </div>
    <div class="stars">
            <h4>Paints of the Future</h4>
            <div>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
            </div>
            <p>The response to your MasterStudy has been really overwhelming! Those who participated in the workshop are spreading the word here on campus and the "buzz" is on. The VP of Instruction wants you to come back! Her goal is to have more faculty trained. She also wants to attend a workshop herself. Our President told me Masterstudy needs to be the cornerstone of our success program."</p>
        </div>
  </section>
</template>

<script>

export default {
    name: 'Slider'
}
</script>

<style scoped lang="scss">
@import '@/styles/preset.scss';
    .slider{
        width: 55%;
        margin: 0 auto;
        padding: 60px 0;

        .slider-title{

            h3{
                text-align: center;
                font-weight: 700;
                font-size: 50px;
                padding-bottom: 50px;
            }
        }
        .image-slide{
            display: flex;
            align-items: center;
            justify-content: space-around;

            i{
                cursor: pointer;
            }

            img{
                border-radius: 100%;
                margin: 0 10px;

                &:first-child{
                    width: 80px;
                }
                &:last-child{
                    width: 80px;
                }
            }
        }
        .stars{
            display: flex;
            justify-content: center;
            flex-direction: column;
            align-items: center;
            padding: 20px 0;

            i{
                color: $buttercup;
            }

            p{
                padding: 20px 0;
                text-align: center;
                color: $abbey;
                line-height: 30px;
                font-size: 18px;
            }
        }
    }
</style>