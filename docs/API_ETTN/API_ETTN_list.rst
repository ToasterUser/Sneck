API
###########

.. hint::
    Всі запити нижче перерахованих API методів сервісу "ЕТТН" направляються на адресу: https://edo-v2.edin.ua 

Авторизація
==============

+-----------+-----------------------------+-------------------------------------------------------------------------------------------------+
| **Метод** |       **URL запиту**        |                                            **Опис**                                             |
+===========+=============================+=================================================================================================+
| POST      | ``/api/authorization/hash`` | `Авторизація <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/Authorization.html>`__            |
+-----------+-----------------------------+-------------------------------------------------------------------------------------------------+
| GET       | ``/api/auth_check``         | `Перевірка активності сесії <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/AuthCheck.html>`__ |
+-----------+-----------------------------+-------------------------------------------------------------------------------------------------+

Робота з е-ТТН
============================

+-----------+--------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Метод** |               **URL запиту**               |                                                                         **Опис**                                                                          |
+===========+============================================+===========================================================================================================================================================+
| POST      | ``/api/ettn/eds/ettn/consignor``           | `Створення чернетки нової е-ТТН <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateConsignorETTN.html>`__                                             |
+-----------+--------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/doc/v2/xml``               | `Створення XML документа для подальшого підписання <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateEttnV2XML.html>`__                              |
+-----------+--------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/ettn/v2/eds/doc/body``              | `Отримання (завантаження) документа сервісу «ЕТТН» в JSON/XML/PDF/ZIP форматі <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetDocumentBodyV2.html>`__ |
+-----------+--------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/doc/xml/v2/sign``          | `Підписання даних сервісу "ЕТТН" (збереження підпису) <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/SaveEttnV2Sign.html>`__                            |
+-----------+--------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/ettn/v2/doc/xml``                   | `Отримання XML документа <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetDocXML.html>`__                                                              |
+-----------+--------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PATCH     | ``/api/ettn/eds/doc/read``                 | `Відмітити документ, як "прочитаний" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/MarkDocumentAsRead.html>`__                                         |
+-----------+--------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/ettn/v2/eds/doc/body/final``        | `Отримання фінальної версії е-ТТН (разом зі змінами, що були внесені актами) <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetEttnBodyFinal.html>`__   |
+-----------+--------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/v2/eds/doc/processing_status`` | `Відправка статуса обробки документа ТТН <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/SetProcessingStatus.html>`__                                    |
+-----------+--------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+



Робота з іншими документами сервісу "ЕТТН"
============================================

+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Метод** |             **URL запиту**             |                                                                        **Опис**                                                                        |
+===========+========================================+========================================================================================================================================================+
| POST      | ``/api/ettn/eds/doc/attachment``       | `Створення вкладення до документа <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateDocAttachment.html>`__                                        |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/ettn/eds/doc/attachment``       | `Отримання вкладення документа сервісу "ЕТТН" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetDocAttachment.html>`__                               |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| DELETE    | ``/api/ettn/eds/doc/attachment``       | `Видалення вкладення документа сервісу "ЕТТН" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/DelDocAttachment.html>`__                               |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/booking``              | `Створення/редагування чернетки "Заявка на транспортування" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateBooking.html>`__                    |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/booking/confirmation`` | `Створення/редагування чернетки "Підтвердження транспортування" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateBookingConfirmation.html>`__    |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/acceptance``           | `Створення/редагування чернетки "Акта приймання-передавання" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateAcceptance.html>`__                |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/discrepancy``          | `Створення/редагування чернетки "Акта розбіжностей" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateDiscrepancy.html>`__                        |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/completion``           | `Створення/редагування чернетки "Акта виконаних робіт" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateCompletion.html>`__                      |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PATCH     | ``/api/ettn/eds/doc/from_draft``       | `Створення документу еТТН на основі чернетки, створеної контрагентом <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateFromDraftDocument.html>`__ |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PATCH     | ``/api/ettn/eds/doc/send``             | `Відправка документа сервісу "ЕТТН" з Чернеток <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/DocSend.html>`__                                       |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PATCH     | ``/api/ettn/eds/docs``                 | `Видалення документів сервісу "ЕТТН" з "Чернеток" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/DelDocs.html>`__                                    |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PATCH     | ``/api/ettn/eds/doc/clone``            | `Створити копію документа сервісу "ЕТТН" / Замінити документ е-ТТН <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/DocClone.html>`__                  |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/ettn/eds/doc``                  | `Отримання документа сервісу "ЕТТН" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetDoc.html>`__                                                   |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/ettn/eds/chain``                | `Отримання ланцюжка документів сервісу "ЕТТН" по id ланцюжка чи id документа <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetChain.html>`__        |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/ettn/eds/doc/body``             | `Отримання тіла документа сервісу "ЕТТН" в json форматі <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetDocBody.html>`__                           |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/ettn/eds/doc/signers``          | `Отримання даних підписантів документа сервісу "ЕТТН" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetSignersInfo.html>`__                         |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/ettn/eds/doc/links``            | `Отримання пов'язаних документів сервісу "ETTN" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetLinks.html>`__                                     |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/ettn/eds/doc/xml/ticket``       | `Отримання даних документа сервісу "ЕТТН" для підписання <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetTicket.html>`__                           |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PATCH     | ``/api/ettn/eds/doc/confirm``          | `Підтвердити документ сервісу "ЕТТН" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/DocConfirm.html>`__                                              |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PUT       | ``/api/ettn/eds/doc/reject``           | `Відмовити в підписанні документа сервісу "ЕТТН" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/DocReject.html>`__                                   |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/chains/search``        | `Отримання списку ланцюжків документів сервісу "ЕТТН" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetChainsList.html>`__                          |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/docs/search``          | `Отримання списку документів сервісу "ЕТТН" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetDocList.html>`__                                       |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/doc/xml/sign``         | `Підписання даних сервісу "ЕТТН" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/SaveSignedData.html>`__                                              |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PATCH     | ``/api/ettn/eds/chains/archive``       | `Заархівувати всі документи у вказаному ланцюжку <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/ArcChains.html>`__                                   |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/doc/comment``          | `Додати коментар до документа сервісу "ЕТТН" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/AddComment.html>`__                                      |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/ettn/eds/doc/comments``         | `Отримання коментарів до документу сервісу "ЕТТН" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetComments.html>`__                                |
+-----------+----------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+

