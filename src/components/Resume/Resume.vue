<template>
	<div class="resume-preview">
		<Person></Person>
		<Education></Education>
		<Skills></Skills>
		<Project></Project>
	</div>
</template>

<script>
import Person from './Person.vue'
import Education from './Education.vue'
import Skills from './Skills.vue'
import Project from './Project.vue'
export default {
	name: 'Resume',
	components: {
		Person,
		Education,
		Skills,
		Project
	}
}
</script>

<style scoped>
.resume-preview {
	width: 210mm;
	height: 297mm;
	background: #fff;
	padding: 50px;

}
</style>