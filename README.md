# Image Cropper

Image cropper gives you an API for cropping images inside WordPress

For cropping a post thumbnail image to 200x300 pixels:

	<?php
		the_post();
		img(200, 300);
	?>

This will verify the existence of post thumbnail, crop the image, save it in uploads folder, and generate an image tag.

To verify the existence of a post thumbnail, you can use <code>has_img()</code>

	<?php if (has_img()): ?>
	<figure>
		<?php img(200, 300) ?>
		<figcaption>Some text</figcaption>
	</figure>
	<?php endif ?>
	
	
To crop images that are not post thumbnails, you can use <code>crop($url, $size)</code>
	
	<?php
		$cropped_url= crop( get_bloginfo('url') . '/wp-content/uploads/image.jpg', array(200, 300) );
	?>
	<img src="<?php echo $cropped_url ?>">
	
	
### Changelog
0.3.0
First public version