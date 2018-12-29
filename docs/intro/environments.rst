.. role:: strike
    :class: strike
	
**************************
Среда разработки
**************************

.. contents:: Оглавление
   :local:
   
-------


BitShares позволяет вам установить BitShares-Core на различные платформы; :ref:`Linux:Ubuntu (x64) <build-ubuntu>` , :ref:`OS X <build-osx>` , and :ref:`Windows <build-windows>`.   Зависимости которые требуеться проверить при загрузке это OpenSSL и Boost. Пожайлуста, проверьте какие версии вы скачали.

Кроме того, если вы являетесь пользователем Windows, у вас есть два других варианта установки BitShares Core в операционной системе Windows (x64). Первый - :ref:`CLI-Wallet для Windows (x64) <cli-tool>` , Второй :ref:`Windows SubSystem for Linux (WSL) <build-wsl>` 
 
Инструмент CLI-wallet для Windows (x64) позволят вам использовать CLI-wallet без установки BitShares Core. После того, как вы загрузите Cli-Wallet (zip-файл) и разархивируете его, в нем вы найдете все файлы необходимые для запуска CLI-wallet.

Другой вариант, Windows SubSystem for Linux (WSL). WSL предназначен для разработчика, который использует операционную систему Windows 10 (x64) и хочет собрать BitShares Core в Ubuntu.

> See :ref:`Системные требования <system-requirements-node>` .


-------------------

Код и файлы BitShares 
===============================


- Программа с открытым исходным кодом
- Языки используются (в основном): BitShares-Core(C++), Python, JavaScript
- `BitShares GitHub <https://github.com/bitshares>`_
   - **BitShares-Core (C++)** - Реализация блокчейна BitShares и интерфейс командной строки.
   - **Bitshares-FC** - Быстро компилируемая библиотека C ++ 
   - **BitShares python** - Полнофункциональная клиентская библиотека для блокчейна BitShares - полностью написана на Python.
   - **BitShares-UI** - Полнофункциональный графический интерфейс пользователя/ Рекомендованный кошелек для блокчейна BitShares.
   - **BSIPs** - Предложения и протоколы по улучшению BitShares. В этих технических документах описывается процесс обновления и улучшения блокчейна BitShares и технической экосистемы.
   - **BitSharesjs** - Инструменты JavaScript для шифрования и сериализации BitShares.
   - **BitSharesjs-ws** - Javascript websocket интерфейс для Bitshares 
   - (еще...)

----------
   
Какие у вас интересы?
========================

Что бы вы хотели узнать больше о блокчейне BitShares? Если вам интересно узнать больше о происхождении блокчейна BitShares, его истории, и возможностях, посетите `how.bitshares.works <http://how.bitshares.works/en/latest/#>`_ и `bitshares.org <https://bitshares.org/>`_ для того чтобы узнать больше информации

Если у вас нет аккаунта в BitShares , вы можете воспользоваться графическим кошельком на сайте (`wallet.bitshares.org <https://wallet.bitshares.org>`_ ) или скачать  `Light Client Wallet <https://bitshares.org/download>`_  для создания аккаунта BitShares. Вот последняя версия `BitShares-UI – Release <https://github.com/bitshares/bitshares-ui/releases>`_ . 

Если вам интересно попробовать и изучить функции BitShares, вы можете воспользоваться BitShares TestNet для того чтобы испытать их.Если вы разработчик, который заинтересован внести свой вклад в команду BitShares Core, вы можете скачать ветку для разработчиков и узнать больше о текущем проекте BitShares-Core, который может стать хорошим началом вашего вклада. Выберите соответствующую ветку при установке BitShares-Core.

После того, как вы узнаете, какую ветку загрузить, следующим шагом будет установка BitShares-Core. Проверьте :ref:`Руководство по установке BitShares <installation-guide>` и выберите свою операционную систему, чтобы выполнить шаги установки. 

.. image:: ../../_static/imgs/your-interests.png
        :alt: BitShares
        :width: 750px
        :align: center
  

В BitShares есть отличные сообщества, чтобы поддержать других разработчиков и проводить обсуждения разработки. Посмотрите :ref:`BitShares communities <bitshares-communities>` и присоединяйтесь чтобы встретиться с другими держателями BTS!    
  
