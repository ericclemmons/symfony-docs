.. index::
   single: Forms; Fields; percent

percent Field Type
==================


The ``percent`` type renders an input text field and specializes in handling
percentage data. If your percentage data is stored as a decimal (e.g. ``.95``),
you can use this field out-of-the-box. If you store your data as a number
(e.g. ``95``), you should set the ``type`` option to ``integer``.

This field adds a percentage sign "``%``" after the input box.

+-------------+-----------------------------------------------------------------------+
| Rendered as | ``input`` ``text`` field                                              |
+-------------+-----------------------------------------------------------------------+
| Options     | - ``type``                                                            |
+-------------+-----------------------------------------------------------------------+
| Inherited   | - ``required``                                                        |
| options     | - ``label``                                                           |
|             | - ``read_only``                                                       |
|             | - ``error_bubbling``                                                  |
+-------------+-----------------------------------------------------------------------+
| Parent type | :doc:`field</reference/forms/types/field>`                            |
+-------------+-----------------------------------------------------------------------+
| Class       | :class:`Symfony\\Component\\Form\\Extension\\Core\\Type\\PercentType` |
+-------------+-----------------------------------------------------------------------+

Options
-------

* ``type`` [type: string, default: ``fractional``]
    This controls how your data is stored on your object. For example, a percentage
    corresponding to "55%", might be stored as ``.55`` or ``55`` on your
    object. The two "types" handle these two cases:
    
    * ``fractional``
        If your data is stored as a decimal (e.g. ``.55``), use this type.
        The data will be multiplied by ``100`` before being shown to the
        user (e.g. ``55``). The submitted data will be divided by ``100``
        on form submit so that the decimal value is stored (``.55``);
    * ``integer``
        If your data is stored as an integer (e.g. 55), then use this option.
        The raw value (``55``) is shown to the user and stored on your object.
        Note that this only works for integer values.

Inherited Options
-----------------

These options inherit from the :doc:`field</reference/forms/types/field>` type:

.. include:: /reference/forms/types/options/required.rst.inc

.. include:: /reference/forms/types/options/label.rst.inc

.. include:: /reference/forms/types/options/read_only.rst.inc

.. include:: /reference/forms/types/options/error_bubbling.rst.inc
