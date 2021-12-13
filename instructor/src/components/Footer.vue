<template>
  <footer>
    <div class="container mx-auto">
      <div class="foot row">
        <div class="about col-3" v-for="link in footerLink" :key="`${link.text}`">
          <h4>{{link.name}}</h4>
          <p>{{link.text}}</p>
          <div :class="link.iconnone">
            <i :class="link.icon1"></i>
            <i :class="link.icon2"></i>
            <i :class="link.icon3"></i>
          </div>
           <li :class="link.class">{{link.pages}}</li>
           <div class="image-footer">
             <div class="images-one">
               <img :src="link.imageone">
               <div>
                 <p>{{link.textone}}</p>
                <span>{{link.spanone}}</span>
               </div>
             </div>
             <div class="images-two">
               <img :src="link.imagetwo">
               <div>
                 <p>{{link.texttwo}}</p>
                 <span>{{link.spantwo}}</span>
               </div>
             </div>
           </div>
        </div>
    </div>
    </div>
  </footer>
</template>

<script>
export default {
    name: 'Footer',
    data() {
		return {
			footerLink: [
				{
					name: 'ABOUT',
          text: 'Masterstudy is Education WordPress theme featured by Learning Management System (LMS) for online education.',
          class: 'd-none',
          icon1: 'fab fa-facebook',
          icon2: 'fab fa-twitter',
          icon3: 'fab fa-instagram',
					url: '#',
				},
				{
					name: 'CONTACT',
          text: 'USA, California 20, First Avenue, California Tel.: +212 458 300 32 Fax: +1 212 375 24 14 Info@masterstudy.com',
          class: 'd-none',
          iconnone: 'd-none',
				},
        {
					name: 'PAGES',
          pages: 'Blog, Home, Shortcodes, Courses, Membership A, Titypography',
          iconnone: 'd-none',
				},
        {
          name: 'BLOG',
          class: 'd-none',
					imageone: require('@/assets/img/imagefooterone.jpeg'),
          textone: 'Our main target is to "Developing Yourself as a Leader"',
          spanone: '-August 9, 2018', 
					imagetwo: require('@/assets/img/photo-1490376840453-5f616fbebe5b-69x69.jpeg'),
          texttwo: 'Those Other Collage Expenses You Aren`t Thinking About',
          spantwo: '-June 3 9, 2015', 
          iconnone: 'd-none',
				}
			],
		};
	},
}
</script>

<style scoped lang='scss'>
@import '@/styles/preset.scss';
  footer{
    background-color: $fuel-yellow;
    padding: 40px 0;

    .about{

      h4{
        font-size: 25px;
        font-weight: 700;
        padding: 20px 0;
      }

      p{
        color: $abbey;
        width: 180px;
      }
      li{
        color: $abbey;
      }

      i{
        padding-top: 15px;
        padding-right: 10px;
        font-size: 18px;
      }

      .image-footer{

        .images-one{
          display: flex;
          margin-bottom: 20px;
          p{
            width: 280px;
            padding-left: 10px;
          }

          span{
            color: $cod;
            padding-left: 10px;
          }
        }
        .images-two{
          display: flex;
          margin-bottom: 20px;
          p{
            width: 280px;
            padding-left: 10px;
          }

          span{
            color: $cod;
            padding-left: 10px;
          }
        }
      }
    }
  }
</style>