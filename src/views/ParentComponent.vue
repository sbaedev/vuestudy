<template>
	<div>
		<button type="button" @click="checkChild">자식 컴포넌트 데이터 조회</button>
		<child-component ref="child_component" />
	</div>
</template>
<script>
import ChildComponent from './ChildComponent';
export default {
	components: { ChildComponent },
	computed: {
		msg() {
			return this.$refs.child_component.msg;
		},
	},
	methods: {
		checkChild() {
			alert(this.msg);
		},
	},
};
</script>
