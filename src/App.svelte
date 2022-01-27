<script lang="ts">
	import { onMount } from 'svelte';
	import { Viewer, createWorldTerrain } from 'cesium';
	import '../node_modules/cesium/Build/Cesium/Widgets/widgets.css'

	window.CESIUM_BASE_URL = './build';

    let viewer: Viewer;
	onMount(async () => {
		viewer = new Viewer('cesiumContainer', {
            orderIndependentTranslucency: false,
            timeline: false,
            geocoder: false,
            selectionIndicator: false,
            infoBox: false,
            scene3DOnly: true,
            shouldAnimate: true,
			terrainProvider: createWorldTerrain({
                requestVertexNormals: true,
                requestWaterMask: true
            })
		});
	});

</script>

<div id="cesiumContainer">
</div>
