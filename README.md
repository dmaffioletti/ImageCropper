# Image Cropper

Image cropper gives you an API for cropping images inside WordPress

For cropping an post thumbnail image to 200x300 pixels:
    <?php
      the_post();
      img(200, 300);
    ?>