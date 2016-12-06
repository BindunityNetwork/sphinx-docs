マップチュートリアル
====================

XML内で定義する事によりそのマップを遊ぶ方法などのチュートリアルを作成する事が出来ます。

チュートリアル機能を使用する場合には、必ず ``tutorial.xml`` を読み込む必要があります。


.. code-block:: yaml

    include:
    - src: tutorial.xml

チュートリアルはいくつかのステージに分かれて進行し、各ステージ内で表示するメッセージ、テレポート座標などを定義します。

チュートリアル内でユーザに表示するメッセージは ``line`` ハッシュを使用し、1行ずつ定義します。 テレポートの使用については必須ではありません。

``message`` 及び ``title`` ハッシュについては ``lang`` にRFC3066で規定されている国識別コードサブノードを含む言語コードを指定する事でクライアントの言語設定に合わせたチュートリアルを表示する事が出来ます。

Code
--------

.. code-block:: yaml

    tutorial:
    - stage:
        - title: <title>
            titletag:
            - lang: <titleの言語設定>
              name: <title_lang>
            message:
            - line:
                - message: <message>
                - message: <message>
            - lang: <messageの言語設定>
              line:
                - message: <message_lang>
                - message: <message_lang>

Example
--------

.. code-block:: yaml

    tutorial:
    - stage:
        - title: Introduction
            titletag:
            - lang: ja_JP
            　name: はじめに
            message:
            - line:
                - message: You have observed the game now and cannot interfere in other players.
                - message: '`8`lRight click `rto learn about this map!'
            - lang: ja_JP
            　line:
                - message: 現在ゲームを`b観戦`fしています。他のプレイヤーに干渉する事は出来ません。
                - message: '`8`l右クリック`rしてこのマップについて学びましょう。'
        - title: Finish
            titletag:
            - lang: ja_JP
            　name: 完了
            message:
            - line:
                - message: All things are required to play this map learned.
                - message: Join a team by typing `b/join `ror using the `6`lTeam Selector `rin your inventory.
            - lang: ja_JP
                line:
                - message: このマップについて必要な事をすべて学びました。早速参加してみましょう！
                - message: ゲームに参加するには`b/join`rコマンドを使用するかインベントリー内の`6`lチーム選択`rツールを使用してください。