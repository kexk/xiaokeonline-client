<template>
  <header :class="currentPage">
			<div class="zerogrid">
				<div class="col-full">
					<div class="wrap-col">
						<div class="menu_block">
							<nav class="">
								<ul class="sf-menu">
									<li class="current men"><a @click="setCurrentPage('page1')" href="#">首页 </a> <strong class="hover"></strong></li>
									<li class="men1"><a @click="setCurrentPage('page2')" href="#page2">关于我们</a><strong class="hover"></strong></li>
									<li class=" men2"><a @click="setCurrentPage('page3')" href="#page3">服务</a> <strong class="hover"></strong></li>
									<li class=" men3"><a @click="setCurrentPage('page4')" href="#page4">客户</a> <strong class="hover"></strong></li>
									<li class=" men4"><a @click="setCurrentPage('page5')" href="#page5">联系我们</a> <strong class="hover"></strong></li>
								</ul>
							</nav>
							<div class="clear"></div>
						</div>
						<h1><a href="#" onClick="goToByScroll('page1'); return false;"><img src="images/logo.png" alt="Gerald Harris attorney at law"></a></h1>
					</div>
				</div>
				<div class="clear"></div>
			</div>
		</header>
</template>


<script>
  export default {
    data() {
      return {
				currentPage: "page1",
				plist: []
      }
		},
		mounted() {
			window.addEventListener('scroll', this.handleScroll)
			var page1 = document.querySelector('#page1').offsetTop

			var page2 = document.querySelector('#page2').offsetTop
			var page3 = document.querySelector('#page3').offsetTop
			var page4 = document.querySelector('#page4').offsetTop
			var page5 = document.querySelector('#page5').offsetTop
			this.plist.push(page1)

			this.plist.push(page2)
			this.plist.push(page3)
			this.plist.push(page4)
			this.plist.push(page5)
			
		},
		
		created() {
			
		},

        
    	destroyed () {
        window.removeEventListener('scroll', this.handleScroll); // 离开页面 关闭监听 不然会报错
      },
    	methods: {
      	setCurrentPage(pageName) {
				this.currentPage = pageName
				
				
			},
			handleScroll () {
				var scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop
				var offsetTop = document.querySelector('.toTop').offsetTop
				// this.plist.map((item, index) => {
				// 	if (scrollTop < item) {
				// 		console.log(item, index, '..')
				// 	}
				// })
				console.log(this.plist, '....')

				if (scrollTop > this.plist[0] && scrollTop < this.plist[1]) this.currentPage = "page1"
				else if (scrollTop > this.plist[1] && scrollTop <= this.plist[2]) this.currentPage = "page2"
				else if (scrollTop > this.plist[2] && scrollTop <= this.plist[3]) this.currentPage = "page3"
				else if (scrollTop > this.plist[3] && scrollTop <= this.plist[4]) this.currentPage = "page4"
				else if (scrollTop > this.plist[4] ) this.currentPage = "page5"

			}
    }
  }
</script>

<style>
  /* @import '/static/css/zerogrid.css'; */
</style>
