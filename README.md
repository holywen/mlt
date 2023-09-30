# Magic Lantern Translator
A PoC Magic Lantern module that implements localization in the menus.

![demo](demo.jpg)

## Usage
Drop `mlt.mo` in `ML/modules`.

In order to get menu text items, I logged bmp_printf  
input into a file and removed duplicates and generated  
strings.  

The `bmp_printf` function is hijacked in order to add output translated strings.

## Help Translate
You can edit translations generated by Google Translate.  
French:  https://docs.google.com/document/d/14A0eS9CKrAxoJHmEkFWCfA-011OPeWJIFAH7dp3Stx8/edit?usp=sharing  
German:  https://docs.google.com/document/d/1munmZIPLASBq0aGodO7J9vumgD9TcqnhCKuxYtc72Y8/edit?usp=sharing  
Spanish: https://docs.google.com/document/d/1cg7afAO2GxoiJX2iHze2Ntu36CBteEo_miUcJ_kXG7c/edit?usp=sharing  

## Compiling
```
make
```

You can compile with the following flags:
- `MCUFONT=X`: Compile with the [mcufont](https://github.com/mcufont/mcufont) rendering backend.  

## TODO/Help Needed:
- [ ] Manually review translations, and add more translations
- [ ] Case insensitive string searching (possibly ignore symbols too)
- [ ] "Translate" parts of a string, ignoring generated parts

## How's Speed?
As for now this is just a PoC so it just runs through a large table of strings to find the translated output. This doesn't seem to make the menus slower,
but it will be rewritten with a hashmap in the final implementation. The final implementation should have no performance impact.


# Credits
https://github.com/mcufont/mcufont (MIT License)  
(https://github.com/fcambus/spleen) Uses "spleen" 12x24 BDF font, (BSD 2-Clause "Simplified" License)  
