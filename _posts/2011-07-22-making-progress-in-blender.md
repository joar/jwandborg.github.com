---
layout: post
title: Making progress in blender
category: blender
---
The last two days I have been following a [blender tutorial](http://www.blendercookie.com/2010/11/04/creating-a-bunch-of-balloons/)
at [Blender Cookie](http://www.blendercookie.com/).

This is my first go at it, click on the images for higher resolution.

<pc>
{{ "[![Balloons](/images/balloons-540.png)](/images/balloons.png)" | markdownify }}
</pc>

You can see that the background is a bit grainy, it is more obvious if 
you view the large image. That's because my skydome (a large hemisphere 
with texture on the inside) texture did not have high enough resolution.

I downloaded a new skydome texture, this time with a resolution of 
8591x3912px.

<div class="privilegied-content">
{{ "[![Balloons 2](/images/balloons-2-540.png)](/images/balloons-2.png)" | markdownify }}
</div>

Much better! But still, the balloons have some quite dark patches.

Increasing the global light of the render, and voila!

<pc>
{{ "[![Balloons 3](/images/balloons-3-540.png)](/images/balloons-3.png)" | markdownify }}
</pc>

The clouds are a bit overexposed, but it's good for a training render.
