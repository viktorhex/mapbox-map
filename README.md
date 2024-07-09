# @1nf053c/mapbox-map

### Getting Started

```sh
npm i @1nf053c/mapbox-map
```

```tsx
"use client";

import { MapboxMap } from "@1nf053c/mapbox-map";

export function MapboxMapContainer() {

    const config = {
        publicKey="YOUR_MAPBOX_PUBLIC_KEY",
        startLng=50,
        startLat=-51,
        zoomLevel=12
    }

    return <MapboxMap
        publicKey={config.publicKey}
        startLng={config.startLng}
        startLat={config.startLat}
        zoomLevel={config.zoomLevel} 
    />
}

// 1. import MapboxMap component
// 2. Create or fetch your MapboxMap config
// 3. Render MapboxMap component with config
```

### What's Next:

##### Feature extensions with hooks

```tsx
"use client";

import {
    MapboxMap,
    MapboxMapAthleticsAdvisorPlugin,
    MapboxMapRestaurantAdvisorPlugin,
    // ...etc
} from "@1nf053c/mapbox-map";

export function MapboxMapContainer() {

    const config = {
        publicKey="YOUR_MAPBOX_PUBLIC_KEY",
        startLng=50,
        startLat=-51,
        zoomLevel=12
    };

    const plugins = [MapboxMapAthleticsAdvisor, MapboxMapRestaurantAdvisor];
    
    return (
        <MapboxMap
            plugins={plugins}
            publicKey={config.publicKey}
            startLng={config.startLng}
            startLat={config.startLat}
            zoomLevel={config.zoomLevel} 
        />
    );
}
```
