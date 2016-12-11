Destroy the Monument
======================

Destroy the Monumentゲームモードでは相手チームの破壊対象オブジェクトを破壊する事が勝利条件です。

各チームには一つ以上の ``destroyable`` ハッシュが必要です。

また、それぞれのチームの ``destroyable`` ハッシュは名前がお互い同じ名前として対応している必要があります。別々の名前は使用出来ません

オブジェクト名の左右(L/R)については、攻撃側から見た左右を基準とします。

また、オブジェクト名で目標の場所がはっきりする場合はLeft,Rightに統一する必要はありません。 　　　（例： Adventure Island のocean,remains等。）

Code
^^^^^^^^

.. code-block:: yaml

    destroyables:
    - materials: obsidian
      completion: <モニュメント達成 パーセンテージ>

        destroyable:

        - owner: <モニュメントのチーム>
        　name: <モニュメント名>
        　cuboid:
        　- min: <x,y,z>
         　 max: <x,y,z>

        - owner: <モニュメントのチーム>
        　name: <モニュメント名>
        　cuboid:
        　- min: <x,y,z>
        　  max: <x,y,z>

Example
^^^^^^^^

.. code-block:: yaml

    destroyables:
    - materials: obsidian
      completion: 100%

        destroyable:

        - owner: red
        　name: Monument
        　cuboid:
        　- min: 94,5,-19
        　  max: 94,2,-19
        - owner: blue
        　name: Monument
        　cuboid:
        　- min: 4,5,-19
         　 max: 4,2,-19

destroyables ハッシュ説明
^^^^^^^^^^^^^^^^^^^^^^^^^^

.. csv-table::
   :header: 属性, 説明, 値
   :widths: 10, 80, 10

   "``materials``", ``必須`` モニュメントのMaterialを指定します。, `Material <http://pvp-docs.minecraft.jp/ja/latest/data/material.html>`_
   "``completion``", 目標の達成に必要なパーセンテージを指定します。, "`Number`"

destroyable ハッシュ説明
^^^^^^^^^^^^^^^^^^^^^^^^^
.. csv-table::
   :header: 属性, 説明, 値
   :widths: 10, 80, 10

   "``owner``", ``必須`` モニュメントのオーナーを指定します。 ``team`` ハッシュの ``color`` キーに入力した値を指定してください。, `Material <http://pvp-docs.minecraft.jp/ja/latest/data/material.html>`_
   "``name``", モニュメントの名前を指定します。, 文字列