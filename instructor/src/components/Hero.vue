<template>
    <section class="hero">
        <div class="hero-content">
           <div class="hero-text">
                <h1>Start your human <span>Revolution</span> today</h1>
                <p>A wonderful serenity has taken possession of my entire soul, like these sweet mornings of spring which I enjoy with my whole heart.</p>
           </div>
        </div>
        <div class="sales">
            <div class="box-sales">
                <div class="box-left">
                    <h3><span>Limited Sale: </span>All courses with 55% off</h3>
                    <div>
                        <input type="text" placeholder="Enter your E-mail">
                        <a href="#">SUBSCRIBE</a>
                    </div>
                </div>
                <div class="box-right">
                    <div class="item">
                        <h3>26</h3>
                        <p>Days</p>
                    </div>
                    <div class="item">
                        <h3>01</h3>
                        <p>Hours</p>
                    </div>
                    <div class="item">
                        <h3>47</h3>
                        <p>Minutes</p>
                    </div>
                    <div class="item">
                        <h3>34</h3>
                        <p>Seconds</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Hero',
}
</script>

<style scoped lang="scss">
@import '@/styles/preset.scss';
    .hero{
        background-image: url(../assets/img/slide-1.jpg);
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        height: 90vh;

        .hero-content{
            display: flex;
            justify-content: end;
            align-items: center;
            height: 100%;
            width: 60%;
            margin: 0 auto;
            
            .hero-text{
                display: flex;
                flex-direction: column;
                width: 60%;
                transform: translateY(-100px);

                h1{
                    width: 70%;
                    font-size: 60px;

                    span{
                        color: $fuel-yellow;
                    }
                }

                p{
                    margin-top: 30px;
                    font-weight: 300;
                    line-height: 30px;
                    font-size: 20px;
                }
            }
        }
        .sales{
            display: flex;
            justify-content: center;

            .box-sales{
                display: flex;
                height: 250px;
                width: 1300px;
                transform: translateY(-120px);
                border-radius: 15px;
                background-color: $buttercup;

                .box-left{
                    width: 50%;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    flex-direction: column;

                    div{
                        display: flex;
                        align-items: center;
                        position: relative;
                        width: 85%;
                        padding: 30px 0;

                        input{
                            width: 100%;
                            height: 50px;
                            border: none;
                            outline: none;
                            padding: 0 30px;
                            border-radius: 25px;
                        }

                        a{
                            position: absolute;
                            background-color: $firefly;
                            color: #fff;
                            text-decoration: none;
                            height: 50px;
                            text-align: center;
                            display: flex;
                            align-items: center;
                            border-radius: 25px;
                            padding: 0 20px;
                            right: 0;
                        }
                    }

                    h3{
                        font-size: 30px;
                        color: $shaft;

                        span{
                            color: #fff;
                        }
                    }
                }
                .box-right{
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    width: 50%;

                    .item{
                        padding: 30px;

                        h3{
                            color: #fff;
                            font-size: 70px;
                        }
                        p{
                            font-size: 20px;
                            color: $black;
                            text-align: center;
                            font-weight: 700;
                        }
                    }
                }
            }
        }
    }
</style>