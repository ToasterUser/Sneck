Підписання або відхилення е-ТТН перевізником
###################################################################################################

.. сюда закину немного картинок для текста

.. |drop_pass| image:: signing/drop_pass.png

.. |del_key| image:: signing/del_key2.png

.. role:: red

.. role:: underline

.. contents:: Зміст:
   :depth: 6

---------

Відправлена з боку вантажовідправника е-ТТН відображається в папці "Вхідні".

.. image:: pics_Signing_rejection_ETTN_carrier/Signing_rejection_ETTN_carrier_14.png
   :align: center

.. important::
   Підписання е-ТТН **Перевізником** можливе тільки після підписання **Вантажовідправником** (статус документу – **"Очікує підписання водієм / перевізником"** ). Також Перевізник може виступати в якості завершальної ланки документообігу, коли всі учасники документообігу вже підписали документ (опціонально). 

Вхідний підписаний документ дозволяє "Підтвердити" (1) та "Підписати" (2) чи "Відхилити" (3) документ.

.. image:: pics_Signing_rejection_ETTN_carrier/Signing_rejection_ETTN_carrier_15.png
   :align: center

.. important::
   В залежності від внутрішньої схеми **"Перевізника"** документ перед "Підписанням" може бути "Підтверджений" водієм, (кнопка **"Підтвердити"**) і відповідно цей документ у вхідних змінить свій статус на **"Очікує підписання перевізником (підтверджено водієм)"**, підказка в документі:

.. image:: pics_Signing_rejection_ETTN_carrier/Signing_rejection_ETTN_carrier_16.png
   :align: center

Також в **"Історії змін статусів"** відображається інформація про співробітника, що здійснив "підтвердження".

**Підписання документа**
==============================================================

Для підписання е-ТТН **"Перевізнику"** необхідно відкрити документ та натиснути на кнопку "Підписати".

Відкривається модульне вікно підписання, в якому автоматично вказується водій, в якості особи, що буде здійснювати підписання (поля "Посада" і "П.І.Б." обов'язкові до заповнення). Додатково можливо додати дані експедитора, документи про внесення змін, дані про товарні позиції:

.. image:: pics_Signing_rejection_ETTN_carrier/Signing_rejection_ETTN_carrier_18.png
   :align: center

.. image:: pics_Signing_rejection_ETTN_carrier/Signing_rejection_ETTN_carrier_19.png
   :align: center

.. attention::
   Блоки, що були додані містять обов'язкові поля (відмічені червоною зірочкою :red:`*`). Додаткові блоки можливо "Видалити". 

Після того, як всі обов'язкові поля будуть заповнені потрібно натиснути **"Підписати"**.

.. hint::
   Лише у ролі **"Перевізник"** є можливість підписати за допомогою мобільного додатку "Дія":

   .. image:: pics_Signing_rejection_ETTN_carrier/Signing_rejection_ETTN_carrier_24.png
      :align: center

   При перегляді через ПК відображається qr-код для переходу в мобільний додаток "Дія", а при перегляді через смартфон відображається посилання для переходу в додаток.

Після ініціалізації бібліотеки підписання, система надасть можливість додати ключ для підписання. При :underline:`першому` підписанні у модальному вікні потрібно обрати файл чи токен (1), ввести пароль (2) та натиснути **"Зчитати"** (3) ключ для підписання:

.. image:: signing/file1n.png
   :align: center

.. image:: signing/file2n.png
   :align: center

При успішному додаванні ключа автоматично відобразиться особа, від імені якої буде здійснено підписання. У користувача може бути додано кілька ключів - для вибору потрібного для здійснення операції підписання потрібно проставити відмітку (4) лівою кнопкою миші і натиснути **"Підписати"** (5):

.. image:: signing/file3n.png
   :align: center

.. important::
   Якщо підписання цим ключем вже було здійснено або знайдена невідповідність даних ЄДРПОУ/ІПН (перевірка), то підписання блокується, а користувачу виводиться відповідне повідомлення:

.. image:: signing/wrong_key.png
   :align: center

Додатково в вікні підписання можливо натиснути **"Детальніше"** для того, щоб переглянути інформацію про підписанта; можливо видалити помилкові ключі (|del_key|).

При подальшій роботі з раніше доданим ключем/-ами потрібно вводити лише пароль для обраного ключа:

.. image:: signing/file4n.png
   :align: center

.. image:: signing/file5n.png
   :align: center

Після підписання е-ТТН додається інформація щодо підписантів документа, документ змінює свій статус на **"Очікує підписання вантажоодержувачем"**:

.. image:: pics_Signing_rejection_ETTN_carrier/Signing_rejection_ETTN_carrier_17.png
   :align: center

Підписаний документ відображається в журналі вхідних документів:

.. image:: pics_Signing_rejection_ETTN_carrier/Signing_rejection_ETTN_carrier_20.png
   :align: center

**Відхилення документа**
==============================================================

У **Перевізника** є можливість відхилити е-ТТН до того, як документ буде підписано **Перевізником**. Для цього потрібно натиснути на кнопку **"Відхилити"**:

.. image:: pics_Signing_rejection_ETTN_carrier/Signing_rejection_ETTN_carrier_21.png
   :align: center

Після чого в модульному вікні обов'язково потрібно заповнити причину відміни документа:

.. image:: pics_Signing_rejection_ETTN_carrier/Signing_rejection_ETTN_carrier_12.png
   :align: center

.. image:: pics_Signing_rejection_ETTN_carrier/Signing_rejection_ETTN_carrier_22.png
   :align: center

Для відхиленної **"Перевізником"** еТТН присвоюється статус "Скасовано водієм / перевізником". Також в **"Історії змін статусів"** відображається інформація про співробітника, що здійснив "відхилення". Документ зі статусом "Відхилено" відображається у "Вхідних" **"Перевізника"**. Документообіг завершено.

.. image:: pics_Signing_rejection_ETTN_carrier/Signing_rejection_ETTN_carrier_23.png
   :align: center

---------------------------------

.. include:: kontakti.rst

