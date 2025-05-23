---
layout: page
title: Branding
subtitle: Our Team Identity
show_sidebar: false
hero_image: ../images/Assets/Branding/BrandingHeader.png
hero_darken: true 
hero_height: is-large
--- 
<div class="full" style="text-align: center">
<p>Branding is a vital and crucial part of Team 17218. Below you can find our standards in branding.</p>


<h2><center>Logo</center></h2>
<p>Our team offers three usable logos. </p>
<p>We offer a scalable svg file, used when possible.</p>

<a href="../images/Assets/Branding/BrooklineBots.svg" download>
    <img width="300px" src="../images/Assets/Branding/BrooklineBots.svg">
</a>

<p>In addition we provide a high resolution logo. Used whenever svg is not a viable option and it is expected to be enlarged or seen at a large scale.</p> 

<a href ="../images/Assets/Branding/HighRes.png" download>
<img width="300px" src="../images/Assets/Branding/HighRes.png" >
</a>

<br>
<br>

<p>We also offer a illustrator file, if needed. </p>

<a href="../images/Assets/Branding/Logo.ai" download>  
<img width="200px" src="../images/AI_Icon.svg">
</a>

<h2>Colors</h2>
<p> Our team colors are Dark Purple, Pink, and Sky Blue . We determine which color is used based off of vibrance and cohesivness.</p>

<a href="../images/Assets/Branding/BrandingColors.png" download>
    <img width = "50%" src="../images/Assets/Branding/BrandingColors.png">
</a>

<h2>Fonts</h2>
<p>We use Dongle as our team font. Used in all logos, when available.</p>
<p class="hidden-when-failed" style="color: black; font-family: Dongle; font-size: 64px;">Dongle</p>
<p class="hidden-when-failed" style="color: black; font-family: Dongle; font-size: 28px;">"The quick brown fox jumps over the lazy dog."</p>
<p id="font-message" style="color: red; font-size: 16px;" class="font-message"></p>
</div>



<style>
    .font-message {
        color: black;
        font-family: Dongle, sans-serif;
        font-size: 28px;
    }
</style>
<script>
    function isFontLoaded(fontName) {
        var canvas = document.createElement("canvas");
        var context = canvas.getContext("2d");
        var text = "abcdefghijklmnopqrstuvwxyz0123456789";
        context.font = "40px " + fontName + ", sans-serif";
        var originalWidth = context.measureText(text).width;
        context.font = "40px sans-serif";
        var fallbackWidth = context.measureText(text).width;
        return originalWidth !== fallbackWidth;
    }
    
    // Check if Dongle font is loaded
    window.onload = function() {
        if (!isFontLoaded("Dongle")) {
            var messageElement = document.getElementById("font-message");
            messageElement.innerHTML = "It appears that you're using a browser that is not compatible with the Dongle font. This can be caused by an unexpected MIME type and/or an outdated browser. For the best viewing experience please use a different browser.";
            
            // Hide the lines that should only be displayed when Dongle font is rendered correctly
            var hiddenElements = document.getElementsByClassName("hidden-when-failed");
            for (var i = 0; i < hiddenElements.length; i++) {
                hiddenElements[i].style.display = "none";
            }
        }
    }
</script>
