<template>
	<nav class="navbar center navbar-expand-lg navbar-dark bg-dark rounded">
	  <div class="collapse navbar-collapse d-flex justify-content-center" id="navbarSupportedContent">
	    <ul class="navbar-nav mr-auto">
	      <li class="nav-item" v-for="section in sections">
	        <a class="nav-link" :href="section.id">
	        	{{ section.text }}
	        </a>
	      </li>
	    </ul>
	  </div>
	</nav>
</template>

<script>
export default {
	data(){
		return{
			sections:[
				{
					'text':'Curriculum Vitae',
					'id':'#academic-cv'
				},
				{
					'text':'Contact',
					'id':'#contact'
				}
			]
		}
	}
}
</script>