tailor
======

.. dfhack-tool::
    :summary: Automatically keep your dwarves in fresh clothing.
    :tags: fort auto workorders

Once a day, this plugin will scan the clothing situation in the fort. If there
are fresh cloths available, dwarves who are wearing tattered clothing will have
their rags confiscated (in the same manner as the `cleanowned` tool) so that
they'll reequip with replacement clothes.

If there are not enough clothes available, manager orders will be generated to
manufacture some more. ``tailor`` will intelligently create orders using raw
materials that you have on hand in the fort. For example, if you have lots of
silk, but no cloth, then ``tailor`` will order only silk clothing to be made.

Usage
-----

::

    enable tailor
    tailor [status]
    tailor now
    tailor materials <material> [<material> ...]

By default, ``tailor`` will prefer using materials in this order::

    silk cloth yarn leather

but you can use the ``tailor materials`` command to restrict which materials
are used, and in what order.

Examples
--------

``enable tailor``
    Start replacing tattered clothes with default settings.

``tailor now``
    Run a scan and order cycle right now, regardless of whether the plugin is
    enabled.

``tailor materials silk cloth yarn``
    Restrict the materials used for automatically manufacturing clothing to
    silk, cloth, and yarn, preferred in that order. This saves leather for
    other uses, like making armor.
