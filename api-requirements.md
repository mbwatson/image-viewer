# NC DOT Roadway Safety


## Client Features


### For Each Image


#### Single image (one for at each time stamp...)

- show _three_ forward-facing images
- show image metadata
- show current annotations (see below)
- show annotation history -- who, what, when
- show map view of image location

#### Annotations

- binary feature tagging, e.g., guardrail, sign, tree
- users can create new annotation type -- name, description, comment
- users can modify existing annotation -- name, description, comment


```
- GET all annotations
- POST new annotation
- PATCH existing annotation
- GET annotations for image
- PATCH annotation value for image
```


### Image Navigation


#### Gallery view

- show many images simultaneously

```
GET (all?) images (pagination, start index, offset)
```

#### Time-based

- navigate along runs -- prev, next buttons

```
- GET image from id/timestamp
```

#### Space-based

- render map with image locations
- user clicks on map to view image closest to click target

```
- GET images from location
    + rectangle drawn on map ?
    + zipcode ?
    + [lon lat] ⟼ [ lon ± 𝛿, lat ± 𝛿 ] ?
```

#### Annotation-based (Smart fast-forward)

- browse to (next) image with given annotation

```
GET images with given annotation
```

#### Random image

- perhaps
    + from defined geographic region
    + perhaps from certain image subset

```
GET random image
```


### Statistics View

