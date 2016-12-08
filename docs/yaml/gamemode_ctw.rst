Capture the Wool
================

Capture the Woolゲームモードは相手チームの陣地から羊毛を奪い、自チームの台座に設置する事が勝利条件です。

各チームには1つ以上の ``wool`` ハッシュが必要です。 現時点では目標が多すぎる場合、スコアボードが表示されなくなるため目標を減らすなどの対応を行ってください。

.. code-block:: yaml

    wools:
    - wool:
        - team: <team>
        color: <color>
        block:
        - location: <x,y,z>

        - team: <team>
        color: <color>
        block:
        - location: <x,y,z>

        - team: <team>
        color: <color>
        block:
        - location: <x,y,z>

        - team: <team>
        color: <color>
        block:
        - location: <x,y,z>

Example
--------

.. code-block:: yaml

    wools:
    - wool:

        - team: red
        color: magenta
        block:
        - location: -61.0,8.0,66.0

        - team: red
        color: pink
        block:
        - location: -24.0,8.0,29.0

        - team: blue
        color: green
        block:
        - location: 24.0,8.0,151.0
        
        - team: blue
        color: lime
        block:
        - location: 61.0,8.0,114.0

wool ハッシュの説明
^^^^^^^^^^^^^^^^^^

.. csv-table:: 
    :header: "ハッシュ", "説明", "値"
    :widths: 15, 10, 20

    "``block``", 羊毛を設置する座標です。 Regionで指定します。, :doc:`Region </yaml/regions.html>`
    "``team``", 羊毛を設置する側のチーム名です。, `Chat Color <http://pvp-docs.minecraft.jp/ja/latest//data/chatcolor>`_
    "``color``", 設置する羊毛の色です。羊毛の色はDyeColorをご覧ください。, `Dye Color <http://pvp-docs.minecraft.jp/ja/latest//data/dyecolor>`_