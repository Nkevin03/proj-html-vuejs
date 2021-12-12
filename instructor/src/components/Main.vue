<template>
  <main>
      <!-- John -->
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
      <!-- New courses -->
      <section  class="courses">
          <div class="title-courses">
              <h3>New Courses</h3>
            </div>
          <div class="card-courses">
            <div class="card row col-4" v-for="card in CardInfo" :key="`${card.text}`">
                <div class="card-img">
                    <img :src="card.image">
                </div>
                <div class="card-content">
                    <div class="card-text">
                    <h4>{{card.title}}</h4>
                    <p>{{card.subTitle}}</p>
                </div>
                <div class="line"></div>
                    <div class="icon">
                        <div class="info-icon">
                            <i class="fas fa-signal"></i>
                            <p>Advanced</p>
                        </div>
                        <div class="info-icon">
                            <i class="fas fa-list-ul"></i>
                            <p>8 Lectures</p>
                        </div>
                        <div class="info-icon">
                            <i class="far fa-clock"></i>
                            <p>6 hours</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="btn">
                <a href="#">LOAD MORE</a>
            </div>
          </div>
      </section>
  </main>
</template>

<script>
export default {
    name: 'Main',
    data() {
		return {
			CardInfo: [
				{
					title: 'How to be a DJ? Make ElectronicMusic',
                    subTitle: 'Eletronic',
                    image:  require('@/assets/img/eletronic.jpeg')
				},
                {
					title: 'Nvidia and UE4 Technologies Practice',
                    subTitle: 'Nvidia',
                    image:  require('@/assets/img/unreal.png')
				},
                {
					title: 'Fashion Photography from professional',
                    subTitle: 'Fashion',
                    image:  require('@/assets/img/fashon.jpeg')
				},
                {
					title: 'Design Instruments for Communication',
                    subTitle: 'Desgin',
                    image:  require('@/assets/img/design.jpeg')
				},
                {
					title: 'Make your Concept Right and Beatiful',
                    subTitle: 'Art',
                    image:  require('@/assets/img/book.jpg')
				},
                {
					title: 'Road Bike Manual or How to be a Champion.',
                    subTitle: 'Bicycling',
                    image:  require('@/assets/img/bike.jpeg')
				},
			],
		};
	},
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
        .courses{
            background-color: $haze;
            padding: 60px 0;

            h3{
                color: $black;
                font-size: 50px;
                text-align: center;
                padding-bottom: 65px;
            }

            .card-courses{
                display: flex;
                flex-wrap: wrap;
                width: 65%;
                margin: 0 auto;



                .btn{
                    display: flex;
                    justify-content: center;
                    width: 100%;
                    padding-top: 35px;

                    a{
                        text-align: center;
                        background: $buttercup;
                        text-decoration: none;
                        padding: 10px 20px;
                        border-radius: 25px;
                        color: $white;
                        font-weight: 700;
                    }
                }

                .card{
                    margin: 10px 0;

                    .card-img{
                        width: 100%;

                        img{
                            width: 100%;
                        }
                    }
                    .card-content{
                        background: $white;
                        padding: 20px;

                        h4{
                            font-weight: 700;
                            text-align: center;
                            padding: 0 10px;
                        }

                        p{
                            text-align: center;
                            color: #aabdd6;
                            padding: 10px 0;
                        }
                    }

                    .line{
                        height: 1px;
                        background: $gray;
                        width: 100%;
                        margin: 20px 0;
                    }

                    .icon{
                        display: flex;
                        justify-content: space-between;
                        padding: 10px 0;

                        .info-icon{
                            display: flex;
                            align-items: center;

                            p{
                                text-align: center;
                                color: black;
                                padding: 10px 0;
                            }

                            i{
                                padding-right: 5px;
                                color: $fuel-yellow;
                            }
                        }
                    }
                }
            }
        }
    }
</style>