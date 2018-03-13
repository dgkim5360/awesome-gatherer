======================
 Awesome-Gatherer
======================

A Python script that run through the directory structure and collecting json data to make an awesome list.

Check out `this repository`_ for the live example.

.. _this repository: https://github.com/dgkim5360/today-i-found

Directory Structure
===================

::

  root/
  ├── gather (executable python script)
  ├── data.json
  ├── folder1
  │   └── data.json
  ├── folder2
  │   ├── data.json
  │   ├── folder2-1
  │   │   └── data.json
  │   └── folder2-2
  │       └── data.json
  └── folder3
      └── data.json

``root`` and its all subdirectory should contain ``data.json`` file for generating ``README.rst``.

Json Structure
==============

Currently items in ``data.json`` should contain ``group``, ``title``, and ``link`` as its fields.

::

  [
    {
      "group": "Reddit",
      "title": "Awesome post on Linus Torvalds",
      "link": "https://reddit.com/..."
    },
    ...
  ]

If there is no items for a category, just leave it as an empty array.

Usage
=====

1. Place ``gather`` script in your project root. (Clone it, or whatever)
2. Make category directories and add ``data.json``.
3. If each directory has its own ``data.json``, then it's ready to gather.

::

  $ ./gather

Since the ``gather`` is a plain Pythen script, modify it for your own purpose.

Lisence
=======

Please see ``COPYING``.