Робота з актами ("Акт перевантаження", "Акт розбіжностей до ТТН")
----------------------------------------------------------------------------------------------------

+-----------+------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Метод** |           **URL запиту**           |                                                                               **Опис**                                                                                |
+===========+====================================+=======================================================================================================================================================================+
| POST      | ``/api/ettn/eds/reload``           | `Створення/редагування чернетки "Акта перевантаження" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateReload.html>`__                                          |
+-----------+------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/disagreement``     | `Створення/редагування чернетки "Акта розбіжностей" до е-ТТН <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateDisagreement.html>`__                             |
+-----------+------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/warehouse_change`` | `Створення/редагування чернетки "Акта про заміну пункту призначення вантажу" до е-ТТН <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateWarehouseChange.html>`__ |
+-----------+------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/adjustment``       | `Створення/редагування чернетки "Акта коригування" до е-ТТН <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateAdjustment.html>`__                                |
+-----------+------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/act/xml``          | `Створення XML Акта для подальшого підписання <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CreateActXml.html>`__                                                  |
+-----------+------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| POST      | ``/api/ettn/eds/act/sign``         | `Підписання "Акта" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/SaveActSign.html>`__                                                                              |
+-----------+------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PATCH     | ``/api/ettn/eds/act/send``         | `Відправка "Акта" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/SendAct.html>`__                                                                                   |
+-----------+------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PUT       | ``/api/ettn/eds/act/reject``       | `Відхилити "Акт" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/RejectAct.html>`__                                                                                  |
+-----------+------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Робота з довідниками
============================

+-----------+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Метод** |              **URL запиту**              |                                                                                         **Опис**                                                                                         |
+===========+==========================================+==========================================================================================================================================================================================+
| POST      | ``/api/oas/v2/exdata``                   | `Отримання даних компанії, співробітників, адрес з довідників сервісу "ЕТТН" <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/ExtraData.html>`__                                         |
+-----------+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/oas/v2/company/search``           | `Отримання даних про компанію за назвою / ІНН / ЄДРПОУ <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/CompanySearch.html>`__                                                           |
+-----------+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/oas/v2/company/employees/search`` | `Отримання даних співробіника компанії за назвою / містом / вулицею / кодом КОАТУУ / номером посвідчення водія <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/EmployeesSearch.html>`__ |
+-----------+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/oas/v2/company/addresses/search`` | `Отримання адреси з довідника компанії за назвою / містом / вулицею / кодом КОАТУУ <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/AddressesSearch.html>`__                             |
+-----------+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/oas/v2/koatuu/search``            | `Отримання данних КОАТУУ за назвою / кодом <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/KoatuuSearch.html>`__                                                                        |
+-----------+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/oas/v2/company``                  | `Отримання даних про компанію по ідентифікатору компанії <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetCompany.html>`__                                                            |
+-----------+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| GET       | ``/api/oas/invitation``                  | `Отримання запрошення для незареєстрованого користувача в сервісі ЕТТН <https://wiki.edin.ua/uk/latest/API_ETTN/Methods/GetInvitation.html>`__                                           |
+-----------+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


.. toctree::
   :hidden:
   :glob:

   Methods/*

