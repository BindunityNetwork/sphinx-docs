Destroy the Core
==================

Destroy the Coreゲームモードは相手チームのコアと呼ばれるオブジェクトから溶岩を流出させる事が勝利条件です。 コアの中には溶岩が入っており、コア領域の外まで一定以上溶岩が流れ出ると勝利判定になります。

各チームに一つ以上の ``core`` ハッシュが必要です。また、各チームの ``core`` ハッシュはお互いに対応している必要があります。

Code
^^^^^^^^

.. code-block:: yaml

    cores:
    - material: <時間経過によるブロック変化を起こすブロック>
      leak: <溶岩の流す長さを指定>
      core:
      - team: <チーム指定>
        <regionの指定>:
      - team: <チーム指定>
        <regionの指定>:

Example
^^^^^^^^

.. code-block:: yaml

    cores:
    - material: obsidian
    　leak: 7
    　core:
    　- team: red
    　  cuboid:
        - min: -1,26,-69
          max: 1,24,-67
      - team: blue
        cuboid:
        - min: 1,26,69
          max: -1,24,67


.. csv-table:: 
    :header: "ハッシュ", "説明","値"
    :widths: 15, 10, 20

    "``material``", 	時間経過によるブロック変化を起こすブロックを決めます。, `Material <http://pvp-docs.minecraft.jp/ja/latest/data/material.html>`_
    "``leak``", 	溶岩の流す長さを指定します。指定した数字以上の流れが発生すると試合が終わります。, "`Number`"

注意事項
--------

* コアは ``material`` に指定した素材で完全に囲むようにしてください。
* コアの範囲座標は外郭がすべて収まる範囲を指定してください。