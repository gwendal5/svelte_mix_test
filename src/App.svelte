<script>
	import { BarChartSimple } from "@carbon/charts-svelte";
	import "@carbon/charts/styles.min.css";
	import "carbon-components/css/carbon-components.min.css";
</script>

<BarChartSimple
	data={[
		{ group: "Qty", value: 65000 },
		{ group: "More", value: 29123 },
		{ group: "Sold", value: 35213 },
		{ group: "Restocking", value: 51213 },
		{ group: "Misc", value: 16932 },
	]}
	options={{
		title: "Simple bar (discrete)",
		height: "400px",
		axes: {
			left: { mapsTo: "value" },
			bottom: { mapsTo: "group", scaleType: "labels" },
		},
	}}
/>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
