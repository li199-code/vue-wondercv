<template>
	<div class='resume-edit'>
		<PersonEdit></PersonEdit>
		<EducationEdit></EducationEdit>

	</div>
</template>

<script>
import EducationEdit from './EducationEdit.vue';
import PersonEdit from './PersonEdit.vue';

export default {
	name: 'Resume-edit',
	components: {
		EducationEdit,
		PersonEdit
	}
}
</script>

<style scoped>
.resume-edit {
	width: 210mm;
	height: 297mm;
	background: #fff;
	padding: 50px;
	margin-right: 10px;
}
</style>