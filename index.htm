<!doctype html>
<html>
<head>
	<meta charset="utf-8" />

	<title>
		Showing Plupload Image Previews Using Base64-Encoded Data Urls
	</title>

	<link rel="stylesheet" type="text/css" href="./assets/css/styles.css"></link>
</head>
<body>

	<h1>
		Showing Plupload Image Previews Using Base64-Encoded Data Urls
	</h1>

	<div id="uploader" class="uploader">

		<a id="selectFiles" href="#">Select Files</a>

	</div>

	<ul class="uploads">
		<!-- Will be populated dynamically with LI/IMG tags. -->
	</ul>


	<!-- Load and initialize scripts. -->
	<script type="text/javascript" src="./assets/jquery/jquery-2.0.3.min.js"></script>
	<script type="text/javascript" src="./assets/plupload/js/plupload.full.min.js"></script>
	<script type="text/javascript">

		(function( $, plupload ) {


			// Find and cache the DOM elements we'll be using.
			var dom = {
				uploader: $( "#uploader" ),
				uploads: $( "ul.uploads" )
			};


			// Instantiate the Plupload uploader.
			var uploader = new plupload.Uploader({

				// Try to load the HTML5 engine and then, if that's
				// not supported, the Flash fallback engine.
				runtimes: "html5,flash",

				// The upload URL - for our demo, we'll just use a 
				// fake end-point (we're not actually uploading).
				url: "./post.json",

				// The ID of the drop-zone element.
				drop_element: "uploader",

				// To enable click-to-select-files, you can provide
				// a browse button. We can use the same one as the 
				// drop zone.
				browse_button: "selectFiles",

				// For the Flash engine, we have to define the ID 
				// of the node into which Pluploader will inject the 
				// <OBJECT> tag for the flash movie.
				container: "uploader",

				// The URL for the SWF file for the Flash upload 
				// engine for browsers that don't support HTML5.
				flash_swf_url: "./assets/plupload/js/Moxie.swf",

				// Needed for the Flash environment to work.
				urlstream_upload: true

			});


			// Set up the event handlers for the uploader.
			// --
			// NOTE: I have excluded a good number of events that are
			// not relevant to the current demo.
			uploader.bind( "PostInit", handlePluploadInit );
			uploader.bind( "FilesAdded", handlePluploadFilesAdded );
			
			// Initialize the uploader (it is only after the 
			// initialization is complete that we will know which
			// runtime load: html5 vs. Flash).
			uploader.init();


			// ------------------------------------------ //
			// ------------------------------------------ //


			// I handle the init event. At this point, we will know
			// which runtime has loaded, and whether or not drag-
			// drop functionality is supported.
			// --
			// NOTE: For this build of Plupload, I had to switch from
			// using the "Init" event to the "PostInit" in order for
			// the "dragdrop" feature to be correct defined.
			function handlePluploadInit( uploader, params ) {

				console.log( "Initialization complete." );

				console.log( "Drag-drop supported:", !! uploader.features.dragdrop );

			}


			// I handle the files-added event. This is different
			// that the queue-changed event. At this point, we 
			// have an opportunity to reject files from the queue.
			function handlePluploadFilesAdded( uploader, files ) {

				console.log( "Files selected." );

				// Show the client-side preview using the loaded File.
				for ( var i = 0 ; i < files.length ; i++ ) {

					showImagePreview( files[ i ] );

				}

			}


			// I take the given File object (as presented by 
			// Plupoload), and show the client-side-only preview of 
			// the selected image object.
			function showImagePreview( file ) {

				var item = $( "<li></li>" ).prependTo( dom.uploads );
				var image = $( new Image() ).appendTo( item );

				// Create an instance of the mOxie Image object. This
				// utility object provides several means of reading in
				// and loading image data from various sources.
				// --
				// Wiki: https://github.com/moxiecode/moxie/wiki/Image
				var preloader = new mOxie.Image();

				// Define the onload BEFORE you execute the load() 
				// command as load() does not execute async.
				preloader.onload = function() {

					// This will scale the image (in memory) before it
					// tries to render it. This just reduces the amount
					// of Base64 data that needs to be rendered.
					preloader.downsize( 300, 300 );

					// Now that the image is preloaded, grab the Base64
					// encoded data URL. This will show the image 
					// without making an Network request using the 
					// client-side file binary.
					image.prop( "src", preloader.getAsDataURL() );

					// NOTE: These previews "work" in the FLASH runtime.
					// But, they look seriously junky-to-the-monkey. 
					// Looks like they are only using like 256 colors.

				};

				// Calling the .getSource() on the file will return an
				// instance of mOxie.File, which is a unified file 
				// wrapper that can be used across the various runtimes.
				// --
				// Wiki: https://github.com/moxiecode/plupload/wiki/File
				preloader.load( file.getSource() );

			}


		})( jQuery, plupload );

	</script>

</body>
</html>