|
  
----------------   
   
   
   
BitShares Core: Руководство по проектам 
==================================

Если вы заинтересованы в том, чтобы изучить или принять участие в разработке BitShares-Core, вы найдете руководство по вкладам, текущий проект, проблемы и планы в этом разделе.

Руководство по проекту и основные этапы
------------------------------

- `Руководство по вкладам [Проект] <https://github.com/bitshares/bitshares-core/wiki/Contribution-Guide>`_
- `Проект <https://github.com/bitshares/bitshares-core/projects/6>`_
- `BitShares-Core: текущие проблемы и запросы <https://github.com/bitshares/bitshares-core/issues>`_ 
- `Этапы и Планы <https://github.com/bitshares/bitshares-core/milestones>`_ 
- `BitShares-Core Релизы <https://github.com/bitshares/bitshares-core/releases>`_ 


BitShares-Core (Команда) 
^^^^^^^^^^^^^^^^^^^^^^^
 
Команда BitShares-Core - это команда разработчиков, которые управляют кодом репозитория BitShares-Core и решают проблемы, представленные другими разработчиками. Команда создает планы проекта для следующих выпусков и передает результат сообществу Bitshares.

* Роли

  - улучшение
  - поддержка
  - обновление протокола при необходимости
  - составление планов проекта для будущих релизов
  - создание/ анонс релиза
  - поддержка сообщества BitShares / ответы на вопросы
  
	
------------------	
	
BitShares Core: GitFlow
=========================

Цель
-------------

* Цель этого документа, описать и определить, как происходят изменения  в нашем коде на разных этапах разработки, пока он наконец, не перейдет в продакшн.
* Общая идея основана на `git-flow <https://datasift.github.io/gitflow/IntroducingGitFlow.html>`_
* Для наших целей концепция Gitflow была расширена, чтобы учесть дополнительные потребности:

1. У нас есть два различных выпуска, mainnet и testnet, с ветвью master для каждого.
2. Мы должны различать изменения, влияющие на консенсус (хардфорки), и изменений, не влияющих на консенсус.


Без консенсуса: Разработка / Релиз / Исправление ошибок
-----------------------------------------------------------

.. image:: ../../_static/structures/bts-non-concensus.png
        :alt: BitShares
        :width: 750px
        :align: center

При консенсусе: Разработка / Релиз / Исправление ошибок
------------------------------------------------------

.. image:: ../../_static/structures/bts-concensus.png
        :alt: BitShares 
        :width: 750px
        :align: center


Цели
---------------------

1. Поддержите две независимые версии релиза, testnet и mainnet.
2. Отделите разработку от релизов, то есть сохраняйте возможность создавать аварийные исправления для текущего релиза, не вводя в работу недоработанные новые функции.
3. Отделяйте изменения, связанные с консенсусом и изменения не связанных с консенсусом.
4. Поддерживайте совместимость веток разработки с mainnet.

Основные правила
---------------

1. Разработка всегда происходит в приватных тематических ветках. Единственным исключением является изменение, которое необходимо разместить в ветви master  (пример: дата хардфорка в testnet).
2. Функции объединяются после того, как они достаточно доработаны, т.е. они идут с модульными тестами, которые обеспечивают стабильную работу и не сообщают о каких-либо ошибках.
  - «Завершенные» функции, не связанные с консенсусом, объединяются в «Develop».
  - «Завершенные» функции, связанные с консенсусом, объединяются в ветку «hardfork» с датой hardfork в далеком будущем.
  - Все слияния с «Develop» или «hardfork» выполняются с помощью PR на github и требуют проверки и одобрения со стороны основного разработчика (если PR создается с помощью основного разработчика, по крайней мере один другой основной разработчик должен просмотреть и одобрить).
  - Чтобы сохранить чистую историю и сделать обзор и объединение проще, ветви функций должны быть перенастроены на текущую «разработку» (или «хардфорк») перед созданием PR.
  - Слияния всегда выполняются как настоящие слияния.
3. Базовые разработчики координируют регулярные слияния из "develop" в "hardfork".
4. "develop" и "hardfork" должны оставаться совместимыми с основной сетью, то есть полный откат должен быть возможным..

|

--------------

Как создать релиз
---------------------------

Для выпуска,

