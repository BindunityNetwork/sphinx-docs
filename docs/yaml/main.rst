マップ構造
===========

全てのYAML定義ファイルは ``xmlname`` 及び ``map`` ハッシュが存在していなければなりません。 また、ファイルの文字コードはUTF-8を使用してください。
現在のYAML定義ファイルの対応バージョンは ``1.3.3`` です。

Code
--------

.. code-block:: yaml

    xmlname:
        space: ""
        local: map
    map:
        proto: 1.3.3
        name: <マップ名>
        version: <マップバージョン>
        objective: <マップの説明>
        authors:
        - author:
            - name: <マップ作者>
            contribution: <貢献内容>
        contributors:
        - contributor:
            - name: <マップ制作協力者>
            contribution: <貢献内容>

Example
--------

.. code-block:: yaml

    xmlname:
        space: ""
        local: map
    map:
        proto: 1.3.3
        name: Example
        version: 1.0.0
        objective: Capture the Control point!
        authors:
        - author:
            - name: example
            contribution: XMLCoding
        contributors:
        - contributor
            - name: example
            contribution: Builder