<template>
    <a href="#" v-bind:class="{toTop: 'toTop', isHide: isHide}" style="margin-right: -55px; right: 50%; display: inline;">
        <span id="toTopHover" style="opacity: 0;"></span>
    </a>
</template>

<script>
    export default {
        data() {
            return {
                toTop: false,
                isHide: true
            }
        },
        mounted() {
	    window.addEventListener('scroll', this.handleScroll)
        },

        methods: {
            handleScroll () {
                var offsetTop = document.querySelector('#page1').offsetTop + 500
                var scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop
                if (scrollTop > offsetTop) this.isHide = false
                else this.isHide = true
            }
        },

        destroyed () {
            window.removeEventListener('scroll', this.handleScroll); // 离开页面 关闭监听 不然会报错
        }
    }
</script>

<style>
	.toTop {
		display:none;
		text-decoration:none;
		position:fixed;
		bottom:40px;
		margin-right: -620px !important;
		overflow:hidden;
		width:45px;
		height:45px;
		border:none;
		text-indent:-999px;
		z-index:999;
		background:url(/static/images/totop.png) no-repeat left top;
		transition: 0s ease;
		-webkit-transition: 0s ease;
		-o-transition: 0s ease;	
	}
	.toTop:hover {
		background-position: right 0;
    }
    
    .isHide {
        visibility: hidden;
    }
</style>
