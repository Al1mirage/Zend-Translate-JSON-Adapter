Zend-Translate-JSON-Adapter (FORK FOR JSPERANTO)
================================================

A JSON Adapter for the Zend Translate Module

Allows the use of JSON resource files.
Example:

    {
      "app": {
        "name": "MY AWESOME APP",
        "version": "1.0",
        "events": {
          "jump": "The quick brown __subject__ __action__ over the lazy __object__"
        }
      }
    }

You can access the translations hierarchical e.g. `$translate->_("app.name")`

Simply pass additional parameters as an associative array, e.g.
`$translate->_("app.events.jump", array('subject' => 'fox', 'action' => 'jumps', 'object' => 'dog'))`

# Initialisation #

You can simply put the file into the Zend/Translate directory to initialise it like the other adapters:

    $translate = new Zend_Translate(
        array(
            'adapter' => 'Json',
            'content' => 'translations/de.json',
            'locale'  => 'de'
        )
    );

or follow the [Zend Translate Guidelines](http://framework.zend.com/manual/en/zend.translate.adapter.html#zend.translate.adapter.selfwritten) on integrating self written adapters.


# Motivation #

This is just a fork of adapter originally created by [SxDx](https://github.com/SxDx), but updated to be more consistent
with jQuery translation library [jsperanto](https://github.com/jpjoyal/jsperanto), and my motivation is mostly the same :)