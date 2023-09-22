<script>
    import { onMount } from 'svelte';
  
    let mapContainer;
  
    onMount(() => {
      if (typeof window !== 'undefined') {
        // Мы на клиенте, можете импортировать Leaflet и инициализировать карту
        import('leaflet').then((L) => {
          const map = L.map(mapContainer).setView([51.505, -0.09], 13);
  
          L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            maxZoom: 19,
            attribution: 'Map data &copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors',
          }).addTo(map);
        });
      }
    });
  </script>

<main class="map__content">
    <div bind:this="{mapContainer}" id="mapContainer"></div>
</main>

<style>
    .map__content{
        width: 100%;
        height: 550px;
        border-radius: 40px;
        background: var(--Gradient-blue, linear-gradient(233deg, #9FCCFA -20.48%, #0974F1 97.38%));
        flex-shrink: 0;
    }
    #mapContainer {
        width: 200px;
        height: 400px;
    }
</style>