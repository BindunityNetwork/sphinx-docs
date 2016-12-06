Team Death Match
======================

Team Death Matchではチーム毎にキル数を競い合い、時間内でより多くのキル数、またはリミットに到達したチームが勝利になります。

Code
--------

.. code-block:: yaml

    score:
    - time:
        - sec: <制限時間 （秒）>
        limit:
        - int: <キル数リミット （指定は自由）>

Example
--------

.. code-block:: yaml

    score:
    - time:
        - sec: 600
        limit:
        - int: 100