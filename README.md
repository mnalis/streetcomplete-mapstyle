**This repository is obsolete. StreetComplete changed its map renderer from tangram-es to MapLibre-native. Development continues in the [repository of the MapLibre map style definition](https://github.com/streetcomplete/maplibre-streetcomplete-style)**

# StreetComplete map style

This is the map style used in the the android application [StreetComplete](https://github.com/streetcomplete/StreetComplete), an easy OpenStreetMap editor.

There are three variations on the style available: light, dark and satellite-style.

<img src="https://raw.githubusercontent.com/streetcomplete/streetcomplete-mapstyle/gh-pages/images/light.png" height="200px"> <img src="https://raw.githubusercontent.com/streetcomplete/streetcomplete-mapstyle/gh-pages/images/dark.png" height="200px"> <img src="https://raw.githubusercontent.com/streetcomplete/streetcomplete-mapstyle/gh-pages/images/satellite.png" height="200px">

## Purpose of this map style

This map style's design goal is to serve as a background map, used solely for visual orientation and navigating as a pedestrian while using the StreetComplete app during an (on-foot) survey.
It is designed to not visually distract the user from the quests that are displayed on the map. Elements that are neither relevant for orientation nor for quests asked in the app itself, are not displayed at all.

## Compatibility

Every vector map tiles hoster has his own schema, so every map style is per se only compatible with the schema it was created for. The style was originally created for are for the [mapzen/nextzen](https://www.nextzen.org/) schema. However, it has been adapted to work (with some reservations) with other vector tile schemes as well. It is available for:

- [jawg.io](https://www.jawg.io/en/maps) on branch [`jawg`](https://github.com/streetcomplete/streetcomplete-mapstyle/tree/jawg) which is used in StreetComplete and is maintained
- [nextzen](https://www.nextzen.org/) on the [`nextzen`](https://github.com/streetcomplete/streetcomplete-mapstyle/tree/nextzen) branch - not maintained, was used by StreetComplete in past
- [openmaptiles](https://openmaptiles.org/schema/) on branch [`openmaptiles`](https://github.com/streetcomplete/streetcomplete-mapstyle/tree/openmaptiles) - was created to test various tile providers for StreetComplete and is not maintained
- [thunderforest outdoors](https://www.thunderforest.com/docs/thunderforest.outdoors-v2/) on branch [`thunderforest`](https://github.com/streetcomplete/streetcomplete-mapstyle/tree/thunderforest) - was created to test various tile providers for StreetComplete and is not maintained

While improving map style it is fine to edit just `jawg` branch. Fixes to other branches are also welcome, but code there is not guaranteed to work.

## Contributing

* Open the code in an editor
  * StreetComplete Map Style Editor (recommended; [Normal map](https://streetcomplete.github.io/streetcomplete-mapstyle/?provider=jawg&style=light), [Satellite map](https://streetcomplete.github.io/streetcomplete-mapstyle/?provider=jawg&style=satellite), [Dark map](https://streetcomplete.github.io/streetcomplete-mapstyle/?provider=jawg&style=dark))
    * Already includes a jawg.io API key
  * Tangram Play ([Normal map](https://tangram.city/play/?scene=https://raw.githubusercontent.com/streetcomplete/streetcomplete-mapstyle/jawg/streetcomplete-light-style.yaml),  [Satellite map](https://tangram.city/play/?scene=https://raw.githubusercontent.com/streetcomplete/streetcomplete-mapstyle/jawg/streetcomplete-satellite-style.yaml), [Dark map](https://tangram.city/play/?scene=https://raw.githubusercontent.com/streetcomplete/streetcomplete-mapstyle/jawg/streetcomplete-dark-style.yaml))
    * You have to add your jawg.io API key to the field `api_key` in the `global` section
* Change or add something to the style
* Download the file after you did your work
* Make a pull request to this repository

## Useful links

* [View map & edit map style](https://streetcomplete.github.io/streetcomplete-mapstyle/?provider=jawg)
* [Tangram documentation](https://mapzen.com/documentation/tangram/)
* [Tangram Play](https://tangram.city/play/)
* [Issue #183 of StreetComplete](https://github.com/streetcomplete/StreetComplete/issues/183) (The reason why this repository was created)
