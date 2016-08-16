# Evenly

## Update evenly.io

1. Update a file on master (can be done on Gitlab or clone locally)
2. Go to [Pipelines](/internal/evenly-io/pipelines)
3. See your change and click on the "Run" triangle icon
4. Watch your changes appear on evenly.io 
5. Check that all went well


## Building the website locally
### Prerequisites
You need to install the static site generator [jekyll](http://jekyllrb.com).

To install run `gem install jekyll` in the terminal. If that fails run `gem update` and try again.

### Running the website locally
Go to the folder in Terminal where you cloned the repository (see above).

`jekyll build` creates the site from the template files.

`jekyll serve` allows you to try the page locally in your browser at [http://127.0.0.1:4000](http://127.0.0.1:4000)

## Image Specs
The path for images used on the site is `/images` and project images live in another level, named after the project, in lowercase (example `/images/3daround`).

Images are different for some breakpoints; details below.

### Home

#### Carousel

Carousel images are fused with device images for launch. That will be changed later. For now, these are the dimensions in which images should be exported. Ox will take care of producing the usable assets.

File name				|	Dimension (iPad)	|	Dimension (iPhone)
---|---|---
[img].png 				|	640 x 478px			|	182 x 317px
[img]-medium-2x.png		|	1030 x 774px		|	294 x 522px
[img]-medium.png		|	515 x 387px			|	147 x 261px
[img]-small-2x.png		|	476 x 356px			|	154 x 266px
[img]-small.png			|	238 x 178px			|	77 x 133px




### Team

#### Team Member Picture

For launch, this needs to be rendered with a circle shaped mask, as a transparent PNG. Later we should fix that to use HTML.

File name				|	Dimension
----------------|----------------
[img].png				|	190 x 190px
[img]-medium-2x.png		|	380 x 380px
[img]-medium.png		|	190 x 190px
[img]-small-2x.png		|	380 x 380px
[img]-small.png			|	190 x 190px




### Projects

#### App Icon

For launch, this needs to be rendered with a rounded square shaped mask and drop shadow, as a transparent PNG. Later we should fix that to use HTML.

File name				|	Dimension
----------------|---------------
[img].png				|	66 x 66px

#### Color Mode

You can add color modes for the navigation bar and the App Icon drop shadow.
You can add the following variables on the markdowns:
* `color-mode` - [dark-mode/light-mode] color mode for text on the navigation bar.
* `icon-color-mode` - [dark-mode/light-mode] color mode for text on the navigation bar. *(optional)*

#### Project Screenshot (Description)

File name				|	Dimension (Portrait)
---|---|---
[img].png				|	300 x 530px
[img]-medium-2x.png		|	600 x 1060px
[img]-medium.png		|	300 x 530px
[img]-small-2x.png		|	540 x 960px
[img]-small.png			|	270 x 480px


#### Project Screenshot (Listings)

For launch, some of the sizes (medium, default) have a device outline which needs to be rendered manually with the device background.

File name				|	Dimension (Portrait)
----------------|---------------
[img].png				|	340 x 530px
[img]-medium-2x.png		|	548 x 970px
[img]-medium.png		|	274 x 485px
[img]-small-2x.png		|	540 x 960px
[img]-small.png			|	270 x 480px

##### Available Devices for Screenshots
You can select appropriate devices and its orientation for the screenshots.
Use the following variables below and place it on the project markdowns:
* `device` - The device that will be used on the screenshot. *(Refer to the Variable column on the table below)*
* `orientation` - The orientation of the device.

Device  | Variable | Orientation          |
--------|----------|----------------------|
iPhone  | iphone5  | Landscape / Portrait |
iPad    | ipad     | Landscape / Portrait |
