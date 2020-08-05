<template>
	<div>
		<Header class="site-title"/>
		<div class="tabs">
			<span class="tab" :class="(activeTab === 'profile')? 'active' : '' " @click="clickTab('profile')">profile</span> 
			<span class="slash"> / </span>
			<span class="tab" :class="(activeTab === 'contents') ? 'active' : '' " @click="clickTab('contents')">contents</span>
		</div>

		<div class="content-wrapper">
			<Profile  v-if="activeTab === 'profile'"/>
			<Contents v-if="activeTab === 'contents'"/>
		</div>
	</div>
</template>

<script>
import Header from '../components/Header.vue';
import Profile from '@/views//Profile.vue';
import Contents from '@/views//Contents.vue';

export default {
	name: 'Homepage',
	components: {
		Header,
		Profile,
		Contents,
	},
	data() {
		return {
			activeTab: 'profile',
		}
	},
	methods: {
		clickTab(tabName) {
			this.activeTab = tabName;
		}
	}
}
</script>

<style lang="less">
@import  '../variables.less';
.site-title {
	margin-top: 5%;
	margin-bottom: 5%;
	text-align: center;
}

.content-wrapper {
	margin: 5% auto 0 auto;
	width: 50%;
	text-align: center;
}

.tabs {
	text-align: center;
	color: @black;
	cursor: default;

	.tab {
		cursor: default;

	}

	.tab:hover {
		color: @green;
	}

	.active {
		color: @dark-green;
	}

	.slash {
		margin: 0 7px 0 7px;
	}
}
</style>
