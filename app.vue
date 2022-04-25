<template>
	<div>
		<button @click="dynamic">Open dynamic Modal</button>
		<ModalsContainer></ModalsContainer>
	</div>
</template>

<script>
	import { ModalsContainer, $vfm } from 'vue-final-modal';

	export default {
		components: {
			ModalsContainer,
		},
		methods: {
			dynamic() {
				$vfm.show({
					component: 'CustomModal',
					bind: {
						name: 'Test'
					},
					on: {
						confirm(close) {
							console.log('confirm')
							close()
						},
						cancel(close) {
							console.log('cancel')
							close()
						},
					},
				})
			}
		}
	}
</script>