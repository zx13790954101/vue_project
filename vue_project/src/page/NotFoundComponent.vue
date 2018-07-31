<template>
	<div>
	    <h1>404页面</h1>
	</div>
</template>

<script>
	export default {
		name: 'NotFoundComponent',
	    data () {
		    return {
		      post: {                   
		      	author: {
	                loginname: 'temp',//设置默认值，防止Vue在axios未被调用前报错
	               }
		      },
	  	      loading:false
		    }
		},
		computed:{
		
		},
	  	methods: {
		 
		},
	    beforeMount() {
	    	this.loading = true;
	        this.getData();
	    },
	    watch:{
			$route(){
				this.getData();
			}
		}
	}
</script>

<style>
/*scoped属性导致css仅对当前组件生效，而html绑定渲染出的内容可以理解为是子组件的内容，子组件不会被加上对应的属性，所以不会应用css.
解决的话把scoped属性去掉就行了*/
	@import url("../assets/markdown-github.css");
	.ArticleSection {
		-webkit-box-sizing: border-box;
		-moz-box-sizing: border-box;
		box-sizing: border-box;
		display: inline-block;
		width: 70%;
		border: 1px solid #ddd;	
	    padding: 0.8rem 0.4rem;
	    margin-left: 3%;
	}
	.ArticleSection #content {
		padding: 2rem 1rem 2rem 1rem;
		line-height: 1.6;
		padding-bottom: 1rem;
	}
	.ArticleSection > h1 {
		font-size: 0.1rem;
	}
	.article {
		background: white;
   	    margin-bottom: 10px;
        padding-left: 20px;
        padding-top: 10px;

	}
	.article h1 {
		font-size:1.2rem;
		font-weight: 600;
	}
	.article >ul li {
		display: inline-block;
		font-size:0.8rem ;
		color:#a8a3a3 ;
		padding-left: 5px;
	}
	.article li a {
	    color: inherit;
   		 text-decoration: none;
	}
    .replySec {
        box-sizing: border-box;
        border-bottom: 1px solid #C0CCDA;
        width: 100%;
        padding: 1rem;
        background: white;
    }
    #reply {
        display: flex;
        flex-direction: column;
    }
    .replyUp {
    	display: inline-block;
    }
    .replyUp span {
    	display: inline-block;
	    vertical-align: top;
	    margin-top: 7px;
	    margin-left: 6px;
	    font-size: 14px;
	    color: #806767;
    }
    .thumbsClass {
    	float: right;
    }
    .replyUp > a{
    	color: black;
	   	text-decoration: none;
		font-weight: 600;
    }
    .replyUp a:nth-of-type(2) {
    	margin-left: -14px;
    	vertical-align: super;
    }
    .thumbsClass  {
    	color: red;
    }
    .replySec > p {
    	padding-left: 50px;
    	clear: both;
    }
    .replySec img {
    	width: 1.5rem;
    	height: 1.5rem;
    	margin-right: 1rem;
    }	
    .replySec p img {
    	overflow: hidden;
    	width: 100%;
    	height: 100%;
    }
</style>