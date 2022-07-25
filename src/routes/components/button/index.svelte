<script lang="ts">
	export let text: string;
	export let onClick: (value: string) => void;
	export let color: 'orange' | 'grey' | 'dark-grey';
</script>

<div class="button" data-color={color} on:click={() => onClick(text)}>{text}</div>

<style lang="scss">
	.button {
		width: 80px;
		height: 80px;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 24px;
		font-weight: 600;
		&[data-color='orange'] {
			background-color: orange;
		}
		&[data-color='grey'] {
			background-color: grey;
		}
		&[data-color='dark-grey'] {
			background-color: darkgrey;
		}
	}
</style>