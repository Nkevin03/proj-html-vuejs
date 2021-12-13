<template>
  <section class="container col-12 course">
      <div class="row">
          <div class="title-course">
            <h3>Why my Courses?</h3>
          </div>
            <div class="card-course col-6 d-flex" v-for="card in CardCourse" :key="`${card.text}`">
                <div class="border-card mx-3 my-3">
                    <div class="icon">
                        <i :class="card.class"></i>
                    </div>
                    <div class="text-card">
                        <h4>{{card.title}}</h4>
                        <p>{{card.description}}</p>
                    </div>
                </div>
            </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'Courses',
    data() {
		return {
			CardCourse: [
				{
                    class: 'fas fa-briefcase',
                    title: 'Entrepreneurship',
                    description: 'Vestibulum vitae aliquam nunc. Suspendisse mollis metus ac tellus egestas pharetra. Suspendisse at viverra purus. Pellentesque nec posuere ligula, eu congue leo. Integer vulputate tempor arcu. Vestibulum vulputate.'
				},
                {
                    class: 'fas fa-rocket',
                    title: 'Accelerated learning',
                    description: 'Vestibulum vitae aliquam nunc. Suspendisse mollis metus ac tellus egestas pharetra. Suspendisse at viverra purus. Pellentesque nec posuere ligula, eu congue leo. Integer vulputate tempor arcu. Vestibulum vulputate.'
				},
                {
                    class: 'far fa-thumbs-up',
                    title: 'Productivity',
                    description: 'Vestibulum vitae aliquam nunc. Suspendisse mollis metus ac tellus egestas pharetra. Suspendisse at viverra purus. Pellentesque nec posuere ligula, eu congue leo. Integer vulputate tempor arcu. Vestibulum vulputate.'
				},
                {
                    class: 'fas fa-cog',
                    title: 'Life Coaching',
                    description: 'Vestibulum vitae aliquam nunc. Suspendisse mollis metus ac tellus egestas pharetra. Suspendisse at viverra purus. Pellentesque nec posuere ligula, eu congue leo. Integer vulputate tempor arcu. Vestibulum vulputate.'
				},
			],
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/preset.scss';
    .course{
        margin: 0 auto;
        padding: 50px 0;
        
        .card-course{

            .border-card{
                display: flex;
                border-left: 4px solid $buttercup;
                box-shadow: 5px 5px 10px 0px #0000005b;

                &:hover{
                    background: $buttercup;
                    transition: 0.5s;

                    &:hover i{
                        color: $white;
                    }

                    &:hover p{
                        color: #000;
                    }
                }
            }

            .icon{

                i{
                    color: $buttercup;
                    font-size: 50px;
                    padding: 30px 20px;
                }
            }
        }

        .title-course{
            text-align: center;
            padding: 20px;

            h3{
                font-size: 50px;
                font-weight: 700;
            }
        }
        .text-card{
            padding: 30px 20px;
            
            h4{
                font-weight: 700;
            }

            p{
                color: $firefly;
                padding: 20px 0;
            }
        }
    }
</style>