# Fonts
The PDF standard references 14 standard fonts, which are not distributed with it.
Due to dubious practices by Adobe, it is not safe to publish them in the viewer.

You can download them [here](https://lbry.tv/pdf-standard-fonts.tar.bz:060d67b0d4f5ef9089853f3b314598e0e5d9c487) and unpack with
```
tar -xf fonts.tar.bz
```
placing the `fonts` directory in repository directory.

Finally set the environment variable `STANDARD_FONTS` to the fonts folder:
```
export STANDARD_FONTS=$pwd/fonts
```

Alternativly you can run `./download_fonts.sh` to get them from [this old debian release of the Adobe PDF reader](http://ardownload.adobe.com/pub/adobe/reader/unix/9.x/9.5.5/enu/AdbeRdr9.5.5-1_i386linux_enu.deb). And `AdobePiStd.ttf` can be found on the internet as well:

Note that the `Arial*` files are not included here. Your options are:
 - get them from somewhere else
 - skip them (see note below)

Over all you will need in the `fonts` directory:
 - `CourierStd.otf`
 - `CourierStd-Bold.otf`
 - `CourierStd-Oblique.otf`
 - `CourierStd-BoldOblique.otf`
 - `MinionPro-Regular.otf`
 - `MinionPro-Bold.otf`
 - `MinionPro-It.otf`
 - `MinionPro-BoldIt.otf`
 - `MyriadPro-Regular.otf`
 - `MyriadPro-Bold.otf`
 - `MyriadPro-It.otf`
 - `MyriadPro-BoldIt.otf`
 - `SY______.PFB`
 - `AdobePiStd.otf`
 - `Arial-BoldMT.otf`
 - `ArialMT.ttf`
 - `Arial-ItalicMT.otf`

**Note**: If you do not have this exact list, update `STANDARD_FONTS` in `pdf/src/fonts.rs` accordingly.

Once you have the fonts, you can enable the `standard-fonts` feature for the pdf crate.