0. Изучить документацию 

  1) Проверьте, нужно ли повышать, DB_VERSION чтобы принудительно воспроизвести после обновления: если есть изменение схемы данных или логика, которая влияет на исторические данные, ответ - да. 
  2) Версия FC обычно поднималась уже во время разработки, но это не повредит, если проверить снова.
  3) Bump docs sub-module which links to wiki.

1. A "release" branch is created based on "develop" or "hardfork".
2. The "release" branch is merged into "testnet".
3. For a hardfork release, the hardfork date is adapted directly on the testnet branch.
4. The "testnet" branch is tagged as test-version.
5. Bugfixes for the release are created on the "release" branch and merged into "testnet". Additional test-versions are tagged as needed.
6. After sufficient testing, the release must be approved. In the case of a hardfork release, witness approval is required.
7. After approval, the mainnet hardfork date is decided and set in the "release" branch.
8. The "release" branch is merged into "master", and a version tag is created on "master".
9. The "release" branch is merged back into "develop" and "hardfork".
10. The "release" branch is merged into "testnet". This will produce a merge conflict for the hardfork dates, which must be resolved without changing the testnet hardfork date.
11. Update ``Doxyfile`` with the last version tag. Update online code documentation by using updated ``Doxyfile`` as config file in the ``master`` branch. Send pull request to https://github.com/bitshares/bitshares.github.io with new content in html format.Send pull to https://github.com/bitshares/dev.bitshares.works with new content in xml format.
12. Update `download page of bitshares.org site <https://github.com/bitshares/bitshares.github.io/blob/master/_includes/download.html>`_
13. Create binaries for linux, macos and windows. Once the tag name is known create binaries for this 3 OS. Attach them to release notes. 

  - Example: https://github.com/bitshares/bitshares-core/releases/tag/2.0.181105 Binaries names for this release:
  
    - Linux: BitShares-core-2.0.181105-Linux-cli-tools.tar.gz
    - Windows: BitShares-Core-2.0.181105-Windows-x64-cli-tools.zip
    - macOS: BitShares-Core-2.0.181105-macOS-cli-tools.tar.gz

	
**Note:** Solving conflicts by github(web) will merge branches in unintended directions. Avoid solving this way, merge and resolve conflicts manually through the git command line. Conflicts generally occur when merging release to testnet.

**Note 2:** Follow command line github suggestion to resolve conflicts but at the end of the process you will not have permission to merge directly to ``testnet``, never push the fix to ``release``. Create a new branch and push there, then create a new pull request between ``testnet`` and ``new_branch``, merge ``new_branch`` to ``testnet`` and ``release`` will be automatically added to the merge.

**Note 3:** When creating tag for testnet do it from the command line with ``git tag``. Github don't have the option to create a tag without a release.

**Note 4:** :strike:`the tag commit can be changed`. Don't change tags on github. This is a source of confusion, and of irreproducible bug reports. Make new one is better (ex: test-2.0.180321b or wait 1 day).

**Note 5:** Do not mark releases as "pre release" unless there is a real new version coming immediately after. Never upgrade "pre release" to "release" as new emails to subscribers will not be sent when doing so.

|

--------------

How To Create an Emergency Fix
-------------------------------------

An emergency fix may become necessary when a serious problem in mainnet is discovered. The goal here is to fix the problem as soon as possible, while keeping the risk for creating additional problems as low as possible.

First of all, the problem must be analyzed and debugged. This happens, naturally, directly on the release version.

Presumably the developer who creates the fix will work on his private master branch. That is OK. But for publishing the fix, the following steps should be taken:

Emergency Fix Workflows
-----------------------------

.. image:: ../../_static/structures/bts-emergency-fix.png
        :alt: BitShares
        :width: 750px
        :align: center
		

1. The fix is applied to the version of the "release" branch that was merged into ``master`` when creating the broken release version.
2. The ``release`` branch is merged into ``master``, and a version tag is created on ``master``.
3. Witnesses update to the new version, and production continues.
4. A unit test is created on ``develop`` that reproduces the problem.
5. The ``release`` branch is merged into ``develop``, and it is verified that the fix resolves the problem, by running the unit test.
6. The ``release`` branch is merged into ``hardfork`` and ``testnet``.



|

|

