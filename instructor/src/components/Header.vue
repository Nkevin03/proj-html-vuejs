<template>
<section>
        <header>
        <head>
            <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" integrity="sha512-Fo3rlrZj/k7ujTnHg4CGR2D7kSs0v4LLanw2qksYuRlEzO+tcaEPQogQ0KaoGN26/zrn20ImR1DfuLWnOo7aBA==" crossorigin="anonymous" referrerpolicy="no-referrer">
            <link rel="icon" href="<%= BASE_URL %>favicon.ico">
        </head>
        <div class="logo-navbar">
            <a href="#"><img src="@/assets/img/MasterStudy-1.svg" alt=""></a>
        </div>
        <div class="right-navbar">
            <ul>
                <li v-for="link in NavbarLink" :key="`${link.text}`">
					<a :href="`${link.url}`">
						{{link.name}}
					</a>
                     <div class="arrow"></div>
				</li>
            </ul>
            <div class="social-header">
                <i class="fab fa-linkedin"></i>
                <i class="fab fa-instagram"></i>
                <i class="fab fa-facebook"></i>
                <i class="fab fa-twitter"></i>
            </div>
        </div>
    </header>
    <Hero />
</section>
</template>

<script>
import Hero from '@/components/Hero.vue'
export default {
    name: 'Header',
    components: {
    Hero
    },
    data() {
		return {
			NavbarLink: [
				{
					name: 'Home',
                    span: false,
					url: '#',
				},
				{
					name: 'Course Formats',
                    span: false,
					url: '#',
				},
				{
					name: 'Add Course',
                    span: true,
					url: '#',
				},
				{
					name: 'Pages',
                    span: false,
					url: '#',
				},
				{
					name: 'Demons',
                    span: false,
					url: '#',
				}
			],
		};
	},

}
</script>

<style scoped lang="scss">
@import '@/styles/preset.scss';
    header{
        width: 70%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .logo-navbar{
            display: flex;
            align-items: center;
            
            img{
                cursor: pointer;
            }
        }
        .right-navbar{
            display: flex;
            align-items: center;
            line-height: 100px;

            ul{
                display: flex;
                list-style: none;

                li{
                    line-height: 165px;
                    position: relative;

                    &:hover{
                        border-bottom: 3px solid $kourmikova;
                        display: flex;
                        justify-content: center;

                        .arrow{
                            position: absolute;
                            bottom: 0;
                            width: 0; 
                            height: 0; 
                            border-left: 5px solid transparent;
                            border-right: 5px solid transparent;
                            border-bottom: 5px solid $kourmikova;
                        }
                    }

                    span{
                        position: absolute;
                        top: 45px;
                        right: 0;
                        background: $red;
                        line-height: 22px;
                        font-weight: 500;
                        width: 48px;
                        text-align: center;
                        border-top-left-radius: 10px;
                        border-top-right-radius: 10px;
                        border-bottom-right-radius: 10px;
                        border-bottom-left-radius: 3px;
                        color: $white;
                        font-size: 13px;
                    }
                }

                a{
                    text-decoration: none;
                    color: $shaft;
                    font-size: 20px;
                    padding: 0 10px;
                    font-weight: 700;
                }
            }
            .social-header{
                padding-left: 40px;
                i{
                    cursor: pointer;
                    padding-right: 10px;
                    font-size: 20px;
                    color: $shaft;
                }
            }
        }
    }
    
        
</style>