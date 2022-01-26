<script lang="ts">
	import { onMount } from 'svelte';
	import { Viewer } from 'cesium';
	import '../node_modules/cesium/Build/Cesium/Widgets/widgets.css'

	window.CESIUM_BASE_URL = './build';

    let viewer: Viewer;
	onMount(async () => {
		viewer = new Viewer('cesiumContainer');
	});

</script>

<div id="cesiumContainer">
</div>
