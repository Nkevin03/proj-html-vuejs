<template>
  <main>
      <section class="john">
        <div class="presentation">
            <h2>Hey there, my name is John Doe. I'm the founder of the Brain Academy.</h2>
            <div>
                <img src="@/assets/img/sign.jpg" alt="">
            </div>
        </div>
        <div class="text-presentation">
            <p>A wonderful serenity has taken possession of my entire soul, like these sweet mornings of spring which I enjoy with my whole heart. I am alone, and feel the charm of existence in this spot, which was created for the bliss of souls like mine. I am so happy, my dear friend, so absorbed in the exquisite sense of mere tranquil existence, that I neglect my talents. When, while the lovely valley teems with vapour around me, and the meridian sun strikes the upper surface of the impenetrable foliage of my trees, and but a few stray gleams steal into the inner sanctuary</p>
        </div>
      </section>
  </main>
</template>

<script>
export default {
    name: 'Main'
}
</script>

<style scoped lang="scss">
@import '@/styles/preset.scss';
    main{
        margin-top: 200px;

        .john{
            display: flex;
            width: 65%;
            margin: 0 auto;

            .presentation{
                width: 50%;

                h2{
                    color: $black;
                    font-size: 35px;
                    padding: 25px;
                    line-height: 50px;
                }

                div{
                    display: flex;
                    justify-content: center;
                }
            }
            
            .text-presentation{
                width: 50%;

                p{
                    color: $black;
                    font-size: 16px;
                    line-height: 40px;
                    padding: 25px;
                    font-weight: 300;
                }
            }
        }
    }
</style>