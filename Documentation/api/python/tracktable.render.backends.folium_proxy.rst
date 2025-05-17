================================================
tracktable.render.backends.folium_proxy module
================================================

Folium is a wrapper around `leaflet.js <https://leafletjs.com>`_.  As such, it includes links for the browser to go download Leaflet and whatever plugins are being used.  This works great on systems connected to the Internet but fails on isolated networks or stand-alone systems.

Most institutions that deal with this on a regular basis have built their own versions of Folium that either embeds the Javascript resources inline or changes the URLs to point to servers accessible on whatever network they use.  The point of the ``folium_proxy`` module is to make it easier to use those alternate versions of Folium.

Here's how we use it:

.. code-block:: python

    # Instead of this...
    import folium

    # Do this.
    from tracktable.render.backends import folium_proxy
    folium = folium_proxy.import_folium()

    # Instead of this...
    from folium.plugins import heat_map

    # Do this.
    from tracktable.render.backends import folium_proxy
    heat_map = folium_proxy.import_folium("plugins.heat_map")

::


By default, the ``import_folium`` method will first try to import the package ``offlinefolium``.  If it can't find that package, it will fall back to regular Folium.

You can change the name of the package that ``import_folium`` looks for by calling ``set_folium_proxy_name(new_module_name)``, documented below.  You can disable the proxy mechanism entirely with ``set_folium_proxy_enabled(onoff)``.

This is a new feature in Tracktable 1.7.2.  We are experimenting with different approaches in the hope of simplifying it further.



---------------
Module contents
---------------

.. automodule:: tracktable.render.backends.folium_proxy
    :members:
