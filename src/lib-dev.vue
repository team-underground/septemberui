<script>
import { Alert, DateInput } from "@/entry";
export default {
	name: "SeptemberuiLibDev", // vue library dev component
	components: {
		Alert,
		DateInput
	},
	data() {
		return {
			date: "16/12/2019"
		};
	}
};
</script>

<template>
	<div class="septemberui-lib-dev">
		<alert>asdjjjk</alert>
		<date-input v-model="date" min-date="2019-12-15" max-date="2019-12-20"></date-input>
	</div>
</template>

<style scoped>
.septemberui-lib-dev {
	display: block;
	width: 400px;
	margin: 25px auto;
}
</style>
