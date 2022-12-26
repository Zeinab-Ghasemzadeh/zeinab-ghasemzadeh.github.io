<template>
	<div id="contact">
		<div class="alert alert-info">
			<div class="d-flex justify-content-center">
	      		<a class="px-3" v-for="section in sections" :href="section.link">
					<box-icon type='logo' :name="section.class_name" size='lg' @mouseenter="changeColor(section)" @mouseleave="changeColor(section)" :color="[section.is_active ? section.color : '']" />
		        </a>
	      	</div>
		</div>
	</div>
</template>

<script>
export default {
	data(){
		return{
			sections:{
				gamil:{
					is_active:false,
					color:'#BB001B',
					class_name:'gmail',
					link:'mailto:zeinabghasemzade@gmail.com'
				},
				linkedin:{
					is_active:false,
					color:'#2867b2',
					class_name:'linkedin',
					link:'https://www.linkedin.com/in/zeinab-ghasemzadeh-715aa8169/'
				}
			}
		}
	},
	methods:{
		changeColor(section){
			section.is_active=!section.is_active
		}
	}
}
</script>