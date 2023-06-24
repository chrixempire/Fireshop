<template>
	<div>
		<div class="container">
			<largeCardDisplay v-for="cardInfo in largeCardSections.slice(0, 1)" :key="cardInfo.id"
				:cardSection="cardInfo" />
			<smallCardDisplay v-for="cardInfo in smallCardSections" :key="cardInfo.id" :cardSection="cardInfo" />
		</div>
	</div>
</template>

<script>
import { largeCardSections, smallCardSections } from '~/assets/data.js';
export default {
	data() {
		return {
			largeCardSections,
			smallCardSections
		}
	}
}
</script>

<style  scoped></style>