<script lang="ts">
	export let value: boolean = true;
	export let default_value: boolean;
	export let style: string = "";
	export let variant: "default" | "panel" = "default";

	if (default_value) value = default_value;
</script>

<div
	{style}
	class:hidden={!value}
	class:bg-gray-50={variant === "panel"}
	class:p-2={variant === "panel"}
	class:rounded-lg={variant === "panel"}
	class="flex flex-1 flex-col gr-gap gr-form-gap relative"
>
	<slot />
</div>
