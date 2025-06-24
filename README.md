# DitherDown URP

DitherDown URP is a dithering and quantization post process for Unity URP.

## How to use

**Note:** Your camera must have the **Post Processing** property set to *enabled* for the pixelization effect to work properly.

In your **URP Asset** set your **Upscaling Filter** to *Nearest-Neighbour*. Set the **Render Scale** property to something like *0.3333336*; I use the target resolution divided by the screen height to calculate the desired scale, ex. 360/1080 = 0.3333336.

Add a **Full Screen Render Pass Feature** to your **URP Renderer**. Set the **Pass Material** to the *DitherDown* material. Set the **Injection Point** to *After Rendering Post Processing*. Set the **DitherTexture**, **DitherAmount**, **ColorResolution**, and **ScreenScale** properties accordingly. The **ScreenScale** should be matched to the **Render Scale** you set in your **URP Asset**.

## Example
![Example 1](https://cdn.bsky.app/img/feed_thumbnail/plain/did:plc:lox54mi3njidfxxufmci3bdm/bafkreiafyk4napwe4pmtslebggsljimw6dvhan3xipyovwnb7mc7pz4wca@jpeg)
![Example 2](https://cdn.bsky.app/img/feed_thumbnail/plain/did:plc:lox54mi3njidfxxufmci3bdm/bafkreihkpq2ug7vtm3bm3nshzqxyvl3x767icjvvh5722ul2udfwlz5hve@jpeg)