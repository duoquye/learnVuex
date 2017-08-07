<template>
	<div class="">
		<v-head></v-head>
		<ul>
			<li v-for="lis in ul">{{lis.li}}</li>
		</ul>
		<p>
			Copyright © {{author}} - 2016 All rights reserved
		</p>

	</div>
</template>

<script>
	import vHead from './Header.vue'
	export default {
		component: {
			vHead
		},
		data() {
			return {
				ul: [{
						li: '琉璃之金'
					},
					{
						li: '朦胧之森'
					},
					{
						li: '缥缈之滔'
					},
					{
						li: '逍遥之火'
					},
					{
						li: '璀璨之沙'
					}
				]
			}
		},
		computed: {
			author() {
				return this.$store.state.author
			}
		}

	}
</script>