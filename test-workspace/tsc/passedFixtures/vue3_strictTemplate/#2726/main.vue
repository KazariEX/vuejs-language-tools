<script lang="ts" setup>
import { ref } from 'vue';

const foo = ref('bar');

defineSlots<{
	default: (props: {
		foo: string;
		buz?: number;
	}) => any;
}>();
</script>

<template>
	<slot v-bind="{ foo: foo }" />
</template>
