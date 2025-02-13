:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/master/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/master/doc/classes/EditorResourcePreviewGenerator.xml.

.. _class_EditorResourcePreviewGenerator:

EditorResourcePreviewGenerator
==============================

**Inherits:** :ref:`RefCounted<class_RefCounted>` **<** :ref:`Object<class_Object>`

Custom generator of previews.

.. rst-class:: classref-introduction-group

Description
-----------

Custom code to generate previews. Please check ``file_dialog/thumbnail_size`` in :ref:`EditorSettings<class_EditorSettings>` to find out the right size to do previews at.

.. rst-class:: classref-reftable-group

Methods
-------

.. table::
   :widths: auto

   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`bool<class_bool>`           | :ref:`_can_generate_small_preview<class_EditorResourcePreviewGenerator_method__can_generate_small_preview>` **(** **)** |virtual| |const|                                                        |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Texture2D<class_Texture2D>` | :ref:`_generate<class_EditorResourcePreviewGenerator_method__generate>` **(** :ref:`Resource<class_Resource>` resource, :ref:`Vector2i<class_Vector2i>` size **)** |virtual| |const|             |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Texture2D<class_Texture2D>` | :ref:`_generate_from_path<class_EditorResourcePreviewGenerator_method__generate_from_path>` **(** :ref:`String<class_String>` path, :ref:`Vector2i<class_Vector2i>` size **)** |virtual| |const| |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`bool<class_bool>`           | :ref:`_generate_small_preview_automatically<class_EditorResourcePreviewGenerator_method__generate_small_preview_automatically>` **(** **)** |virtual| |const|                                    |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`bool<class_bool>`           | :ref:`_handles<class_EditorResourcePreviewGenerator_method__handles>` **(** :ref:`String<class_String>` type **)** |virtual| |const|                                                             |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Method Descriptions
-------------------

.. _class_EditorResourcePreviewGenerator_method__can_generate_small_preview:

.. rst-class:: classref-method

:ref:`bool<class_bool>` **_can_generate_small_preview** **(** **)** |virtual| |const|

If this function returns ``true``, the generator will call :ref:`_generate<class_EditorResourcePreviewGenerator_method__generate>` or :ref:`_generate_from_path<class_EditorResourcePreviewGenerator_method__generate_from_path>` for small previews as well.

By default, it returns ``false``.

.. rst-class:: classref-item-separator

----

.. _class_EditorResourcePreviewGenerator_method__generate:

.. rst-class:: classref-method

:ref:`Texture2D<class_Texture2D>` **_generate** **(** :ref:`Resource<class_Resource>` resource, :ref:`Vector2i<class_Vector2i>` size **)** |virtual| |const|

Generate a preview from a given resource with the specified size. This must always be implemented.

Returning an empty texture is an OK way to fail and let another generator take care.

Care must be taken because this function is always called from a thread (not the main thread).

.. rst-class:: classref-item-separator

----

.. _class_EditorResourcePreviewGenerator_method__generate_from_path:

.. rst-class:: classref-method

:ref:`Texture2D<class_Texture2D>` **_generate_from_path** **(** :ref:`String<class_String>` path, :ref:`Vector2i<class_Vector2i>` size **)** |virtual| |const|

Generate a preview directly from a path with the specified size. Implementing this is optional, as default code will load and call :ref:`_generate<class_EditorResourcePreviewGenerator_method__generate>`.

Returning an empty texture is an OK way to fail and let another generator take care.

Care must be taken because this function is always called from a thread (not the main thread).

.. rst-class:: classref-item-separator

----

.. _class_EditorResourcePreviewGenerator_method__generate_small_preview_automatically:

.. rst-class:: classref-method

:ref:`bool<class_bool>` **_generate_small_preview_automatically** **(** **)** |virtual| |const|

If this function returns ``true``, the generator will automatically generate the small previews from the normal preview texture generated by the methods :ref:`_generate<class_EditorResourcePreviewGenerator_method__generate>` or :ref:`_generate_from_path<class_EditorResourcePreviewGenerator_method__generate_from_path>`.

By default, it returns ``false``.

.. rst-class:: classref-item-separator

----

.. _class_EditorResourcePreviewGenerator_method__handles:

.. rst-class:: classref-method

:ref:`bool<class_bool>` **_handles** **(** :ref:`String<class_String>` type **)** |virtual| |const|

Returns ``true`` if your generator supports the resource of type ``type``.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
