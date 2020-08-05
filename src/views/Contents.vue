<template>
	<div>
		<div class="selectors">
			<div 
				v-for=" lang in languageFirst"
				:key="lang"
				class="selector"
				>
				<LangSelector 
					:lang="lang"
					class="inline"
				/>
				
			</div>
		</div>
		<div class="selectors second">
			<div 
				v-for=" lang in languageSecond"
				:key="lang"
				class="selector"
				>
				<LangSelector 
					:lang="lang"
					class="inline"
				/>
			</div>
		</div>
		</div>
</template>

<script>
import LangSelector from '../components/LangSelector.vue';

export default {
	name: 'Contests',
	components: {
		LangSelector,
	},
	data() {
		return {
			languageFirst: [ 'HTML', 'css', 'python', 'js'],
			languageSecond: ['java' ,'C' ,'go' ,'R'],
		}
	}
}
</script>

<style lang="less">

.selectors {
	display: flex;

	.selector {
		margin: 0 auto;
	}

	.selector:hover {
		opacity: 0.7;
	}

	.inline {
		display: inline-block;
	}

}

.second {
	margin-top: 3%;
}

.not-leftmost {
	margin-left: 20px;
}
</style>