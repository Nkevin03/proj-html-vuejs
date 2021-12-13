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
                <div class="border-cards mx-4">
                    <div class="card-img">
                        <div class="hover-price">
                            <p>$59</p>
                        </div>
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
            </div>
            <div class="btn">
                <a href="#">LOAD MORE</a>
            </div>
          </div>
      </section>

      <!-- Order book -->
      <section class="order-book">
          <div class="book">
              <div class="icon-book">
                  <i class="fas fa-tv"></i>
                  <i class="far fa-circle"></i>
                  <i class="fas fa-wrench"></i>
                  <i class="fas fa-shopping-cart"></i>
                  <i class="fas fa-mobile-alt"></i>
              </div>
              <div class="left-book">
                  <h4>Get My exclusive Investing Book just fot $19.50</h4>
                  <p>Vestibulum imentum eu urna vel cursus. Aenean vehicula quam quam, vitae pellentesque urna elementum cursus.</p>
                  <div class="image-book">
                      <img src="@/assets/img/amazon.png" alt="">
                  </div>
              </div>
              <div class="right-book">
                  <img src="@/assets/img/book.png" alt="">
              </div>
          </div>
      </section>
      <Courses />
      <!-- Banner -->
      <section class="banner row">
          <div class="container col-12 mx-auto d-flex">
              <div class="info-banner col-3">
                  <div class="d-flex align-items-center">
                      <i class="fas fa-user-friends"></i>
                  </div>
                  <div class="info-icon">
                      <h4>3915</h4>
                      <p>Online Learner</p>
                  </div>
              </div>
              <div class="info-banner col-3">
                  <div class="d-flex align-items-center">
                     <i class="fas fa-film"></i>
                  </div>
                  <div class="info-icon">
                      <h4>23</h4>
                      <p>Video Courses</p>
                  </div>
              </div>
              <div class="info-banner col-3">
                  <div class="d-flex align-items-center">
                      <i class="far fa-file-image"></i>
                  </div>
                  <div class="info-icon">
                      <h4>437</h4>
                      <p>Sliders & Images</p>
                  </div>
              </div>
              <div class="info-banner col-3">
                  <div class="d-flex align-items-center">
                      <i class="far fa-thumbs-up"></i>
                  </div>
                  <div class="info-icon">
                      <h4>1440</h4>
                      <p>Excellent Reviews</p>
                  </div>
              </div>
          </div>
      </section>
      <Slider />
  </main>
</template>

<script>
import Courses from '@/components/Courses.vue'
import Slider from '@/components/Slider.vue'
export default {
    name: 'Main',
      components: {
        Courses,
        Slider
    },
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

                        &:hover{
                            background: $fuel-yellow;
                        }
                    }
                }

                .card{
                    margin-bottom: 30px;
                    border: none;
                    background-color: $haze;
                    display: flex;
                    align-items: center;

                    .border-cards{
                        border: 1px solid $silver;
                        width: 335px;

                        .card-img{
                            position: relative;
                            width: 100%;
                            cursor: pointer;

                            .hover-price{
                                position: absolute;
                                background: rgba(0, 0, 0, 0.452);
                                height: 100%;
                                width: 100%;
                                display: none;
                                color: $white;

                                p{
                                    position: absolute;
                                    top: 45%;
                                    left: 45%;
                                    font-size: 30px;
                                }

                            }

                        &:hover .hover-price{
                            display: block;
                        }

                        img{
                            width: 100%;
                        }
                    }
                    }
                    .card-content{
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
                        justify-content: space-around;
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
        .order-book{
            background-image: url(../assets/img/slider-book.jpg);
            background-repeat: no-repeat;
            background-position: center;
            position: relative;
            background-size: cover;

            .book{
                display: flex;
                align-items: center;
                width: 65%;
                margin: 0 auto;

                .icon-book{
                    position: absolute;
                    top: 30px;
                    right: 0;
                    background: $white;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    align-items: center;
                    width: 50px;

                    i{
                        font-size: 25px;
                        padding: 15px 0;
                    }
                }

                .left-book{
                    width: 50%;
                
                    h4{
                        font-size: 40px;
                        font-weight: 700;
                        padding: 30px 0;
                        color: $buttercup;
                        text-align: center;
                    }
                    
                    p{
                        font-size: 25px;
                        padding: 10px 0;
                        text-align: center;
                        color: $white;
                        font-weight: 500;
                        font-style: italic;
                    }
                    .image-book{
                        width: 100%;
                        display: flex;
                        justify-content: center;
                        padding: 10px 0;
                    }
                }
                .right-book{
                    padding-top: 40px;
                    width: 50%;
                }
            }
        }
        .banner{
            background-image: url(../assets/img/banner2.jpg);
            background-size: cover;
            background-position: top;
            background-repeat: no-repeat;

            .info-banner{
                display: flex;
                justify-content: center;
                padding: 150px 0;

                i{
                    font-size: 45px;
                    color: $white;
                    padding-right: 20px;
                }

                .info-icon{

                    h4{
                        color: $buttercup;
                        font-size: 30px;
                        font-weight: 700;
                    }

                    p{
                        color: $white;
                    }
                }
            }
        }
    }
</style>