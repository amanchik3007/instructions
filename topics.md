

<p><a href="https://t.me/botdockercontainercreatorbot" data-card-appearance="inline">https://t.me/botdockercontainercreatorbot</a> </p>
<p />
<p>Доброго времени суток, в этом полном гайде я вам расскажу, как настраивать и пользоваться нашей системой топиков для обработки. Как вы знаете, в Telegram есть функция для создания групп с так называемыми топиками, это выглядит так:</p>
<p /><ac:image ac:align="center" ac:layout="center" ac:original-height="712" ac:original-width="380" ac:custom-width="true" ac:alt="image-20240424-134239.png" ac:width="116"><ri:attachment ri:filename="image-20240424-134239.png" ri:version-at-save="1" /></ac:image>
<p>Мы решили использовать эту функцию для оптимизации работы обработчиков, повышения реинтеншена и вовлечения клиентов, а также мы добавили много интересных функций для работы с топиками:</p>
<ul>
<li>
<p>Возможность пометить топик клиента, как reg или dep. Помимо визуального разделения, можно будет запустить спам только по регам или депам</p></li>
<li>
<p><ac:inline-comment-marker ac:ref="97ceb92e-a3b5-4b67-a05f-8ee637ca67f1">Возможность перевода на 15 языков. Для работы с мультигео или просто гео с неизученным для обработки языков добавлена нейросеть-переводчик. Обработка сможет писать в топики по-русски, а клиенту будет отправляться сообщение, переведенное на его язык и наоборот</ac:inline-comment-marker></p></li>
<li>
<p>Спам. В любой момент можно будет проспамить аудиторию любым видом контента телеграм (видео, фото, видеосообщения, текст и тд). При этом можно будет отфильтровать аудиторию по времени последнего взаимодействия, регам и депам</p></li>
<li>
<p>Приветственное и прощальное сообщение. Можно настроить любое количество сообщений которые будут отправляться каждому пользователю при подписке на канал, на который идет траффик. Также при отписке пользователю будет отправляться прощальное сообщение, которое также можно настроить</p></li>
<li>
<p>Возможность настройки первых пяти сообщений от аккаунта. Для того, чтобы не тратить время обработчиков на приветствия новых клиентов, можно настроить до пяти сообщений отправляющихся автоматически</p></li>
<li>
<p>Сбор статистики. Наша система будет собирать статистику по проекту в целом (количество новых и старых тикетов за интервал времени) и каждому обработчику отдельно (среднее время ответа, количество обработанных тикетов)</p></li></ul>
<p />
<ol start="1">
<li>
<p><strong>Создание группы с топиками для обработки</strong></p>
<p>Создайте группу телеграмм и в ее настройках включите ползунок топиков (тем). Таким образом группа будет адаптирована под нашу систему.</p></li></ol>
<p /><ac:image ac:align="center" ac:layout="center" ac:original-height="443" ac:original-width="269" ac:custom-width="true" ac:alt="image-20240425-200612.png" ac:width="197"><ri:attachment ri:filename="image-20240425-200612.png" ri:version-at-save="1" /></ac:image><ac:image ac:align="center" ac:layout="center" ac:original-height="740" ac:original-width="950" ac:custom-width="true" ac:alt="image-20240425-200704.png" ac:width="370"><ri:attachment ri:filename="image-20240425-200704.png" ri:version-at-save="1" /></ac:image>
<p />
<ol start="2">
<li>
<p><strong>Создание Telegram бота</strong></p>
<p>Вам нужно создать телеграм бота через @BotFather (официальный бот телеграм для создания ботов), указать его имя и юзернейм и настроить его внешний вид под себя. После создания вы получите токен бота который нужно скопировать.</p>
<p>Для привязки ботов к нашей системе используйте <a href="https://t.me/botdockercontainercreatorbot" data-card-appearance="inline">https://t.me/botdockercontainercreatorbot</a> </p>
<p>Выберите пункт &ldquo;Добавить бота&rdquo; и отправьте скопированный токен. Созданный вами бот привязан к нашей системе и теперь можно нажать в нем START и настроить под нужный проект</p></li>
<li>
<p><strong>Добавление в администраторы</strong></p>
<p>Вам нужно добавить созданного бота в канал вашего проекта (на который вы льете трафик) и в группу с топиками, а также сделать и там, и там администраторами</p></li>
<li>
<p><strong>Настройка бота</strong></p>
<p>В созданном вами боте выберите пункт &ldquo;Настроить бота&rdquo; для открытия меню настроек:<br /></p><ac:image ac:align="center" ac:layout="center" ac:original-height="304" ac:original-width="259" ac:custom-width="true" ac:alt="image-20240425-201637.png" ac:width="259"><ri:attachment ri:filename="image-20240425-201637.png" ri:version-at-save="1" /></ac:image>
<p />
<ul>
<li>
<p>Группа для обработчиков - нужно отправить id группы с топиками для привязки ее к боту (id группы можно получить добавив в нее любого бота для получения id например <a href="https://t.me/chatIDrobot" data-card-appearance="inline">https://t.me/chatIDrobot</a>  )<br /></p><ac:image ac:align="center" ac:layout="center" ac:original-height="647" ac:original-width="325" ac:custom-width="true" ac:alt="image-20240425-202622.png" ac:width="183"><ri:attachment ri:filename="image-20240425-202622.png" ri:version-at-save="1" /></ac:image>
<p> </p></li>
<li>
<p><ac:inline-comment-marker ac:ref="a2841b90-a94c-406e-b349-36c960723d32">Задержка перед ответом - нужно ввести два числа через пробел (в секундах), это будет интервал в рамках которого юзербот выбирает случайную задержку перед ответом клиентов, это создает имитацию живого общения при отправке автоматических сообщений</ac:inline-comment-marker><br /></p><ac:image ac:align="center" ac:layout="center" ac:original-height="647" ac:original-width="325" ac:custom-width="true" ac:alt="image-20240425-202646.png" ac:width="181"><ri:attachment ri:filename="image-20240425-202646.png" ri:version-at-save="1" /></ac:image>
<p> </p><ac:image ac:align="center" ac:layout="center" ac:original-height="59" ac:original-width="764" ac:custom-width="true" ac:alt="image-20240425-203850.png" ac:width="712"><ri:attachment ri:filename="image-20240425-203850.png" ri:version-at-save="1" /></ac:image>
<p> </p></li>
<li>
<p>Задержка при спаме - нужно ввести два числа через пробел, это будет интервал в рамках которого юзербот выбирает задержку между сообщениями юзерам при спаме, то есть отправив спам одному он подождет столько секунд прежде чем отправить другому, это нужно чтобы спам не остановился за флуд<br /></p><ac:image ac:align="center" ac:layout="center" ac:original-height="647" ac:original-width="325" ac:custom-width="true" ac:alt="image-20240425-202715.png" ac:width="177"><ri:attachment ri:filename="image-20240425-202715.png" ri:version-at-save="1" /></ac:image>
<p>  </p></li>
<li>
<p>Приветственное сообщение - можно отправить сколько угодно сообщений любого вида контента, которые бот будет копировать и отправлять пользователю при подписке на канал проекта</p>
<p> </p><ac:image ac:align="center" ac:layout="center" ac:original-height="647" ac:original-width="325" ac:custom-width="true" ac:alt="image-20240425-202753.png" ac:width="169"><ri:attachment ri:filename="image-20240425-202753.png" ri:version-at-save="1" /></ac:image>
<p> </p></li>
<li>
<p>Прощальное сообщение - одно сообщение, которое бот отправит при отписке пользователя от канала<br /></p><ac:image ac:align="center" ac:layout="center" ac:original-height="647" ac:original-width="325" ac:custom-width="true" ac:alt="image-20240425-202814.png" ac:width="167"><ri:attachment ri:filename="image-20240425-202814.png" ri:version-at-save="1" /></ac:image>
<p> </p></li>
<li>
<p><ac:inline-comment-marker ac:ref="cf8269e9-a551-41d3-af1d-f3d4f2b1ef9c">Реферальная ссылка - для каждого проекта можно сразу настроить реферальную ссылку, чтобы она автоматически менялась. Замена происходит следующим образом - если в тексте встречен фрагмент &ldquo;/ref&ldquo;, то он автоматически заменяется на указанную рефералку, это исключает возможность ошибочной отправки не той ссылки</ac:inline-comment-marker><br /></p><ac:image ac:align="center" ac:layout="center" ac:original-height="647" ac:original-width="325" ac:custom-width="true" ac:alt="image-20240425-202836.png" ac:width="181"><ri:attachment ri:filename="image-20240425-202836.png" ri:version-at-save="1" /></ac:image>
<p> </p></li>
<li>
<p><ac:inline-comment-marker ac:ref="0a723a4a-95bb-46aa-bd53-b5cb4f1513cf">1,2,3,4,5 сообщения - их можно настроить по желанию, чтобы бот ответил на 1,2,3,4,5 сообщение пользователя заготовленным текстом. Чтобы не настраивать то или иное сообщение, отправьте текстовое сообщение &ldquo;NULL&ldquo;</ac:inline-comment-marker><br /></p><ac:image ac:align="center" ac:layout="center" ac:original-height="647" ac:original-width="325" ac:custom-width="true" ac:alt="image-20240425-202931.png" ac:width="187"><ri:attachment ri:filename="image-20240425-202931.png" ri:version-at-save="1" /></ac:image>
<p> </p></li>
<li>
<p>Язык для перевода - можно выбрать язык, на который нейросеть будет переводить сообщения от обработчика и обратно, перевод осуществляется с русского<br /></p><ac:image ac:align="center" ac:layout="center" ac:original-height="647" ac:original-width="325" ac:custom-width="true" ac:alt="image-20240425-202954.png" ac:width="185"><ri:attachment ri:filename="image-20240425-202954.png" ri:version-at-save="1" /></ac:image>
<p> </p></li>
<li>
<p><ac:inline-comment-marker ac:ref="1a3eb616-ffab-4d93-8373-9612f32deb8c">Создание топика при подписке на канал - по умолчанию выключено</ac:inline-comment-marker></p>
<ul>
<li>
<p>Отключено - создание топика только если пользователь сам написал в бота</p></li>
<li>
<p>Включено - создание топика сразу при подписке на канал, таким образом можно самостоятельно написать человеку как только он подпишется на канал и не ждать интеракции с его стороны<br /><br /></p><ac:image ac:align="center" ac:layout="center" ac:original-height="647" ac:original-width="325" ac:custom-width="true" ac:alt="image-20240425-203025.png" ac:width="164"><ri:attachment ri:filename="image-20240425-203025.png" ri:version-at-save="1" /></ac:image>
<p> </p></li></ul></li>
<li>
<p>Перессылка спама в топики - по умолчанию включено, рекомендуется отключить, при запуске спама дублирует сообщения в соответствующие топики<br /></p><ac:image ac:align="center" ac:layout="center" ac:original-height="647" ac:original-width="325" ac:custom-width="true" ac:alt="image-20240425-203101.png" ac:width="167"><ri:attachment ri:filename="image-20240425-203101.png" ri:version-at-save="1" /></ac:image>
<p> </p></li></ul></li>
<li>
<p><strong>Добавление обработчиков</strong></p>
<p>Кроме добавления обработчиков в саму группу для топиков, вам нужно отправить их айдишники в созданного вами <ac:inline-comment-marker ac:ref="4fa84ac2-ea3e-45b6-9ad0-c72d813eab3d">бота</ac:inline-comment-marker>, используя кнопку Добавить нового обработчика. Далее вам просто нужно будет отправить id обработчика, это необходимо для сбора статистики по обработчику в нашей базе данных.<br /></p><ac:image ac:align="center" ac:layout="center" ac:original-height="308" ac:original-width="268" ac:custom-width="true" ac:alt="image-20240425-203154.png" ac:width="213"><ri:attachment ri:filename="image-20240425-203154.png" ri:version-at-save="1" /></ac:image>
<p /></li>
<li>
<p> <strong>Статусы в топиках</strong><br />Важная особенность системы топиков заключается в автоматическом трекинге статуса пользователей (клиентов), написавших боту.<br />Имеются следующие статусы:</p>
<ul>
<li>
<p>Новый клиент (💎) - таким статусом помечаются все новый клиенты, пока их сообщения обрабатываются системой автоответчика бота</p></li>
<li>
<p>Неотвеченное (❗❗) - таким статусом помечаются топики, в которых есть новые сообщения со стороны пользователя, на которые не было ответа со стороны обработчиков</p></li>
<li>
<p>Отвеченное (✅) - таким статусом помечаются топики, где последнее сообщение было со стороны обработчика</p></li></ul></li></ol><ac:structured-macro ac:name="note" ac:schema-version="1" ac:macro-id="7988d6dc-0af1-4329-91af-245fa6549c6d"><ac:rich-text-body>
<p>Важно: если топик помечен статусом из списка ниже, к нему перестают применяться статусы прочитанно/непрочитанно, такой топик требует ручной проверки</p></ac:rich-text-body></ac:structured-macro>
<p />
<ul>
<li>
<p>Рег (🔥) - пользователь в топике зарегистрировался по отправленной ссылке</p></li>
<li>
<p>Деп (💰) - пользователь в топике оформил депозит</p></li></ul><ac:structured-macro ac:name="info" ac:schema-version="1" ac:macro-id="11f8981e-4538-4355-b82c-b45c8776a69d"><ac:rich-text-body>
<p>Статусы &ldquo;новый клиент&ldquo;, &ldquo;прочитанное&ldquo; и &ldquo;непрочитанное&ldquo; проставляются автоматически, а статусы reg и dep - вручную</p></ac:rich-text-body></ac:structured-macro>
<p />
<ol start="7">
<li>
<p><strong><ac:inline-comment-marker ac:ref="a40654df-1bd9-4ed0-aa2f-dc4b77476fdf">Команды в топиках</ac:inline-comment-marker></strong></p>
<ol start="1">
<li>
<p><ac:inline-comment-marker ac:ref="9b89fa6c-ed15-407e-80ee-18c66ede00bc">/reg - установить в топике статус рег</ac:inline-comment-marker></p></li>
<li>
<p><ac:inline-comment-marker ac:ref="9b89fa6c-ed15-407e-80ee-18c66ede00bc">/dep - установить в топике статус деп</ac:inline-comment-marker></p></li>
<li>
<p><ac:inline-comment-marker ac:ref="ee6ac1e6-8fde-42c8-975e-0dcc660a8845">/del - в случае ошибки вы можете быстро удалить любое свое сообщение ответив на него командой /del, тогда оно удалиться и для вас и для пользователя. Удаление происходит бесследно, как если бы оно было удалено в телеграме после отправки</ac:inline-comment-marker></p></li>
<li>
<p>/top - эту команду нужно прописывать в General группы для топиков, она продублирует последнее сообщение каждого непрочитанного диалога и таким образом поднимет все пропущенные диалоги наверх, что позволит не пропустить сообщение от клиента</p></li></ol></li></ol><ac:image ac:align="center" ac:layout="center" ac:original-height="59" ac:original-width="281" ac:custom-width="true" ac:alt="image-20240425-221659.png" ac:width="323"><ri:attachment ri:filename="image-20240425-221659.png" ri:version-at-save="1" /></ac:image>
<p style="margin-left: 30.0px;">e.<ac:inline-comment-marker ac:ref="e8b35821-27b3-439a-b2da-b685aa14cf0b"> /topreg dd-mm-yyyy - этой командой наверх поднимутся реги (Это для тех кто регнулся но не пополнил) </ac:inline-comment-marker></p>
<p style="margin-left: 30.0px;"><ac:inline-comment-marker ac:ref="e8b35821-27b3-439a-b2da-b685aa14cf0b">f. /topdep dd-mm-yyyy - этой командой наверх поднимутся депы (Для тех кто регнулся и пополнил)</ac:inline-comment-marker></p>
<p />
<ol start="8">
<li>
<p><strong>Спам</strong></p></li></ol>
<p>Вы можете запустить спам по аудитории нескольких типов:</p>
<ul>
<li>
<p><ac:inline-comment-marker ac:ref="c243c696-5097-4b82-a94e-cbf72c745e3b">Спам по всем отправит сообщение всем пользователям хоть как то взаимодействовавшим с ботом, в том числе просто подписавшимся на канал. Порядок действий</ac:inline-comment-marker></p>
<ul>
<li>
<p>Вернуться в главное меню (команда &ldquo;/start&ldquo;)</p></li>
<li>
<p>Выбрать &ldquo;запустить спам&ldquo;</p></li>
<li>
<p>Выбрать &ldquo;Спам по всем&ldquo;</p></li>
<li>
<p>Ввести сообщение для отправки</p></li></ul></li>
<li>
<p><ac:inline-comment-marker ac:ref="c243c696-5097-4b82-a94e-cbf72c745e3b">Спам по регам отправит тем, кто был помечен регом, точно так же с депами</ac:inline-comment-marker></p>
<ul>
<li>
<p>Вернуться в главное меню (команда &ldquo;/start&ldquo;)</p></li>
<li>
<p>Выбрать &ldquo;запустить спам&ldquo;</p></li>
<li>
<p>Выбрать &ldquo;Спам по регам&ldquo;</p></li>
<li>
<p>Ввести сообщение для отправки</p></li></ul></li>
<li>
<p><ac:inline-comment-marker ac:ref="c243c696-5097-4b82-a94e-cbf72c745e3b">Также по каждому типу аудитории можно выбрать интервал дат последнего сообщения с ней, чтобы проспамить только свежих клиентов</ac:inline-comment-marker></p>
<ul>
<li>
<p>Вернуться в главное меню (команда &ldquo;/start&ldquo;)</p></li>
<li>
<p>Выбрать &ldquo;запустить спам&ldquo;</p></li>
<li>
<p>Выбрать &ldquo;Спам по всем (по регам, по депам) по дате&ldquo;</p></li>
<li>
<p>Ввести интервал дат в формате: дд-мм-гггг дд-мм-гггг. Всем клиентам, которые отправили или получили любое сообщение из системы в указанный интервал, будет отправлен спам</p></li>
<li>
<p>Ввести сообщение для отправки</p></li></ul></li></ul><ac:image ac:align="center" ac:layout="center" ac:original-height="782" ac:original-width="560" ac:custom-width="true" ac:alt="image-20240424-135040.png" ac:width="174"><ri:attachment ri:filename="image-20240424-135040.png" ri:version-at-save="1" /></ac:image>
<p />
<ol start="9">
<li>
<p><strong>Статистика</strong></p>
<p>Вы можете получить статистику по всему проекту и по каждому обработчику по отдельности за выбранный интервал дат</p></li></ol>
<p />
<p><strong>ДОП ФУНКЦИИ (нужно обращаться к </strong><a href="https://t.me/rtttzzy" data-card-appearance="inline">https://t.me/rtttzzy</a><strong> ):</strong></p>
<p />
<ol start="1">
<li>
<p>Добавление языков</p></li>
<li>
<p>Интеграция с с2с (если пользуетесь TKPartnerStat2.0)</p></li></ol>
