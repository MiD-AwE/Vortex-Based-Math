Vortex-Based-Math
=================

Project for the study of Vortex Based Mathematics and it's accompanying 3d visualization utilizing free open source, GPL, and web technologies.

Don't know what Vortex Based Mathematics is? Check out: http://vortexmath.webs.com/ And here is a video presentation from the TEDx conference: http://www.theabhakingdom.com/The_Gateway.html

Strut live preview (Firefox, Chrome and Safari only): http://tantaman.github.com/Strut/web-dist/index.html

Preview

A github hosted preview is available at: http://tantaman.github.com/Strut/web-dist/index.html (Firefox, Chrome and Safari only)

The preview currently points to the development version of Strut.

Mailing List

strut-presentation-editor@googlegroups.com

Building

Note: You can get pre-built versions of Strut here: https://github.com/tantaman/Strut/downloads

You'll need CoffeeScript and Handlebars installed in order to build Strut, as well as some ruby gems.

Install CoffeeScript (sudo npm install -g coffee-script)
Install HandleBars (sudo npm install -g handlebars)
Install bundler (sudo gem install bundler)
Run bundle in the root Strut directory
To build everything in one shot, run: rake devbuild

To build and minify everything for a production deployment, run: rake productionbuild (the production build will put its results into web-dist instead of web)

You can produce a new devbuild whenever a resource in the Strut directory changes by running guard from the root Strut directory.

Running

Strut can run entirely from your local filesystem.
Just point your browser to file:///path/to/Strut/web/index.html to view Strut.

Contributing

Strut uses a Maven directory layout so code and resource will be found in src/main

In Strut there is an object for each major component. The Slides, SlidePreviews, TransitionEditor, SlideEditor, etc. all have their own objects so it's easy to track down and make changes to a component. Strut uses RequireJS to keep source files small and focused. BackboneJS is used for Strut's data model and serialization as well as for binding events in the view layers.

In addition to having organized code, the markup for Strut is also split up by component and placed in HandlebarsJS template files.

Here is the basic layout of the source:

Presentation Model: src/model/presentation
Editor UI Layer: src/ui/editor
Model -> ImpressJS Rendering: src/ui/impress_renderer
templates for UI components are contained in src/ui/COMPONENT_NAME/res/templates in order to package related markup and backing UI (not model) code into modules.

Acknowledgements

ImpressJS (of course) https://github.com/bartaz/impress.js/
BackboneJS http://documentcloud.github.com/backbone/
CoffeeScript http://coffeescript.org/
RequireJS http://requirejs.org/
JQuery http://jquery.com/
Rake http://rubyforge.org/projects/rake/
HandlebarsJS http://handlebarsjs.com/
DustJS http://akdubya.github.com/dustjs/
Class class http://ejohn.org/blog/simple-javascript-inheritance/
Impressionist https://github.com/hsivaramx/Impressionist