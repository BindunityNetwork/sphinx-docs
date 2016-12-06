外部XMLファイル
=============

マップ定義の各項目は別のXMLファイルに記載し、各マップのXMLファイルから読み込むこともできます。各マップで共通のクラスやキットなどに使用可能です。

Code <Single>
--------

.. code-block:: yaml

    include:
    - src: tutorial.xml

Code <Multiple>
--------

.. code-block:: yaml

    include:
    - src: tutorial.xml
    - src: splatt.xml