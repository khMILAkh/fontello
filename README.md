Fontello - icon font scissors
=============================

[![Build Status](https://travis-ci.org/fontello/fontello.png)](https://travis-ci.org/fontello/fontello)

Website: [fontello.com](http://fontello.com/)

This tool lets you combine icon webfonts for your own project. With fontello you can:

1. shrink glyph collections, minimizing font size
2. merge symbols from several fonts into a single file
3. access large sets of professional-grade open source icons

Now it's trivial to make a custom icon webfont, exactly for your needs.
First, select the icons you like. Then update glyph codes (optional), and
download your webfont bundle. We generate everything you need, ready for publishing
on your website!

Don't forget about donations :)


## Compatibility

1. Desktop is fully supported. IE6-7 requires alternate CSS.
2. Mobiles - all modern systems work without problems. There are limits on very old androids
   and rare browsers. Also, Windows Mobile IE9 sucks, as IE  usually does :) . See
   [details](http://blog.kaelig.fr/post/33373448491/testing-font-face-support-on-mobile-and-tablet).


## Developers API

Fontello allows easy scripting, to implement different convenient features:

1. Open site from command line, with your configuration, and import edited project
    - [Makefile example](https://gist.github.com/puzrin/5537065). That's a live working code, used
      for development of fontello itself.
2. Writing website plugins, to import/export icons via admin panel.

When more examples available, those will be added here.


### API methods

1. `POST http://fontello.com/` creates a session with your config and
   return you `session_id`. You can use it later to open fontello with you configuration
   and to automatically download your font. Session is stored for 24h. POST params
   (form-encoded):
    - `config` - content of `config.json` for your font
    - `url` - if used, download button will link to your admin panel, where you can
      run importing script.
2. `http://fontello.com/[session_id]` - opening fontello with your config preloaded.
   When you edit font, your config is automatically sent to server
3. `http://fontello.com/[session_id]/get` - download your font.

Note. When you open site via API url, `download` button will have another text.


## Embedded Fonts <a name="embedded"></a>

Fontello comes with the following embedded set of icon fonts:

- [__Entypo__](http://www.entypo.com/) by Daniel Bruce (CC BY-SA license)
- [__Font Awesome__](http://fortawesome.github.com/Font-Awesome//) by Dave Gandy (CC BY-SA license)
- [__Iconic__](https://github.com/somerandomdude/Iconic) by P.J. Onori (SIL OFL)
- [__Typicons__](http://typicons.com/) by Stephen Hutchings (CC BY-SA 3.0 license)
- [__Modern Pictograms__](http://thedesignoffice.org/project/modern-pictograms/) by John Caserta (SIL OFL)
- [__Meteocons__](http://www.alessioatzeni.com/) by Alessio Atzeni (SIL OFL)
- [__Fontelico__](https://github.com/fontello/fontelico.font) by... all :) (SIL OFL)
- [__Web Symbols__](http://www.justbenicestudio.com/studio/websymbols/) by Just Be Nice studio (SIL OFL)
- [__Brandico__](https://github.com/fontello/brandico.font) by... all :) (SIL OFL)

Please, note that these embedded fonts differ from the original files. We did some
modifications to unify characteristics such as scale, ascent/descent and alignment.


## Contacts

- Questions: [Google group](https://groups.google.com/group/fontello/)
- Bug reports: [Issue tracker](https://github.com/fontello/fontello/issues)
- Suggestion for adding your OFL fonts or other collaborations: vitaly@rcdesign.ru


## Authors

- Roman Shmelev ([shmelev](https://github.com/shmelev))
- Vitaly Puzrin ([puzrin](https://github.com/puzrin)).
  [Follow](https://twitter.com/puzrin) on twitter.
- Aleksey Zapparov ([ixti](https://github.com/ixti)).
  [Follow](https://twitter.com/zapparov) on twitter.
- Evgeny Shkuropat ([shkuropat](https://github.com/shkuropat)).


## License

Fontello's code (all files, except fonts) is distributed under MIT license. See
[LICENSE](https://github.com/fontello/fontello/blob/master/LICENSE) file for details.

Embedded fonts are distributed under their primary licenses (SIL OFL / CC BY / CC BY-SA).
See section [Embedded Fonts](#embedded) above for credits & links to font homepages.

Generated fonts are intended for web usage, and should not be
considered/distributed as independent artwork. Consider fontello a
font archiver and credit original font creators according to their respective license.

Crediting fontello is not required :)
