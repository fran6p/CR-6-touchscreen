# CR-6 Touchscreen software
Attempt to extend the CR-6 touch screen software. You need the [DGUS v8.0.x software](http://dwin.com.cn/home/Index/download_file?download_id=4796) for that.

You can open the .dgus project file in the [`src\DWIN`](src\DWIN) folder:

![DGUS II interface](doc/dgus2util.png)

## Images / screen images sources

You can find the source files where the screen bitmaps are generated from in the [`src\images_src`](src\images_src) folder.

## How buttons are handled with code

This picture says it all:

![DWIN button-code correlation](doc/button_type.png)

How the code currently works is that there is an `AddrBuf` array that contains the Virtual Pointer addresses (check chapter 7 in [docs/vendor/T5L_DGUSII Application Development Guide20200902.pdf](./docs/vendor/T5L_DGUSII%20Application%20Development%20Guide20200902.pdf)). The enum `PROC_COM` contains the indices in that array. 

Virtual Pointer addresses are shared between buttons, so the "Key Data" is used to distinguish between the actual key pressed.

## Other documentation

Vendor documentation is mirrored to the [doc/vendor](doc/vendor) folder.

In addition, [this is a nice resource](https://github.com/rubienr/MarlinDgusResources/tree/creality-ender-5-plus/projects).
