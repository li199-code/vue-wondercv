<template>
	<div class="resume">
		<Person></Person>
		<Education></Education>
		<Skills></Skills>
	</div>
</template>

<script>
import Person from './Person.vue'
import Education from './Education.vue'
import Skills from './Skills.vue'
export default {
  name: 'Resume',
  components: {
    Person,
    Education,
    Skills
}
}
</script>

<style scoped>
.resume{
	width: 210mm;
	height: 297mm;
	background: #fff;
	padding: 50px;

}
</style>