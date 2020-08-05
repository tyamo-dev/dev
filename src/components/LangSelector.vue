<template>
	<div class="selector">
		<div class="selector-text">
			{{ lang || 'none' }}
		</div>
	</div>
</template>

<script>
export default {
	name: 'LangSelector',
	props: {
		lang: {
			type: String,
			default: null
		}
	}
}
</script>

<style lang="less" scoped>
@import '../variables.less';
.selector {
	margin-top: 20px;
	width: 70px;
	height: 70px;
	background: @dark-green;
	opacity: 1.3;
	color: white;
	border-radius: 50%;
	text-align: center;

	.selector-text {
		padding-top: 22px;
	}
}
</style>