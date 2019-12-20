<template>
	<component
		:is="tag"
		:href="to"
		class="border-b-2"
		:class="[display, {
            'text-blue-600 border-blue-200 hover:text-blue-700 hover:border-blue-400': color == 'blue',
            'text-blue-600 border-blue-200 hover:text-blue-700 hover:border-blue-400': color == 'blue'
        }]"
	>
		<slot></slot>
	</component>
</template>

<script>
export default {
	props: {
		color: {
			type: String,
			default: "blue"
		},
		tag: {
			type: String,
			default: "a"
		},
		to: {
			type: String
		},
		display: {
			type: String,
			default: "inline-flex"
		}
	}
};
</script>
